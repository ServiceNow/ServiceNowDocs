---
title: Create a CI class for a virtual cloud resource
description: If the base system does not provide a CI type for cloud-based virtual resources, you can create a CI class based on the virtual machine object class.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Add a product to an existing provider in CAPI, Cloud API \(CAPI\), Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create a CI class for a virtual cloud resource

If the base system does not provide a CI type for cloud-based virtual resources, you can create a CI class based on the virtual machine object class.

## Before you begin

Role required: admin

## About this task

This topic provides general instructions for extending an existing cloud provider, product, and resource type.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Click **Open Hierarchy**.

    ![Open the CI hierarchy](../image/cl-class-manager-open.png)

3.  On the **CI Classes** pane, enter `Virtual Machine Object` in the search field, and then select **Virtual Machine Object**.

    ![The virtual machine object class](../image/virtual-machine-object.png)

4.  Click the **Virtual Machine Object** link.

    ![Click Virtual Machine Object](../image/virtual-machine-object-select.png)

5.  Click **Add Child Class**.

6.  In the **Provide Basic Info** step that appears, enter a name and a description.

    When you move the focus of the cursor away from the **Display Name** field, the **Table Name** field automatically populates with the same name in lower case. For a table in a scoped application, the name is prefixed with a namespace identifier to indicate that it is part of an application. For a table in the global application, the name is prefixed with the string **u\_cmdb\_ci**. You cannot modify the prefix; however, you can modify the rest of the table name. The name can contain only lowercase alphanumeric ASCII characters and underscores \(\_\). The maximum string length is 80 characters.

7.  Click **Next**.

8.  On the **Add Attributes** step, click **Derived**, and then review the attributes that are inherited from the Virtual Machine Object class.

    Most attributes that you need are provided.

9.  To add an attribute:

    1.  Double-click the **Insert a new row** text in the **Column label** field.

    2.  Enter a name for the column and then click the green arrow.

    3.  Fill out the rest of the fields in the row.

        See [Dictionary entry form](https://www.servicenow.com/docs/access?context=r_DictionaryEntryForm&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for a description of all the fields.

10. Click **Next**.

11. On the **Set Identification Rule** step, create an identification rule that specifies a unique Object ID, which is required for identification.

    **Important:** Cloud Provisioning and Governance depends on the Object ID to uniquely identify an instance of the CI Class Type.

    1.  Click **Replace** on the default rule under **Identification Rule**.

    2.  Enter a name for the rule and select the **Dependent** option.

    3.  Click **Save**.

    4.  Under **Identifier Entries**, click **Add**.

    5.  Move **Object ID** from the **Available** column to the **Selected** column.

    6.  Click **Save**.

12. Click **Next**.

13. On the **Add Dependent Relationships** step, click **Override Dependencies**.

14. Configure the relationship between this virtual resource and the logical datacenter on which it resides:

    |Field|Value|
    |-----|-----|
    |Rule Type|**Hosting**|
    |Relationship|**Hosted on \(Hosted on::Hosts\)**|
    |Target Class|**Logical Datacenter**|

    ![A Hosted on:Hosts relationship](../image/relationship-rule-new-class.png)

15. Click **Save**.

16. Click **Next**.

17. Click **Next** again to skip the **Add Reconciliation Rules** step, and then click **Done** to skip the **Add Suggested Relationships** step.


## What to do next

Use the CI class in a resource type for a cloud provider. See [Add a product to an existing provider in CAPI](create-provider.md) for instructions.

Your response processor, which is part of the resource block, must also specify the necessary CI class types so it can update the CMDB. Usually, the response processor needs the object ID, the specific datacenter, and the cloud service account. See [Virtual server response processor example](../reference/response-processor-example.md) for example response processor code that uses CI classes.

**Parent Topic:**[Cloud Provisioning and Governance](../concept/cloud-management-v2-landing-page.md)

