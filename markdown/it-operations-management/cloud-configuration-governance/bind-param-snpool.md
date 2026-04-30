---
title: Bind a parameter to a resource pool
description: To make catalog ordering less error-prone, you can bind a parameter to an resource pool \(a pool provided in the base system\). Parameters that are based on an resource pool list only specified values from existing tables on the catalog order form in the Cloud User Portal.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Pools and Filters for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Bind a parameter to a resource pool

To make catalog ordering less error-prone, you can bind a parameter to an resource pool \(a pool provided in the base system\). Parameters that are based on an resource pool list only specified values from existing tables on the catalog order form in the Cloud User Portal.

## Before you begin

Role required: sn.cmp.cloud\_service\_designer

## About this task

The catalog order form lists only parameters values that have the **datasource** specified. For example, if you use the **Resource Group Name** parameter in your template, you can bind the **Resource Group Name** field to an existing SN pool \(**ResourceGroupPool**\) in the metadata section.

When you create a resource block using a cloud template, you can bind a parameter to an SN pool in the metadata section of the Azure Resource Manager \(ARM\) or CloudFormation \(CF\) template. All SN pools are listed in the procedure.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud Catalog Items**.

2.  Select an existing template or click **New** to create a new cloud template.

    If you select an existing template, rename the template.

    In the next step, you modify the template definition for the appropriate template type \(choose ARM or CloudFormation\). You specify the SN pool filter as the **datasource** value.

<table id="table_phv_yqq_4bb"><thead><tr><th>

SN Pool

</th><th>

Filter

</th></tr></thead><tbody><tr><td>

AvailabilityZonePool

</td><td>

getAllObjects: Gets all availability zones.

 getObjectsByLDC: Gets availability zone depending on LDC.

</td></tr><tr><td>

HardwareTypePool

</td><td>

 

</td></tr><tr><td>

ImagePool

</td><td>

 

</td></tr><tr><td>

LoadBalancerPool

</td><td>

All: Gets all load balancers.

</td></tr><tr><td>

NetworkPool

</td><td>

getAllObjects: Gets all networks.

 getObjectsByLDC: Gets networks depending on LDC.

</td></tr><tr><td>

ResourceGroupPool

</td><td>

getObjectsByLDC: Gets resource groups depending on LDC.

</td></tr><tr><td>

SecurityGroupPool

</td><td>

getObjectsByNetwork: Gets all security groups.

</td></tr><tr><td>

SecurityGroupProfilePool

</td><td>

All: Gets all security group profiles.

</td></tr><tr><td>

SSHKeyPool

</td><td>

UserKeys: Gets all SSH keys.

</td></tr><tr><td>

StorageAccountPool

</td><td>

getObjectsByLDC: Gets storage accounts depending on LDC.

</td></tr><tr><td>

StorageVolumePool

</td><td>

All: Gets all storage volumes.

</td></tr><tr><td>

SubnetPool

</td><td>

getObjectsByNetwork:Gets all subnets.

</td></tr><tr><td>

VirtualMachinePool

</td><td>

getByAvailabilityZone: Gets all virtual machines.

</td></tr></tbody>
</table>3.  Modify an ARM template definition:

    1.  Add the attribute **SNC::Parameter::Metadata** in the **parameters** metadata section.

    2.  For the **SNC::Parameter::Metadata** attribute, add datasource as the key and enter an SN pool filter for the value, such as `StorageAccountPool.getObjectsByLDC` as shown in this example.

        ```
        "parameters": {
            "newStorageAccountName": {
              "type": "string",
              "metadata": {
                "description": "Unique DNS Name for the Storage Account where the Virtual Machine's disks will be placed.",
                 "SNC::Parameter::Metadata": {
                 "allowedPattern": "[0-9a-z]{1,11}",
                 "ConstraintDescription": "must be a alphanumeric ",
                 "datasource":"ServiceNow::Pools::StorageAccountPool.getObjectsByLDC",
         
                } 
              }
            }
        
        ```

4.  Modify a CloudFormation template definition:

    1.  Add the attribute **SNC::Parameter::Metadata** and define the custom attribute name \(**VpcId**\) with a **datasource**.

        For the **datasource** value, enter an SN pool filter such as `NetworkPool.getObjectsByLDC` in this example.

    2.  Define the **datasourceFilter** mapping attribute to bind the custom name \(**VpcId**\) to the actual attribute name \(**Network**\).

        ```
        "Parameters" : { 
         
              "VpcId" : {
              "Type" : "AWS::EC2::VPC::Id",
              "Description" : "VpcId of your existing Virtual Private Cloud (VPC)",
              "ConstraintDescription" : "must be the VPC Id of an existing Virtual Private Cloud."
            },
         
            "SubnetId" : {
              "Type" : "AWS::EC2::Subnet::Id",
              "Description" : "SubnetId of an existing subnet (for the primary network) in your Virtual Private Cloud (VPC)",
              "ConstraintDescription" : "must be an existing subnet in the selected Virtual Private Cloud."
            }
          },
          "Metadata": {
                  "SNC::Parameter::Metadata": {
                        "VpcId":{
                             "datasource":"ServiceNow::Pools::NetworkPool.getObjectsByLDC",
                             "datasourceFilter":{"Network":"VpcId"}
                         },
                         "SubnetId":{
                             "datasource":"ServiceNow::Pools::SubnetPool.getObjectsByNetwork",
                             "datasourceFilter":{"Network":"VpcId"}
                         }
         
                    }
            }
        
        ```

5.  Click **Submit**.

6.  After the resource block, blueprint, and catalog items are created, the cloud service user sees only the list of values of the pool data for the parameter in the catalog order form.


