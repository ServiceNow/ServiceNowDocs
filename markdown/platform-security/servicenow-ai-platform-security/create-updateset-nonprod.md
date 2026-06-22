---
title: Prepare Circle of Trust certificates
description: Create an update set in the trusted environment to export the trusted certificate to the production environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/servicenow-ai-platform-security/create-updateset-nonprod.html
release: australia
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Code Signing, Platform Security]
---

# Prepare Circle of Trust certificates

Create an update set in the trusted environment to export the trusted certificate to the production environment.

## Before you begin

Roles required: admin, security\_admin

## Before you begin

Trusted instance

## Procedure

1.  In the trusted environment, navigate to **sys\_certificate.list**.

    \[Omitted image "sys\_cert\_list.png"\] Alt text: X.509 certificates list

2.  Open the most recently created X.509 Certificate that was generated with the type **Trust Store Cert**.

    You may need to add the **Created** field to the list to find the most recent record. See [Personal lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/c_PersonalLists.md).

3.  Select **Export certificate to production**.

    \[Omitted image "export\_cert-to-prod.png"\] Alt text: Export certificate to production button.

    A signature is created along with the certificate.

4.  Navigate to **System Update Sets** &gt; **Local Update Sets**.

5.  Find and open the code signing update.

    This update starts with the text `code_signing_key_publicsigver`.

    A new code signing update set record has been created by the previous steps. To find this record, sort the list using the **Created by** field and look for records with in the **Name** field.

6.  View the relevant Signature Records and the X.509 Certificate.

    The update set includes the attachment for the signature record along with the entry of the signature in the table and the certificate.

    \[Omitted image "nonprod-updateset.png"\] Alt text: Displays the contents of the update set.

7.  Select the **Export to XML** related link.

    \[Omitted image "export-to-xml.png"\] Alt text: Export to XML related link.

8.  Retrieve the update set in production.

    See [Retrieve an update set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/t_RetrieveAnUpdateSet.md) for details.

    **Important:** Repeat these steps for your second key pair. Remember that there’s a key for both the cm\_code\_attest and cm\_code\_signing cryptographic modules.


