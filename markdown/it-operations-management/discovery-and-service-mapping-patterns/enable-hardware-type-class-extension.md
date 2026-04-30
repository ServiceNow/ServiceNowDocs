---
title: Enable the Cloud Hardware Type class extension
description: Enable the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table to store the predefined virtual machine \(VM\) hardware type records for Amazon AWS Cloud Microsoft Azure Cloud and Google Cloud Platform \(GCP\). This class extension helps prevent duplication of the VM hardware type records in the Hardware Type \[cmdb\_ci\_compute\_template\] table, which improves performance for Discovery and related flows.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Enable the Cloud Hardware Type class extension

Enable the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table to store the predefined virtual machine \(VM\) hardware type records for Amazon AWS Cloud Microsoft Azure Cloud and Google Cloud Platform \(GCP\). This class extension helps prevent duplication of the VM hardware type records in the Hardware Type \[cmdb\_ci\_compute\_template\] table, which improves performance for Discovery and related flows.

## Before you begin

-   Veirfy that the latest versions of the following applications are installed:
    -   CMDB CI Class Models
    -   Discovery and Service Mapping Patterns

        If the version of Discovery and Service Mapping Patterns is earlier than 1.6.0, see the Knowledge Base article [KB0955939](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0955939).

-   Ensure that the application scope is the Discovery and Service Mapping Patterns application.

Role required: admin

## About this task

Each cloud service provider offers several predefined VM hardware types, such as t1.micro \(AWS\), and so on. You can also create your own. By default, Discovery stores the discovered VM hardware types in the Hardware Type \[cmdb\_ci\_compute\_template\] table. This table is a "child" of the cmdb\_ci\_logical\_datacenter class, so the attributes in the Hardware Type table includes the attributes in the cmdb\_ci\_logical\_datacenter class.

This model might create duplicate records for each discovered VM hardware type:

The count of records for each discovered VM hardware type is determined by the number of service accounts multipled by the Number of logical datacenters.

For example, let's assume an organization has an AWS account of t1.micro VM. The organization has 3000 service accounts and 10 Logical Data Centers \(LDCs\), such as West US. Your next discovery can detect the VM hardware type and create 30,000 records in the Hardware Type \[cmdb\_ci\_compute\_template\] table.

This approach could slow down your discovery and related flows.

Avoid these issues by storing the predefined AWS and GCP VM hardware types in the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table.

This table extends the Hardware Type \[cmdb\_ci\_compute\_template\] table. Because it's not tied to any LDC or service account, Discovery avoids adding many VM hardware type records to the Hardware Type \[cmdb\_ci\_compute\_template\] table.

The Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table uses the object\_id and the provider fields in the identification rule.

**Note:** In AWS environments, the discovery pattern discovers hardware types only to the master account’s datacenter. It then creates relationships of the discovered hardware types to the corresponding regions in member accounts.

-   If a discovery schedule is run for both a master account and member accounts, the pattern discovers only the master account’s datacenter hardware type.
-   If a discovery schedule is run for a standalone member account, the pattern discovers that member account’s datacenter and its hardware type.
-   If a discovery schedule is run for a master account after a standalone member account has already been discovered, the pattern doesn’t rediscover the hardware type for the member account. Instead, it discovers the hardware type for the master account and maps the relationships between the master and member accounts.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** field, search for `sn_itom_pattern.use a single hardware type for cloud data centers`.

3.  Select the **sn\_itom\_pattern.use a single hardware type for cloud data centers** property.

4.  In the **Value** field, enter `true`.

5.  Select **Update**.


## What to do next

1.  Clean up the Hardware Type records. For more information, see the Knowledge Base article [KB1285337](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1285337).

    **Important:** The cleanup removes all the existing compute profiles from the CMDB. Therefore, if you have manually added a hardware template to the Hardware Type \[cmdb\_ci\_compute\_template\] table, you must manually add it to the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table.

2.  Rerun the Cloud Discovery.

**Parent Topic:**[Discovery patterns used by ITOM Visibility](../../service-mapping/concept/c_MappingPatternsCustomization.md)

**Previous topic:**[Activate a disabled pattern](../../service-mapping/task/activate-disabled-pattern.md)

**Next topic:**[Improved query performance with direct field population in CI tables](../../service-mapping/concept/query-service-account-ldc-fields.md)

**Related topics**  


[Amazon AWS Cloud components discovery using patterns](../reference/data-discovered-aws-patterns.md)

[Google Cloud Platform \(GCP\) Cloud components discovery using Patterns](../../service-mapping/reference/gcp-cloud-discovery-patterns.md)

[Microsoft Azure Cloud components discovery using patterns](../../service-mapping/reference/azure-cloud-discovery-patterns.md)

