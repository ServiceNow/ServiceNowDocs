---
title: Install and configure the Vulnerability Response Integration with Palo Alto Prisma Cloud application
description: Install the Vulnerability Response Integration with Palo Alto Prisma Cloud application to use the imported data from Prisma Cloud. Use this data to prioritize and remediate misconfigurations on your assets.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Understanding the Vulnerability Response Integration with Palo Alto Prisma Cloud, Integrate, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Install and configure the Vulnerability Response Integration with Palo Alto Prisma Cloud application

Install the Vulnerability Response Integration with Palo Alto Prisma Cloud application to use the imported data from Prisma Cloud. Use this data to prioritize and remediate misconfigurations on your assets.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System Definition** &gt; **Plugins**.

2.  In the search bar, search for `Vulnerability Response Integration with Palo Alto Prisma Cloud`.

3.  Click **Install**.

    Any dependencies that will be installed are displayed.

4.  Navigate to **All** &gt; **Prisma Cloud Integration** &gt; **Administration** &gt; **Configuration** &gt; **Prisma Cloud Configuration**.

5.  On the form, fill in the fields.

<table id="table_hpn_njr_xyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Instance

</td><td>

Name of the new integration instance.You can create an instance or click the lookup icon to select an existing instance.

</td></tr><tr><td>

API URL

</td><td>

URL to integrate with the Prisma Cloud.

</td></tr><tr><td>

Access key ID

</td><td>

Unique key to authenticate the access request to the Prisma Cloud.**Note:** You must generate the key after logging in to the Prisma Cloud portal.

</td></tr><tr><td>

Secret key

</td><td>

Private key to authenticate the access request to the Prisma Cloud.**Note:** You must generate the secret key after logging in to the Prisma Cloud portal.

</td></tr></tbody>
</table>6.  Click **Save and Test**.


## What to do next

After you complete the installation, navigate to **Prisma Cloud Integration** &gt; **Configuration** to continue with the configuration.

