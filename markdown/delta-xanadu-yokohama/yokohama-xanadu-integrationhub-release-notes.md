---
title: Combined Integration Hub release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Integration Hub from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-integrationhub-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Integration Hub release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Integration Hub from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Integration Hub release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Integration Hub to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Integration Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **Now Assist in [\[Placeholder link text to key bundle-crworkflow.conv-spokes-na\]](https://www.servicenow.com/docs/access?context=conv-spokes-na&family=xanadu&ft:locale=en-US)**

Use Now Assist in Conversational Spokes to utilize the conversational ability of Integration Hub Spoke actions. Now Assist in Conversational Spokes offers generative AI capabilities to make spoke actions conversational. With this, you can perform business actions and automate business workflows through conversational interface.

Install Now Assist for Conversational Spokes plugin and start utilizing the conversational ability of the Look up User spoke action in Microsoft Active Directory v2 spoke. You can call this action from a conversational interface like Now Assist.


-   **[Send and receive messages in an Avro format with Stream Connect](https://www.servicenow.com/docs/access?context=schema-management&family=xanadu&ft:locale=en-US)**

Import and create Avro schemas to store in the Stream Connect Schemas \[stream\_connect\_schema\] table. Stream Connect producers and consumers use the schemas to convert plain-text JSON messages into an Avro binary format and back. Using an Avro format can reduce the size of the payload and simplify your integration to your local Apache Kafka instance.

-   **[Track incoming requests for SOAP and REST APIs, and URL Export](https://www.servicenow.com/docs/access?context=integrationhub-usage-dashboard&family=xanadu&ft:locale=en-US)**

View the data egress details in the enhanced Usage dashboard. Using the dashboard, you can track the data egress usage per source over time. This information is presented in a line chart and, if needed, you can view the amount of data transfer by source on any given date within the specified date range. The dashboard retrieves data from the Data Egress Count table \[data\_egress\_count\].

-   **[Enable parallel loading in custom \(load by script\) type data sources](https://www.servicenow.com/docs/access?context=custom-type-data-source&family=xanadu&ft:locale=en-US)**

Use a script to partition data into smaller sections, then load the sections in parallel. Parallel loading can enable your integrations to finish faster and reduce the impact on other tasks.

-   **[CyberArk credential storage integration](https://www.servicenow.com/docs/access?context=c_CyberArkCredStorageIntegrate&family=xanadu&ft:locale=en-US) Use the CyberArk Digital Vault to store and access your OAuth 2.0 credentials**

Use the ServiceNow® MID Server to access your OAuth 2.0 credentials stored on the CyberArk Digital Vault. The MID Server uses this information to generate OAuth 2.0 tokens for client credentials grant type that are then used to make REST API calls to the third-party server.

-   **[Make outbound REST and SOAP calls through a MID Server using mTLS](https://www.servicenow.com/docs/access?context=mtls-mid-server&family=xanadu&ft:locale=en-US)**

Store mTLS password and certificate information on the instance, in a vault, or in a configuration file. The MID Server uses this information to make outbound REST and SOAP calls with the mTLS protocol.

-   **[Use the Personal Authentication dashboard](https://www.servicenow.com/docs/access?context=personal-auth-dashboard&family=xanadu&ft:locale=en-US)**

Use your personal credentials to connect to third-party integrations. View, authenticate, revoke, and renew your personal authentications through a simplified, consolidated interface.

-   **[Enhancements to the external trigger endpoints](https://www.servicenow.com/docs/access?context=generate-endpt-oauth2&family=xanadu&ft:locale=en-US)**

Generate an endpoint for webhooks in the third-party applications that support [OAuth 2.0 authentication](https://www.servicenow.com/docs/access?context=generate-endpt-oauth2&family=xanadu&ft:locale=en-US). The endpoint enables webhooks to connect with your ServiceNow instance.

Generate the endpoints by updating the base system external event sources on your ServiceNow instance. After that, you can configure the endpoint on the third-party application and enable it to send a webhook to the ServiceNow instance to execute a flow. Based on the authentication type that the third-party system supports, you can generate a hash, secret, or token, or add roles or a user to the external event source. Finally, you generate the endpoint that you can use on the third-party system webhook.

-   **[Automatically generate a JSON payload for the JSON Builder step](https://www.servicenow.com/docs/access?context=json-build-step-action-designer&family=xanadu&ft:locale=en-US)**

Enter a JSON payload into the step's script editor to automatically de-serialize the payload into structured input.

-   **[Enhanced OpenAPI step](https://www.servicenow.com/docs/access?context=open-api-step-action-designer&family=xanadu&ft:locale=en-US)**

Choose to import an OpenAPI specification or a Postman Collection of a third-party outbound REST web service for building an integration. The OpenAPI step is now enhanced to support Postman API collections and is renamed as **OpenAPI/Postman step**.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Stream Connect for Apache Kafka alerting](https://www.servicenow.com/docs/access?context=stream-connect-alert&family=yokohama&ft:locale=en-US)**
    -   Get alerts for your Stream Connect integrations. Stream Connect uses both active and scheduled monitoring to detect events across multiple Stream Connect components. If an issue is detected, an alert is created, and a message is logged to the Stream Connect Log.
    -   Specify alert thresholds by configuring alerting properties. For example, you can specify a maximum amount of time to process the current message queue. If the estimated processing time exceeds your specified time, an alert is generated.
    -   Receive alert notifications via email, SMS, or the ServiceNow® mobile app. Notifications contain detailed alert information, including the alert number, level, and a description. You can configure notification settings based on alert types, severity, and user preferences.
-   **[View producer statistics in the Stream Connect dashboard](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&family=yokohama&ft:locale=en-US)**

Get detailed information about Stream Connect producers and their performance, including a producer’s status and type, the number of bytes and messages produced to a topic, and producer data trends over time, in the Stream Connect dashboard.

-   **[Check data usage in the Stream Connect dashboard](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&family=yokohama&ft:locale=en-US)**

View total data usage and data usage per month and topic with the Stream Connect dashboard. Data usage history is available for the last 12 complete months plus the current month.

-   **[Use error evaluation with Data Stream actions](https://www.servicenow.com/docs/access?context=data-stream-actions&family=yokohama&ft:locale=en-US)**

Catch step errors and specify error behavior for each step in a Data Stream action. Create your own error conditions by specifying when an action returns an error state and the status codes and messages they return.

-   **[View connection aliases in integration actions](https://www.servicenow.com/docs/access?context=managing-connections-integration-hub&family=yokohama&ft:locale=en-US)**

Edit, configure, and create connection aliases in the Action Properties section of actions in ServiceNow® Workflow Studio. View connection error details for connection aliases that are not set up or configured.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Integration Hub features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[External Triggers framework to use new features provided by Platform Security](https://www.servicenow.com/docs/access?context=set-up-external-webhook-endpoints&family=xanadu&ft:locale=en-US)**

Upgrade the existing external triggers framework to use new features like Hash-based and Token-based authentication profiles with access policies.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Integration Hub features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   The Legacy Usage Overview dashboard is deprecated. This feature is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Yokohama

</td><td>

**Important:** Starting with the Yokohama release, Microsoft Teams Spoke is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Microsoft Teams Graph Spoke provides the latest experience for this functionality.

For more information, search for the term `Microsoft Teams Spoke for ServiceNow IntegrationHub` in [Plugins planned for deprecation](https://www.servicenow.com/docs/access?context=plugins-planned-for-deprecation&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Integration Hub features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Integration Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/products/automation-engine.html](https://www.servicenow.com/products/automation-engine.html).

</td></tr><tr><td>

Yokohama

</td><td>

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Integration Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Integration Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Integration Hub, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Integration Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Integration Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Send and receive messages in an Apache Avro format with ServiceNow® Stream Connect.
-   Use the CyberArk Digital Vault to store and access your OAuth 2.0 credentials.
-   Use your personal credentials to connect to third-party integrations.

 See [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Get alerts and alert notifications for your Stream Connect integrations.
-   Use error evaluation with Data Stream actions to catch step errors and specify error behavior for each step.
-   Edit, configure, and create connection aliases in the Action Properties section of actions in Workflow Studio.

 See [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

