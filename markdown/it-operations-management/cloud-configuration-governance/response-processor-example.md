---
title: Virtual server response processor example
description: The Create\_Virtual\_Server\_Response\_Processor script, which is available by default in Cloud Provisioning and Governance, is the response processor that handles the creation of AWS virtual machine CIs.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure a response processor, Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Virtual server response processor example

The **Create\_Virtual\_Server\_Response\_Processor** script, which is available by default in Cloud Provisioning and Governance, is the response processor that handles the creation of AWS virtual machine CIs.

## Create Virtual Server

The Create\_Virtual\_Server\_Response\_Processor resource processor script is available by default on the Virtual Server resource block. Its job is to create a virtual server record in the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table when a new virtual server is provisioned.

All response processors have this first line with these common parameters:

```
function processResponse(response, cloudServiceAccountId, ldc, correlationId,step, requestorContext) {

```

This brings in the response from the cloud provider and the important information, such as the account ID, that is required for the new CI that the system can create. All of these parameters are required for all response processors.

Line 10 parses the response into JSON so that the system can process it. The information is held in the vmResponse variable:

```

var vmResponse = global.JSON.parse(response);

```

Whenever you create or edit a response processor, you must know which inputs are required for the CI type. Line 11 handles one of the necessary inputs, the hardware ID, that the CMDB record requires:

```

var hardwareId = vmResponse.hardwareId;

```

Line 39 shows the information that is required for the system to identify the new virtual server and related CIs, so the information can be put into the CMDB. In this case, the service account object ID identifies the account associated with the virtual server, the datacenter object ID identifies the datacenter in which the virtual server lives, and the virtual machine instance object ID identifies the virtual server itself. This identification code block prevents the creation of duplicate CIs.

```

var vmInfo = {
    "cmdb_ci_vm_instance": {
      "validator": "virtual_machine_create_update_validator",
      "validator_overrides": {},
      "identification": {
        "cmdb_ci_cloud_service_account": {
          "criterion": {
            "object_id": cloudServiceAccountId
          }
        },
        "cmdb_ci_aws_datacenter": {
          "criterion": {
            "object_id": ldc
          }
        },
        "cmdb_ci_vm_instance": {
          "criterion": {
            "object_id": vmResponse.nodeId
          }
        }
      },
```

Attributes are populated into the fields on in the cmdb\_ci\_vm\_instance table. These attributes are defined in line 61:

```

"attributes": {
  "name": vmResponse.nodeName,
  "object_id": vmResponse.nodeId,
  "state": status_map[vmResponse.state],
  "dns_suffix": vmResponse.dnsSuffix,
  "cpus": vmCPUs,
  "memory": vmMemory,
  "disks": vmResponse.volumes.length,
  "disks_size": "",
  "nics": vmResponse.networkInterfaces.length,
  "terminated_on": "",
  "termination_protection": "",
  "ip_address": vmPubIPAddr,
  "assigned_to": reqContext.userId,
  "assignment_group": reqContext.groupId
},

```

References to other CIs can also be included in the response processor. In this case, the OS template that the virtual server is based on is identified by first identifying the object ID of the service account and the datacenter along with the actual OS template.

```

"references": {
  "cmdb_ci_os_template": {
    "identification": {
      "cmdb_ci_cloud_service_account": {
        "criterion": {
          "object_id": cloudServiceAccountId
        }
      },
      "cmdb_ci_aws_datacenter": {
        "criterion": {
          "object_id": ldc
        }
      },
      "cmdb_ci_os_template": {
        "criterion": {
          "object_id": imageIdTrim
        }
      }
    },
```

The following code block adds the object ID of the OS image to the attributes list so that this information can be populated into the virtual server CMDB record.

```

"attributes": {
  "object_id": imageIdTrim
}

```

This code block performs additional identification on the Compute template \(the hardware type\) and then add it to the attributes:

```

"cmdb_ci_compute_template": {
  "identification": {
    "cmdb_ci_cloud_service_account": {
      "criterion": {
        "object_id": cloudServiceAccountId
      }
    },
    "cmdb_ci_aws_datacenter": {
      "criterion": {
        "object_id": ldc
      }
    },
    "cmdb_ci_compute_template": {
      "criterion": {
        "object_id": vmResponse.hardwareId
      }
    }
  },
  "attributes": {
    "object_id": vmResponse.hardwareId,
    "name": vmResponse.hardwareId
  }
}
```

Additional code sections make the relationship with network interfaces and identify any storage attached to the virtual server.

This mandatory code block pushes the data to the CMDB and returns the JSON string:

```

cloudModelString.push(vmInfo);
return global.JSON.stringify(cloudModelString);

```

**Parent Topic:**[Configure a response processor](../task/configure-response-processor.md)

