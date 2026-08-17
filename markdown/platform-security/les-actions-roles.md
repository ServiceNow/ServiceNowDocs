---
title: Log Export Service actions and required roles
description: Reference table of Log Export Service \(LES\) actions, their descriptions, and the roles required to perform them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/les-actions-roles.html
release: australia
topic_type: reference
last_updated: "2026-07-21"
reading_time_minutes: 3
keywords: [log export service, LES, roles, permissions, actions, reference]
breadcrumb: [Reference, Log Export Service \(LES\), Platform Security]
---

# Log Export Service actions and required roles

Reference table of Log Export Service \(LES\) actions, their descriptions, and the roles required to perform them.

## Role-based access control

Log Export Service \(LES\) uses role-based access control so that only authorized users can perform specific actions. The following table maps LES actions to the roles required to perform them.

Unless otherwise noted, any one of the listed roles is sufficient to perform the action.

## LES roles

LES includes the following three primary roles:

-   **sn\_logstoanalytics.admin**

    Application administrator role. Installed with the LES application and allows a non-admin user to configure and use LES.

-   **admin**

    System administrator role. Required to install the LES store application and to perform platform-level setup tasks.

-   **hermes\_admin**

    Required to generate the certificates that secure the connection between LES and the Hermes Messaging Service.


|Action|Description|Required roles|Component|
|------|-----------|--------------|---------|
|Initial setup and configuration|
|Install Log Export Service application|Install LES from the ServiceNow Store.|admin|Instance|
|Review Hermes Messaging Service diagnostics|Verify that the Hermes Messaging Service is up and running, check connectivity, and view topics.|admin|Instance|
|Run Kafka consumer guided setup|Step through the initial configuration of LES for an external Kafka consumer.|admin|Instance|
|Run MID Server consumer guided setup|Step through the initial configuration of LES for a dedicated MID Server consumer.|admin|Instance|
|Log source configuration|
|Create a log source configuration|Regulate and set filters on the logs to be forwarded by creating a source record for each log source.|admin, sn\_logstoanalytics.admin|Instance|
|Create source type and multiple topics|Consume logs for each source type by creating multiple Kafka topics.|admin, sn\_logstoanalytics.admin|Instance|
|Validate Log Producer|View live log records in a topic by using the Hermes Topic Inspector.|admin, sn\_logstoanalytics.admin|Instance|
|Kafka consumer configuration|
|Generate certificates for Hermes secure connection|Generate the certificates required to authorize a client that pulls logs from the Hermes Messaging Service.|admin, hermes\_admin|Instance|
|Configure Kafka consumer processes|Create consumer processes with separate bootstrap addresses to connect to both Hermes Kafka clusters for failover.|admin|External Kafka|
|Verify Kafka consumer pulling logs|Verify that the chosen Kafka consumer can pull log events from the Hermes Messaging Service.|admin|External Kafka|
|MID Server consumer configuration|
|Install and validate dedicated MID Server|Install a MID Server dedicated to LES, and validate it to enable it to execute automation tasks.|admin|MID Server|
|Add MID Server properties for Hermes|Configure properties that establish the Kafka connection between the MID Server and the Hermes Messaging Service.|admin|MID Server|
|Configure Log REST push destination|Create a Destination Configuration record that defines the REST endpoint that the MID Server Extension forwards logs to.|admin, sn\_logstoanalytics.admin|Instance|
|Configure LES Consumer Context|Update the LES Consumer MID Server Extension record to execute on the dedicated MID Server installed for LES.|admin|Instance|
|Configure Consumer|Create a Consumer record specifying the Hermes topic to retrieve logs from and the destination configuration to relay them to.|admin, sn\_logstoanalytics.admin|Instance|
|Test MID Connection|Verify connectivity from the MID Server environment to the Hermes cluster.|admin, sn\_logstoanalytics.admin|Both|
|Verify MID Server integration|Monitor the Consumer Status view to confirm the MID Server process is relaying messages to the REST endpoint.|admin, sn\_logstoanalytics.admin|Instance|
|Administration and monitoring|
|Update the glide.les.disable\_logs\_forwarding system property|Pause or resume LES log forwarding during migration or database reseeding operations.|admin|Instance|
|Review log report dashboard|Analyze the size of each data log and consumption metrics across LES sources.|admin, sn\_logstoanalytics.admin|Instance|

**Parent Topic:**[Log Export Service \(LES\) references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/les-references.md)

**Related topics**  


[Log Export Service roles]()

