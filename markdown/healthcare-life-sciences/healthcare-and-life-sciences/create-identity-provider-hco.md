---
title: Create and Configure an Identity Provider in ServiceNow to Authenticate with Epic
description: Set up an Identity Provider in your ServiceNow instance to enable OIDC for Healthcare Operations Core.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/healthcare-and-life-sciences/create-identity-provider-hco.html
release: australia
product: Healthcare and Life Sciences
classification: healthcare-and-life-sciences
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Embed Care Team Portal in Epic, Configure, Care Team Portal, Healthcare Operations, Healthcare and Life Sciences]
---

# Create and Configure an Identity Provider in ServiceNow to Authenticate with Epic

Set up an Identity Provider in your ServiceNow instance to enable OIDC for Healthcare Operations Core.

## Before you begin

Ensure that the com.snc.integration.sso.multi.installer plugin is installed on your instance.

**Note:** For the following process to be successful, the following script includes need to be available in Global scope:

-   **MultiSSO\_OIDC\_CTO**
-   **OAuthUtilEpic**

If these script includes are in HCLS application scope, they must first be cloned into Global scope before proceeding.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

2.  Select **New**.

3.  Under What kind of SSO are you trying to create, select **OpenID Connect**.

4.  In the Import OpenID Connect Well-Known Configuration window, enter the following fields:

    -   Name – Enter a name for your Identity Provider \(for example, Epic OIDC\)
    -   Client ID – Input the Client ID created from your FHIR app on fhir.epic.com.
    -   Well-Known Configuration IRL – Enter `[https://fhir.epic.com/interconnect-fhir-oauth/api/FHIR/R4/.well-known/openid-configuration](https://fhir.epic.com/interconnect-fhir-oauth/api/FHIR/R4/.well-known/openid-configuration)`.

        **Note:** Verify this value with Epic as it may be different for your environment.

5.  Select **Import.**

6.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

7.  Select the Identity Provider you wish to configure.

8.  Set the ServiceNow Homepage value to `https://<instance-name>.service-now.com/careteam`.

9.  Navigate to the OIDC Provider Configuration related list and open the OIDC provider record.

10. Update the following fields:

    1.  User Claim – enter **preferred\_username**.
    2.  User Field – select **User ID**.
    3.  OIDC Metadata URL - Enter to your FHIR server \(Interconnect\) URL endpoint. For example, from [https://fhir.epic.com/interconnect-fhir-oauth/api/FHIR/R4/.well-known/openid-configuration](https://fhir.epic.com/interconnect-fhir-oauth/api/FHIR/R4/.well-known/openid-configuration) to [https://yourinterconnectendpoint/.well-known/openid-configuration/](https://yourinterconnectendpoint/.well-known/openid-configuration/).
11. Click **Update**.

12. In the Identity Provider, navigate to the Advanced related list.

13. Update the Single Sign-On Script field to **MultiSSO\_OIDC\_CTO**.

14. Ensure the **Active** field is set to true.

15. Click **Save**.

16. Navigate to the OIDC Entity related list.

17. Select the OIDC entity record.

18. In the OAuth API Script field, select **OAuthUtilEpic**.

19. Click **Update**.


## Result

An Identity Provider has been created and configured based on the information provided by the well-known configuration.

