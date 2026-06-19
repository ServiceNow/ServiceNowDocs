---
title: Install Vault plugins
description: Learn how to review and install the necessary plugins for ServiceNow Vault.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/servicenow-ai-platform-security/install-vault-plugins.html
release: zurich
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring ServiceNow Vault, ServiceNow Vault]
---

# Install Vault plugins

Learn how to review and install the necessary plugins for ServiceNow Vault.

## Before you begin

Role required: sn\_vault\_console.vault\_console\_admin

## About this task

ServiceNow Vault is best used with other ServiceNow security products. Install and configure the other plugins to make the most of your tools and metrics.

## Procedure

1.  Navigate to **All** &gt; **Vault** &gt; **Vault Console**.

2.  Review the status of your tools.

    |Status|Description|
    |------|-----------|
    |\[Omitted image "vault-tool-status-1.png"\] Alt text: Limited access|Tool has a limited access license. Reported metrics may be affected or unavailable.|
    |\[Omitted image "vault-tool-status-2.png"\] Alt text: Included with platform|Tool is included by default with the platform|
    |\[Omitted image "vault-tool-status-3.png"\] Alt text: Needs license|Tool has no license. Reported metrics may be affected or unavailable.|
    |\[Omitted image "vault-tool-status-4.png"\] Alt text: Premium license|Tool has full access.|

3.  If a status is either limited or needs a license, review its respective installation page, and then install or activate the tool.

<table id="table_bf1_qhb_1gc"><thead><tr><th>

Tool

</th><th>

Installation page

</th></tr></thead><tbody><tr><td>

[Data Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-discovery/data-discovery-landing.md)

</td><td>

[Activating Data Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-discovery/activate-data-discovery.md)

</td></tr><tr><td>

[Data Classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-classification/data-classification.md)

</td><td>

Included with the platform

</td></tr><tr><td>

[Data anonymization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/dps-data-anonymization.md)

</td><td>

[Activate data privacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/dps-activate-data-privacy.md)**Note:** Data anonymization is installed as part of [Data privacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/dps-data-privacy.md)

</td></tr><tr><td>

[Cloud Encryption with Key Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/cloud-encryption/dare-overview.md)

</td><td>

[Requesting Cloud Encryption for instances with Now Support Service Catalog \[KB1117369\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1117369) article in the Now Support Knowledge Base

</td></tr><tr><td>

[Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/field-encryption.md)

</td><td>

[Activate Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/activate-platform-encryption.md)

</td></tr><tr><td>

-   [Zero Trust Access \(ZTA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/session-access.md)
-   [Continuous Authentication \(CA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/ca-homepage.md)


</td><td>

-   [Activate Zero Trust Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/activate-session-access.md)
-   [Activate Continuous Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/activate-continuous-authentication.md)


</td></tr></tbody>
</table>
**Parent Topic:**[Configuring ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/configuring-servicenow-vault.md)

