---
title: Embedding Care Team Portal in Epic Hyperspace via Hyperdrive
description: Configure the Care Team Portal by embedding it into Epic Hyperspace via Hyperdrive and enabling SMART on FHIR authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/healthcare-life-sciences/healthcare-and-life-sciences/configure-care-team-portal.html
release: zurich
product: Healthcare and Life Sciences
classification: healthcare-and-life-sciences
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Care Team Portal, Healthcare Operations, Healthcare and Life Sciences]
---

# Embedding Care Team Portal in Epic Hyperspace via Hyperdrive

Configure the Care Team Portal by embedding it into Epic Hyperspace via Hyperdrive and enabling SMART on FHIR authentication.

1.  [Configure iFrame embedding for Care Team Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/healthcare-and-life-sciences/configure-iframe-portal.md)

    For the Care Team Portal to successfully launch in Hyperspace via Hyperdrive, the portal must be configured to work within an iFrame.

2.  [Enable Multi-Provider SSO for your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/healthcare-and-life-sciences/hcls-cto-enabling-oidc.md)

    Ensure that Multiple Provider SSO is enabled and configured correctly for Care Team Portal to authenticate with Epic Hyperspace via Hyperdrive.

3.  [Copy HCLS Script Includes to Global Scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/healthcare-and-life-sciences/hco-copy-script-include-global.md)

    Copy the MultiSSO\_OIDC\_CTO and OAuthUtilEpic script includes to the global scope so they are available for later configuration steps.

4.  [In Epic: Build the FHIR App to Authenticate with ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/healthcare-and-life-sciences/hco-authenticate-portal.md)

    Set up your FHIR app in Epic with the correct configurations to allow single sign-on for Epic users to access the Care Team Portal inside Epic Hyperspace via Hyperdrive.

5.  [Create and Configure an Identity Provider in ServiceNow to Authenticate with Epic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/healthcare-and-life-sciences/create-identity-provider-hco.md)

    Set up and configure an Identity Provider in your ServiceNow instance to authenticate with Epic.

6.  [In Epic: Configure Epic Hyperspace Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/healthcare-and-life-sciences/hco-configure-epic-integration.md)

    Configure the Epic integration records \(FDI, Activity, and Menu\) so that a button in Epic launches the ServiceNow Care Team Portal.

7.  [Capture Additional Data From Epic Within ServiceNow Record Producers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/healthcare-and-life-sciences/hco-update-variables-portal.md)

    Capture additional data from Epic within ServiceNow record producers by configuring variables that map to the Epic authorization token.


