---
title: Sample payload for BYOL
description: A sample payload that populates the Software Installation \[cmdb\_sam\_sw\_install\] table in the ServiceNow instance with discovery data collected by the BYOL licensing model.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Sample payload for BYOL

A sample payload that populates the Software Installation \[cmdb\_sam\_sw\_install\] table in the ServiceNow instance with discovery data collected by the BYOL licensing model.

Certain entities need to be populated for BYOL to work with software asset connection as a third party discovery source. The relationship between these entities is crucial for BYOL to work smoothly with software asset connections. For example, some values required for populating Cloud Hosts is different for AWS and Azure. Though the object ID and the name of the host is required for both AWS and Azure, for AWS, the CPU core count is required and for Azure, the host type value is required. For details on entities and their relationships, refer to [Entities for BYOL](sample-payload-byol.md#section_b4d_c5r_nnb) and [Relationships between the entities for BYOL](sample-payload-byol.md#section_xfc_ycs_nnb).

In this example, Cloud Service Account is the topmost entity. All the other entities listed in the Entities for BYOL table are dependent entities of Cloud Service Account. If an entity is marked as a dependent entity, then the parent entity and the relationship between that entity and it's parent needs to be mentioned in the same payload. For example, if you want to create an AWS data center on Cloud Service Account, you need to include the Cloud Service Account entity in the same payload; even if Cloud Service Account already exists in your instance. Similarly, when you create software installations, you need to include all the dependent entities for software installations all through the hierarchy in the same payload.

## Entities for BYOL

<table id="table_t15_bds_nnb"><thead><tr><th>

Entities

</th><th>

Required fields

</th></tr></thead><tbody><tr><td>

Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

</td><td>

account\_id – Unique identifier

</td></tr><tr><td>

AWS Datacenters \[cmdb\_ci\_aws\_datacenter\]

</td><td>

object\_id – Unique identifier

</td></tr><tr><td>

Azure Datacenters \[cmdb\_ci\_azure\_datacenter\]

</td><td>

object\_id – Unique identifier

</td></tr><tr><td>

Cloud Hosts \[cmdb\_ci\_cloud\_host\] **Note:** Not needed for shared VMs.

</td><td>

-   object\_id – Unique identifier
-   name - name of the host
-   host\_type - host type for Azure. For example, DSv3-Type1 \(for Azure hosts only\).
-   cpu\_core-count - Total CPU core count of the host \(for AWS hosts only\).

</td></tr><tr><td>

Virtual Machine Instances \[cmdb\_ci\_vm\_instance\]

</td><td>

object\_id – Unique identifier

</td></tr><tr><td>

Computers \[cmdb\_ci\_computer\]

</td><td>

-   name - name of the virtual machine
-   cpu\_count - CPU count of the virtual machine
-   cpu\_core\_count - CPU core count of the virtual machine
-   cpu\_core\_thread - CPU core thread count of the virtual machine
-   virtual – indicates if the computer is a VM \(always set to true\)

</td></tr><tr><td>

Software Installations \[cmdb\_sam\_sw\_install\]

 **Note:** Software Installations \[cmdb\_sam\_sw\_install\] is a related entry for Computers \[cmdb\_ci\_computer\]

</td><td>

-   publisher
-   version
-   display\_name
-   cloud\_license\_type - license type of the cloud install \(BYOL or License Included\)
-   cloud\_license\_type\_source - source from where cloud license type gets populated. The value is set to third\_party\_integration for Software asset connections.

</td></tr></tbody>
</table>## Relationships between the entities for BYOL

|Entity relationships|Type|Parent|Child|
|--------------------|----|------|-----|
|AWS/Azure Datacenters – Cloud Service Account|Hosted on::Hosts|AWS/Azure Datacenters|Cloud Service Account|
|AWS/Azure Datacenters – Cloud Hosts|Hosted on::Hosts|Cloud Hosts|AWS/Azure Datacenters|
|AWS/Azure Datacenters – Virtual Machine Instances|Hosted on::Hosts|Virtual Machine Instances|AWS/Azure Datacenters|
|Cloud Hosts - Virtual Machine Instances|Runs on::Runs|Virtual Machine Instances|Cloud Hosts|
|Computers - Virtual Machine Instances|Virtualized by::Virtualizes|Computers|Virtual Machine Instances|

## Sample payload for Computer and Installations for dedicated VM \(similar for AWS and Azure\)

In this sample payload, a dedicated computer record is being passed. This computer record has a related array that contains all the software installations. A VM instance corresponds to the computer record. Cloud host is the dedicated host on which the virtual machine resides and the AWS datacenter is to be created on the Cloud Service Account. If you have multiple dedicated virtual machines, you can send one REST API for each dedicated virtual machine. For example, if you have 50 dedicated VMs, you need to send 50 REST API calls each having the same payload. All the software installations on a dedicated VM can be sent in a single payload in the related array.

```
var payload = { 

  'items': [{ 

    'className': 'cmdb_ci_computer', 

    'values': { 

      'name': 'Comp - Dedicated AWS - 1', 

      'cpu_count': 1, 

      'cpu_core_count': 4, 

      'cpu_core_thread': 1, 

      'virtual': true 

    }, 

    'related': [{ 

      'className': 'cmdb_sam_sw_install', 

      'values': { 

        'publisher': 'Microsoft', 

        'display_name': 'SQL Server', 

        'version': '2017', 

        'cloud_license_type': 'BYOL', 

        'cloud_license_type_source': 'third_party_integration' 

      } 

    }] 

  }, { 

    'className': 'cmdb_ci_vm_instance', 

    'values': { 

      'object_id': 'sample_object_id_aws_vm_dedicated', 

      'name': 'VM Dedicated AWS - 1', 

    } 

  }, { 

    'className': 'cmdb_ci_cloud_host', 

    'values': { 

      'object_id': 'sample_object_id_aws_host', 

      'name': 'AWS Dedicated Host - 1', 

      'cpu_core_count': 32 

    } 

  }, { 

    'className': 'cmdb_ci_aws_datacenter', 

    'values': { 

      'object_id': 'sample_object_id_aws_dc', 

      'name': 'AWS DataCenter - 1' 

    } 

  }, { 

    'className': 'cmdb_ci_cloud_service_account', 

    'values': { 

      'account_id': 'sample_account_id_aws_service_account', 

      'name': 'Cloud Service Account AWS - 1' 

    } 

  }], 

  'relations': [{ 

      'type': 'Virtualized by::Virtualizes', 

      'parent': 0, 

      'child': 1 

    }, { 

      'type': 'Runs on::Runs', 

      'parent': 1, 

      'child': 2 

    }, 

    { 

      'type': 'Hosted on::Hosts', 

      'parent': 2, 

      'child': 3 

    }, { 

      'type': 'Hosted on::Hosts', 

      'parent': 3, 

      'child': 4 

    } 

  ] 

} 

 
 var jsonUntil = new JSON(); 

var input = jsonUntil.encode(payload); 

gs.info("Input: " + input.toString()); 

var options = { 

  "partial_payloads": false, 

  "deduplicate_payloads": true 

}; 

var output = SNC.IdentificationEngineScriptableApi.createOrUpdateCIEnhanced('ServiceNow', input, options); 

gs.print("Output:" + output); 
```

**Parent Topic:**[Software Asset Management references](references.md)

