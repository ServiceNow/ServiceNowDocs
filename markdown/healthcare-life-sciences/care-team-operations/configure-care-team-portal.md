---
title: Embedding Care Team Portal in Epic Hyperspace via Hyperdrive
description: Configure the Care Team Portal by embedding it into Epic Hyperspace via Hyperdrive and enabling SMART on FHIR authentication.
locale: en-US
release: australia
product: Care Team Operations
classification: care-team-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Embedding Care Team Portal in Epic Hyperspace via Hyperdrive

Configure the Care Team Portal by embedding it into Epic Hyperspace via Hyperdrive and enabling SMART on FHIR authentication.

1.  [Update variables in record producers to capture tokenized data from Epic Hyperspace](../task/hco-update-variables-portal.md)

    Update the variable values in existing record producers to capture tokenized data from Epic.

2.  [Configure iFrame embedding for Care Team Portal](../task/configure-iframe-portal.md)

    For the Care Team Portal to successfully launch in Hyperspace via Hyperdrive, the portal must be configured to work within an iFrame.

3.  [Enable Multi-Provider SSO for your ServiceNow instance](../task/hcls-cto-enabling-oidc.md)

    Ensure that Multiple Provider SSO is enabled and configured correctly for Care Team Portal to authenticate with Epic Hyperspace via Hyperdrive.

4.  [Authenticate SMART on FHIR for use with the Care Team Portal in Hyperspace via Hyperdrive](../task/hco-authenticate-portal.md)

    Set up your FHIR app with the correct configurations to allow single sign-on for EPIC users to access the Care Team Portal inside EPIC Hyperspace via Hyperdrive.

5.  [Create an Identity Provider on your ServiceNow instance for Healthcare Operations Core](../task/create-identity-provider-hco.md)

    Set up an Identity Provider in your ServiceNow instance to enable OIDC for Healthcare Operations Core.

6.  [Configure your Identity Provider for Care Team Portal](../task/configure-identity-provider-hco.md)

    Configure your Identity Provider to ensure successful user authentication in Care Team Portal.

7.  [Configure the integration settings in the Hyperdrive Client Test Harness for Care Team Portal](../task/configure-hyperspace-hco.md)

    Once the Care Team Portal is configured, create a launch URL that can then be configured inside the Epic Hyperdrive Client Test Harness for testing.


