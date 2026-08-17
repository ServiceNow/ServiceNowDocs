---
title: Activate the HL7 FHIR Spoke
description: Install the HL7 FHIR Spoke from the ServiceNow Store and verify that the required platform plugins are active so that the eight FHIR actions are available in Workflow Studio.Bind the FHIR server URL and OAuth credentials to the shared HL7 FHIR Connection &amp; Credential Alias so that all eight spoke actions can authenticate to and read from your FHIR R4 server.Add an HL7 FHIR Spoke stream action to a flow to search a FHIR resource and process each matching record as it streams in, with pagination handled automatically by the spoke.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/fhir-spoke-activate.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 5
keywords: [activate, install, plugins, connection, credential alias, OAuth, FHIR server, data stream, pagination, Flow Designer, FHIR search]
breadcrumb: [HL7 FHIR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Activate the HL7 FHIR Spoke

Install the HL7 FHIR Spoke from the ServiceNow Store and verify that the required platform plugins are active so that the eight FHIR actions are available in Workflow Studio.

## Before you begin

Role required: admin

The following platform plugins must be active before the spoke's stream actions can be added to a flow:

-   Workflow Studio \(`com.glide.hub`\)
-   Flow Designer Action Step — CORE \(`com.glide.hub.action_step.core`\)
-   REST step type \(`com.glide.hub.action_step.rest`\)
-   Integration Hub Action Template — Data Stream \(`com.glide.hub.action_type.datastream`\)

## About this task

HL7 FHIR Spoke is distributed as a scoped application in the ServiceNow Store. After you install it, the eight FHIR actions appear in the Workflow Studio action picker under the four FHIR Integration Hub categories.

## Procedure

1.  Request the HL7 FHIR Spoke application from the ServiceNow Store and install it on your instance.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

2.  Navigate to **All** &gt; **System Definition** &gt; **Plugins** and confirm that the four required plugins listed in the prerequisites are active.

3.  In Workflow Studio, create or open a flow, add an action step, and confirm that the FHIR actions appear under the Organization Management, Location Management, Practitioner Management, and PractitionerRole Management categories.


## Result

The HL7 FHIR Spoke is installed and its actions are available to flow authors. Before the actions can read from a FHIR server, configure the connection and credentials. See [Configure the HL7 FHIR connection and credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/fhir-spoke-activate.md).

## Configure the HL7 FHIR connection and credentials

Bind the FHIR server URL and OAuth credentials to the shared `HL7 FHIR` Connection &amp; Credential Alias so that all eight spoke actions can authenticate to and read from your FHIR R4 server.

### Before you begin

Role required: admin

You need the following from your FHIR server administrator: the FHIR R4 server base URL, the OAuth authorization, token, and revoke-token endpoint URLs, and the OAuth client ID and client secret registered for your instance.

### About this task

The spoke ships a Connection &amp; Credential Alias named `HL7 FHIR` with an attached configuration template named `FHIR Connection Configuration`. The template adds a guided **Add Connection** action to the alias that creates the HTTP connection and an OAuth 2.0 credential in one step. The OAuth client credentials and the FHIR server URL ship empty — you supply them through the guided setup. All eight actions share this single alias.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases** and open the **HL7 FHIR** alias.

2.  On the alias record, click **Add Connection** to open the guided `FHIR Connection Configuration` setup form.

3.  Enter the connection details: a **Connection Name**, the **Connection URL** \(your FHIR R4 server base URL — host and protocol only, over HTTPS\), and the **API version**.

    Leave **API version** at the default `baseR4` unless your FHIR server uses a different R4 URL fragment. This value populates the `api_version` connection attribute that every action appends to the base URL.

4.  Enter the OAuth credential details supplied by your FHIR server administrator: **OAuth Name**, **OAuth Client ID**, **OAuth Client Secret**, and **OAuth Token URL**.

    The guided setup creates an OAuth 2.0 credential \(`FHIR Spoke Credential`\) and application registry \(`FHIR Spoke OAuth`\) that use the authorization code grant with PKCE \(`S256`\).

5.  Save the connection, then complete the OAuth authorization to obtain an access token.

6.  Use the alias **Test Connection** action to verify that the instance can authenticate to and reach the FHIR server.


### Result

All eight HL7 FHIR Spoke actions can now authenticate to your FHIR server through the shared alias. To add a stream action to a flow, see [Add a FHIR stream action to a flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/fhir-spoke-activate.md).

## Add a FHIR stream action to a flow

Add an HL7 FHIR Spoke stream action to a flow to search a FHIR resource and process each matching record as it streams in, with pagination handled automatically by the spoke.

### Before you begin

Role required: a Workflow Studio authoring role, such as `flow_designer`.

The `HL7 FHIR` connection and credentials must be configured. See [Configure the HL7 FHIR connection and credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/fhir-spoke-activate.md).

### About this task

Stream actions use the data stream action template, which retrieves results page by page. You process the streamed items inside a "For Each" flow logic block so that the flow handles each resource without buffering the entire result set.

### Procedure

1.  In Workflow Studio, open your flow or subflow and add an action step.

2.  Search for the stream action for the resource you want — for example, **Look up Organizations Stream** — and add it to the flow.

3.  Set the required **Page size** input.

    Page size controls how many resources the spoke requests per FHIR page. The spoke continues to request pages until the FHIR server returns no `next` link.

4.  Set any optional FHIR R4 search parameters to filter the results — for example, **name** or **active**.

    For the full set of search parameters per resource, see [HL7 FHIR Spoke actions reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/fhir-spoke-actions.md).

5.  Add a **For Each** flow logic block that iterates over the action's stream output.

6.  Inside the loop, map the resource data pills into your downstream steps — for example, to create or update records in your application.

7.  After the loop, check the action's **status code**, **error code**, and **error message** outputs to detect transport failures.


