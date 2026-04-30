---
title: Preparing for installing the Vulnerability Response Integration with Palo Alto Prisma Cloud
description: Prepare for installing the Vulnerability Response Integration with Palo Alto Prisma Cloud by performing setup tasks.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Palo Alto Prisma Cloud, Integrate, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Preparing for installing the Vulnerability Response Integration with Palo Alto Prisma Cloud

Prepare for installing the Vulnerability Response Integration with Palo Alto Prisma Cloud by performing setup tasks.

## Before you begin

To integrate Vulnerability Response with Palo Alto Prisma Cloud, you must be assigned a permission group in Prisma that provides read-only access to Policy and Alerts data. You can find more information on permission groups at [Prisma Cloud Administrator Roles](https://docs.prismacloud.io/en/classic/cspm-admin-guide/manage-prisma-cloud-administrators/prisma-cloud-administrator-roles#id437b5c4a-3dfa-4c70-8fc7-b6d074f5dffc).

For detailed information on the roles assigned to different permission groups, refer to the page [Prisma Cloud Administrator Permissions](https://docs.prismacloud.io/en/classic/cspm-admin-guide/manage-prisma-cloud-administrators/prisma-cloud-admin-permissions).

In addition, access keys must be created to enable reading the alerts. For more information on creating access keys, see [Create and Manage Access Keys](https://docs.prismacloud.io/en/classic/cspm-admin-guide/manage-prisma-cloud-administrators/create-access-keys).

To install and configure the Vulnerability Response Integration with Palo Alto Prisma Cloud, use the following checklist. Before you install the application, verify that the items listed are completed.

<table id="table_qby_jng_tlb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Checkbox image.](../../../vulnerability-response/image/checkbox.png)

</td><td>

Verify that you have the following sets of information:-   API base URL
-   Access key ID
-   Secret key
-   Username and Password for accessing Prisma Cloud.

 These credentials are used to connect to the Prisma Cloud instance from the ServiceNow AI Platform® instance. The access key ID and secret key must be generated from the Prisma Cloud portal after registration.

</td></tr><tr><td>

![Checkbox image.](../../../vulnerability-response/image/checkbox.png)

</td><td>

If not already installed and activated, install the Vulnerability Response application before you install the Vulnerability Response Integration with Palo Alto Prisma Cloud application.For more information about installing and activating the Vulnerability Response application, see [Install Vulnerability Response](../../../vulnerability-response/task/install-and-configure-vr.md). This integration requires version 15.2.0 of Vulnerability Response or later.

</td></tr><tr><td>

![Checkbox image.](../../../vulnerability-response/image/checkbox.png)

</td><td>

If you don't already have the application on your instance, get entitlements and download the Vulnerability Response Integration with Palo Alto Prisma Cloud application to your ServiceNow AI Platform® instance.

See .

</td></tr><tr><td>

![Checkbox image.](../../../vulnerability-response/image/checkbox.png)

</td><td>

Ensure you have installed the following plugins for a smooth integration run:

-   Vulnerability Response
-   Configuration Compliance
-   Vulnerability Response Integration with Palo Alto Prisma Cloud

 The following plugins are optional but can be useful:

-   Cloud Provisioning and Governance
-   Discovery and Service Mapping Patterns

</td></tr><tr><td>

![Checkbox image.](../../../vulnerability-response/image/checkbox.png)

</td><td>

Estimate the number of test results that you expect to import.

 Verify that your instance can accept the number of test results that you expect to import. An undersized instance can lead to long load times. If you don't know the size of your instance, or if you need assistance, contact ServiceNow Technical Support.

</td></tr><tr><td>

![Checkbox image.](../../../vulnerability-response/image/checkbox.png)

</td><td>

Verify that you have an administrator to manage the integrations and to remediate the test results:The admin installs the Vulnerability Response Integration with Palo Alto Prisma Cloud application. If not assigned, the admin assigns the vulnerability admin \(sn\_vul.vulnerability\_admin\) and other roles.

</td></tr></tbody>
</table>You are ready to [Install and configure the Vulnerability Response Integration with Palo Alto Prisma Cloud application](install-and-configure-prisma-cloud.md).

