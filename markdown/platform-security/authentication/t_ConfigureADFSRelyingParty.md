---
title: Configure an ADFS relying party
description: Take the instance metadata and import it into your ADFS server. However, manual configuration of the relying party appears to be easier to implement.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ADFS integration with SAML 2.0, Integrating SAML 2.0 with other features, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Configure an ADFS relying party

Take the instance metadata and import it into your ADFS server. However, manual configuration of the relying party appears to be easier to implement.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers** &gt; **SAML2 Update1** &gt; **Encryption And Signing** and verify that the SAML property Sign AuthnRequest \(**glide.authenticate.sso.saml2.require\_signed\_authnrequest**\) is not active.

    Only keep this property active if your ADFS administrator can verify that you require signed requests.

2.  Copy the metadata that you generated through the SAML 2 metadata link and save it to a file.

3.  Log into the ADFS server and open the management console.

4.  Select **Relying Party Trusts**.

5.  Select **Add Relying Party Trust** from the top right corner of the window.

    The add wizard appears.

6.  Click **Start** to begin.

7.  Use the **Import File** option to import the metadata file.

8.  Give it a display name such as `ServiceNow` and enter any notes you want.

9.  Select **ADFS 3.0 Profile**.

10. Do not select a token encryption certificate.

    It will use the certificate that is defined on the service that has already been exported. Defining a certificate prevents proper communication with the instance.

11. Do not enable any settings on the **Configure URL**.

12. Enter the instance site to which you connected as the Relying Party trust identifier.

    In this case, use `https://company.service-now.com` and click **Add**.

13. Permit all users to access this relying party.

14. Click **Next** and clear the **Open the Claims when this finishes** check box.

15. Close this page.

    The new relying party trust appears in the window.

16. Right-click on the relying party trust and select **Properties**.

17. Browse to the **Advanced** tab and set the **Secure hash algorithm** as either SHA-256 or SHA-1.

18. Browse to the Endpoints tab and add a **SAML Assertion Consumer** with a **Post** binding and a URL of `https://company.service-now.com/navpage.do`.


