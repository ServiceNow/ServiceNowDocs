---
title: Migrate to SuccessFactors spoke v4.11.0
description: Migrate from an earlier version of the SuccessFactors spoke to SuccessFactors spoke v4.11.0 by selecting the credential records that are associated with the SuccessFactors spoke v4.11.0.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/migrate-successfactors.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SuccessFactors Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Migrate to SuccessFactors spoke v4.11.0

Migrate from an earlier version of the SuccessFactors spoke to SuccessFactors spoke v4.11.0 by selecting the credential records that are associated with the SuccessFactors spoke v4.11.0.

## Before you begin

-   Perform these procedures to migrate to SuccessFactors spoke v4.11.0.
    -   [Register OAuth client application in SuccessFactors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-successfactors.md)
    -   [Upload the JKS certificate in your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-successfactors.md)
    -   [Register SuccessFactors as an OAuth provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-successfactors.md)
    -   [Create the SAML2 assertion producer record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-successfactors.md)
    -   [Create Credential record for the OData API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-successfactors.md)
    -   [Create Credential record for the SOAP API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-successfactors.md)
-   Role required: admin.

**Note:** This procedure is applicable if you are currently using an earlier version of the SuccessFactors spoke and intend to upgrade to SuccessFactors spoke v4.11.0.

If you are setting up the SuccessFactors spoke 4.11.0 for the first time, see [Set up the SuccessFactors spoke v4.x.x](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-successfactors.md).

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record, **SuccessFactors\_OData**.

3.  In the **Connections** tab, open the existing the connection record.

4.  For **Credential**, select the credential record you had created for SuccessFactors spoke v4.11.0.

    For example, `SAML_SuccessFactors_OData_Cred`.

5.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

6.  Open for the record, **SuccessFactors\_Comp\_Emp**.

7.  In the **Connections** tab, open the existing the connection record.

8.  For **Credential**, select the credential record you had created for SuccessFactors spoke v4.11.0.

    For example, `SAML_SuccessFactors_SOAP_Cred`.


