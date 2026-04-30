---
title: REST API reference
description: Use REST interfaces to access data on your instance.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 15
breadcrumb: [API reference, API implementation and reference]
---

# REST API reference

Use REST interfaces to access data on your instance.

-   **[Account API](../../../integrate/inbound-rest/concept/account-api.md#)**  
The Account API provides endpoints to retrieve Customer Service Management \(CSM\) account records.
-   **[ActivitySubscriptions API](../../../integrate/inbound-rest/concept/actsub-api.md#)**  
The ActivitySubscriptions API provides endpoints to retrieve Activity entities from the Subscriptions and Activity Feed Framework.
-   **[Agent Client Collector API](../../../integrate/inbound-rest/concept/agnt_clnt_cll-api.md#)**  
The Agent Client Collector API provides endpoints to manage actions on available agents and managing policies.
-   **[Agent Mapping API](../../../integrate/inbound-rest/concept/agent-mapping-api.md#)**  
The Agent Mapping API provides an endpoint to map external agent IDs from Contact Center as a Service \(CCaaS\) systems to internal agent IDs in the ServiceNow AI Platform.
-   **[Aggregate API](../../../integrate/inbound-rest/concept/c_AggregateAPI.md#)**  
The Aggregate API provides endpoints that allow you to compute aggregate statistics about existing table and column data.
-   **[AI Assets API](../../../integrate/inbound-rest/concept/ai-assets-api.md#)**  
AI Assets API provides endpoints to retrieve, update, and create several types of AI assets, such as systems, data sets, prompts, and models.
-   **[AI Search External User Mapping API](../../../integrate/inbound-rest/concept/ext-user-mapping-api.md#)**  
The AI Search External User Mapping API provides endpoints that enable ingestion of user mapping information from external sources into the ServiceNow® AI Search application's index.
-   **[Alarm Management Open API](../../../integrate/inbound-rest/concept/alarm-open-api.md#)**  
The Alarm Management Open API provides endpoints to create, update, and retrieve data from the Events \[em\_event\] and Alert \[em\_alert\] tables.
-   **[AP Invoice API](../../../integrate/inbound-rest/concept/ap-invoice-api.md#)**  
Allows external systems, such as those used by vendors, to securely submit invoices directly into an accounts payable system in a structured and automated manner.
-   **[Application Service API](../../../integrate/inbound-rest/concept/application-service-api.md#)**  
The Application Service API provides endpoints that enable you to create, modify, and update application services.
-   **[Appointment API](../../../integrate/inbound-rest/concept/appointment-api.md#)**  
The Appointment API provides endpoints for interacting with the appointment booking application. Use this API to book and reschedule appointments, check available appointment slots, and fetch appointment booking configuration details.
-   **[Appointment Open API](../../../integrate/inbound-rest/concept/appointment-open-api.md#)**  
The Appointment Open API is a telecommunication API that allows you to interact with the appointment booking application. Use this API to book appointments and search available time slots.
-   **[Attachment API](../../../integrate/inbound-rest/concept/c_AttachmentAPI.md#)**  
The Attachment API provides endpoints that allow you to upload and query file attachments.
-   **[Automation Center API](../../../integrate/inbound-rest/concept/auto-api.md#)**  
The Automation Center API provides endpoints to create and update data related to robots, processes, and execution jobs. By leveraging this API, you can integrate and reflect details from your automation workflows into the Automation Center dashboard.
-   **[AWA Agent API](../../../integrate/inbound-rest/concept/agent-api.md#)**  
The AWA \(Advanced Work Assignment\) Agent API provides endpoints to manage agent presence, channel availability, and workload.
-   **[AWA Agent Consult API](../../../integrate/inbound-rest/concept/awa-agent-consult-api.md#)**  
Handles agent consult work items.
-   **[AWA Inbox Actions API](../../../integrate/inbound-rest/concept/awa-inbox-actions-api.md#)**  
The AWA Inbox Actions API provides endpoints to accept or reject a work item on behalf of an agent. This API also retrieves reject reasons for rejected work items.
-   **[AWA Manual Assignment API](../../../integrate/inbound-rest/concept/awa_manual_assign-api.md#)**  
The AWA Manual Assignment API provides an endpoint to manually assign available work items to available Advanced Work Assignment \(AWA\) agents.
-   **[AWA Offer Work API](../../../integrate/inbound-rest/concept/awa-offer-work-api.md#)**  
The AWA Offer Work API provides an endpoint to assign or transfer work items to agents.
-   **[AWA Routing API](../../../integrate/inbound-rest/concept/queue-api.md#)**  
The AWA Routing API provides endpoints to route a document to a queue.
-   **[Batch API](../../../integrate/inbound-rest/concept/batch-api.md#)**  
The Batch API provides endpoints to send a single request containing multiple REST API calls, and returns a stream of response payloads.
-   **[Case API](../../../integrate/inbound-rest/concept/case-api.md#)**  
The Case API provides endpoints that enable you to retrieve and update Customer Service Management \(CSM\) case records.
-   **[CCCIF Media Resource API](../../../integrate/inbound-rest/concept/cccif-api.md#)**  
The Custom Chat Chatbot Interoperability Framework \(CCCIF\) Media Resource API provides endpoints that enable a primary bot to upload attachments to the associated ServiceNow instance.
-   **[CdmApplicationsApi](../../../integrate/inbound-rest/concept/applications-api.md#)**  
The CdmApplicationsApi provides endpoints that enable you to `uploadzoominsoftware.io/utah-devops/`configuration data to the component, collection, deployable, and component variable folders found in the DevOps Config Workspace UI. It also has endpoints that enable you to export deployable configuration data to your DevOps pipeline and manage shared components and shared applications.
-   **[CdmChangesetsApi](../../../integrate/inbound-rest/concept/changesets-api.md#)**  
The CdmChangesetsApi provides endpoints that enable you to manage changesets.
-   **[CdmEditorApi](../../../integrate/inbound-rest/concept/editor-api.md#)**  
The CdmEditorApi provides endpoints that enable you to create nodes, update nodes, include existing nodes under other nodes, delete nodes, and retrieve nodes and node includes.
-   **[CdmPoliciesApi](../../../integrate/inbound-rest/concept/policies-api.md#)**  
The CdmPoliciesApi provides endpoints that enable you to manage policy mappings of deployables in Configuration Data Management \(CDM\). Policies that are properly mapped to a deployable are executed when a snapshot of the deployable is validated.
-   **[CdmSharedLibraryApi](../../../integrate/inbound-rest/concept/shared_libraries-api.md#)**  
The CdmSharedLibraryApi provides endpoints that enable you to create and manage shared libraries and shared components. It also has endpoints that enable you to upload and export the configuration data of a shared component.
-   **[CdmSnapshotApi](../../../integrate/inbound-rest/concept/snapshot-api.md#)**  
The CdmSnapshotApi provides endpoints that enable you to publish, unpublish, and re-validate snapshots in Configuration Data Management \(CDM\).
-   **[CdmVersionApi](../../../integrate/inbound-rest/concept/versions-api.md#)**  
The CdmVersionApi provides endpoints that enable you to publish, unpublish, and export versions \(snapshots\) in Configuration Data Management \(CDM\) for shared components under shared libraries.
-   **[Change Management API](../../../integrate/inbound-rest/concept/change-management-api.md#)**  
The Change Management API provides endpoints that enable third-party application integration with the ServiceNow Change Management process.
-   **[CI Lifecycle Management API](../../../integrate/inbound-rest/concept/ci-lifecycle-management-api.md#)**  
The CI Lifecycle Management API provides endpoints to manipulate configuration item \(CI\) operational states and apply CI actions.
-   **[Cloud Runner Test Generation REST API](../../../integrate/inbound-rest/concept/cloudrunner-testgeneration-api.md#)**  
Manages test job generation to be executed in a cloud runner for Automated Test Framework \(ATF\).
-   **[Cloud Runner Test Runner REST API](../../../integrate/inbound-rest/concept/cloudrunner-testrunner-api.md#)**  
Manages tests to be executed in a cloud runner for Automated Test Framework \(ATF\).
-   **[Cloud Runner Test User REST API](../../../integrate/inbound-rest/concept/cloudrunner-testuser-api.md#)**  
Manages test user jobs to be executed in a cloud runner for Automated Test Framework \(ATF\).
-   **[Cloud Services Catalog API](../../../integrate/inbound-rest/concept/cs-catalog-api.md#)**  
The Cloud Services Catalog API provides methods related to Day-1 \(provisioning\) and Day-2 \(modification\) operations available in the Cloud Services Catalog, such as creating cloud service stacks and calling resource operation requests. You can also retrieve information about catalog requests, stacks getting status, and other information.
-   **[CMDB Data Ingestion API](../../../integrate/inbound-rest/concept/cmdb-ingest-api.md#)**  
The CMDB Data Ingestion API provides endpoints that enable the batch ingestion of an array of objects into an Import Set table.
-   **[CMDB Instance API](../../../integrate/inbound-rest/concept/cmdb-instance-api.md#)**  
The CMDB Instance API provides endpoints to create, read, update, and delete operations on existing Configuration Management Database \(CMDB\) tables. You can only insert, update, or delete one record at a time.
-   **[CMDB Meta API](../../../integrate/inbound-rest/concept/cmdb-meta-api.md#)**  
The CMDB Meta API provides endpoints to obtain meta data on a Configuration Management Database \(CMDB\) class.
-   **[Consumer API](../../../integrate/inbound-rest/concept/consumer-api.md#)**  
The Consumer API provides endpoints to retrieve and update Customer Service Management \(CSM\) consumer records.
-   **[Contact API](../../../integrate/inbound-rest/concept/contact-api.md#)**  
The Contact API provides endpoints that enable you to retrieve and update Customer Service Management \(CSM\) contact records.
-   **[Continuous Integration/Continuous Delivery \(CICD\) API](../../../integrate/inbound-rest/concept/cicd-api.md#)**  
The CICD API provides endpoints that enable integration with common DevOps tools for building pipelines. These tools include Jenkins, Azure Pipelines, GitLab, GitHub Actions, Atlassian Bamboo/Pipelines, and more.
-   **[Continuous Integration and Continuous Delivery \(CICD\) Update Set API](../../../integrate/inbound-rest/concept/cicd-update-set-api.md#)**  
The CICD Update Set API provides methods to create, retrieve, preview, commit, and back-out an update set.
-   **[Conversation Member API](../../../integrate/inbound-rest/concept/conversation-member-api.md#)**  
The Conversation Member API provides methods for changing a specific agent’s member state to removed or updated in a given Agent Chat conversation.
-   **[CSM Attachment API](../../../integrate/inbound-rest/concept/attachment_csm-api.md#)**  
The CSM Attachment API provides endpoints that allow both internal and external users to upload, download, and remove attachments associated with a table and to retrieve attachment metadata.
-   **[CSM Pricing API](../../../integrate/inbound-rest/concept/csm-pricing-api.md#)**  
The CSM Pricing API provides methods to calculate prices for transaction lines containing products.
-   **[CTI API](../../../integrate/inbound-rest/concept/cti-api.md#)**  
The CTI API provides endpoints that enable Computer Telephony Integration \(CTI\) providers to interact with the Cloud Call Center framework.
-   **[Customer Central API](../../../integrate/inbound-rest/concept/cust_central-api.md#)**  
The Customer Central API provides endpoints to access customer information and configuration details.
-   **[Data Classification API](../../../integrate/inbound-rest/concept/data-classification-api.md#)**  
The Data Classification API provides endpoints to group data by type.
-   **[DCIM Metric Data Feed API](../../../integrate/inbound-rest/concept/dcim-metric-data-feed-api.md#)**  
The DCIM Metric Data Feed API provides an endpoint to accept Data Center Infrastructure Management \(DCIM\) metric data from an external system and store the data in a MetricBase database.
-   **[DevOps API](../../../integrate/inbound-rest/concept/devops-api.md#)**  
The DevOps API provides endpoints that enable the interaction with external DevOps tools.
-   **[DevOps Config API](../../../integrate/inbound-rest/concept/devops-config-api.md#)**  
The DevOps Config API provides endpoints to manage your applications.
-   **[Digital Product Release API](../../../integrate/inbound-rest/concept/digital-product-release-api.md#)**  
The Digital Product Release API provides endpoints to manage releases and policy compliance.
-   **[Email API](../../../integrate/inbound-rest/concept/email-api.md#)**  
The Email API provides endpoints that enable you to receive and send email messages using REST.
-   **[Entitlement API](../../../integrate/inbound-rest/concept/entitlement-api.md#)**  
The Entitlement API provides endpoints to create and retrieve entitlement records from an instance.
-   **[Event Management Topic Open API](../../../integrate/inbound-rest/concept/event_management_topic-api.md#)**  
The Event Management Topic Open API provides an endpoint that enables you to send a topic through your message broker and store it on a ServiceNow instance.
-   **[Event Notification Management Open API](../../../integrate/inbound-rest/concept/event_open-api.md#)**  
The Event Notification Management Open API provides an endpoint to create, update, and delete events from the Events \[em\_event\] table.
-   **[External Content Ingestion API](../../../integrate/inbound-rest/concept/external-content-ingestion-api.md#)**  
The External Content Ingestion API provides endpoints that enable ingestion of content from sources outside of your ServiceNow® instance into the ServiceNow® AI Search application's index.
-   **[External ID Mapping API](../../../integrate/inbound-rest/concept/external-id-mapping-api.md#)**  
Enables external Contact Center as a Service \(CCaaS\) platforms to store and retrieve routing identifiers for ServiceNow records.
-   **[HR REST API](../../../integrate/inbound-rest/concept/hr-core-api.md#)**  
The HR REST API provides endpoints that return information about employees that work or live in the United States.
-   **[Identification and Reconciliation API](../../../integrate/inbound-rest/concept/c_IdentifyReconcileAPI.md#)**  
The Identification and Reconciliation API provides endpoints that use the Identification and Reconciliation engine \(IRE\) to minimize creation of duplicate Configuration Items \(CIs\) and to reconcile CI attributes by only accepting information from authorized sources when updating the Configuration Management Database \(CMDB\).
-   **[Import Set API](../../../integrate/inbound-rest/concept/c_ImportSetAPI.md#)**  
The Import Set API provides endpoints that allow you to interact with import set tables.
-   **[Install Base Item API](../../../integrate/inbound-rest/concept/integrations-api.md#)**  
The Install Base Item API provides endpoints to access and manage install base items records within a ServiceNow instance.
-   **[Knowledge Management REST API](../../../integrate/inbound-rest/concept/knowledge-api.md#)**  
The Knowledge Management API provides endpoints for searching, viewing, and fetching lists of the most-viewed and featured knowledge articles.
-   **[lead API](../../../integrate/inbound-rest/concept/lead-api.md#)**  
The lead API provides endpoints that enable you to create, update, and query/retrieve marketing leads and their associated lead line items from an instance.
-   **[MetricBase Time Series API](../../../integrate/inbound-rest/concept/Clotho-Time-Series-API.md#)**  
The MetricBase Time Series API provides endpoints to insert data into, retrieve information from, and to run transforms against a MetricBase database.
-   **[Omnichannel Callback API](../../../integrate/inbound-rest/concept/omichannel-callback-api.md#)**  
The Omnichannel Callback API provides methods for creating, updating, and initiating a callback request for live agent conversations.
-   **[openframe API](../../../integrate/inbound-rest/concept/openframe-api.md#)**  
The openframe API provides endpoints that provide Contact Center as a Service \(CCaaS\) the ability to create and update interaction records without using the Operation Handler.
-   **[Order API](../../../integrate/inbound-rest/concept/order_csm-api.md#)**  
The Order API provides endpoints for retrieving and creating orders with order line items for the Customer Service Management application.
-   **[Party Management Open API](../../../integrate/inbound-rest/concept/tmf-party-management-open-api.md#)**  
The Party Management Open API provides endpoints for managing parties with a relationship to the enterprise, like a consumer, account, or contact. Use this API to create, update, and retrieve data from the Consumer \[csm\_consumer\], Account \[customer\_account\], and Contact \[customer\_contact\] tables.
-   **[Predictive Intelligence API](../../../integrate/inbound-rest/concept/agent-intelligence-api.md#)**  
The Predictive Intelligence API provides endpoints that predict a field value based on one or more input fields and a trained solution.
-   **[Proactive Engagement API](../../../integrate/inbound-rest/concept/proactive-engagement-api.md#)**  
The Proactive Engagement API provides an endpoint for creating digital experience issues.
-   **[Product Catalog Open API](../../../integrate/inbound-rest/concept/product-catalog-open-api.md#)**  
The Product Catalog Open API provides endpoints to create and retrieve product catalogs, product offerings, and product specifications.
-   **[Product Inventory Open API](../../../integrate/inbound-rest/concept/product-inventory-open-api.md#)**  
The Product Inventory Open API provides endpoints to create and retrieve product inventories.
-   **[Product Order Open API](../../../integrate/inbound-rest/concept/tmf622_product_ordering-api.md#)**  
The Product Order Open API provides endpoints that enable a standardized mechanism for placing product orders.
-   **[Project Portfolio Management API](../../../integrate/inbound-rest/concept/ppm-api.md#)**  
The Project Portfolio Management API provides endpoints to bulk import cost plans and project tasks.
-   **[Push Installation API](../../../integrate/inbound-rest/concept/pushinstallation-api.md#)**  
The Push Installation API provides endpoints to register and unregister the tokens that enable mobile devices to receive push notifications from an application.
-   **[Push Metrics API](../../../integrate/inbound-rest/concept/push-metrics-MID-server.md#)**  
The Push Metrics API provides endpoints that enable you to push raw Metric Intelligence data from an external source to the MID Server.
-   **[Quote Management API](../../../integrate/inbound-rest/concept/quote-management-api.md#)**  
The Quote Management API provides endpoints to create, update, and retrieve customer quote data.
-   **[Remote help request API](../../../integrate/inbound-rest/concept/remote_help_request-api.md#)**  
The Remote help request API provides endpoints to create, view, and fetch lists of IT service requests and their details from an electronic medical record \(EMR\) system. An IT service request is associated with a task type such as an incident in the ServiceNow instance.
-   **[Resource Inventory Open API](../../../integrate/inbound-rest/concept/resource-inventory-api.md#)**  
The Resource Inventory Open API provides endpoints to create, retrieve, and delete resources.
-   **[Response Templates API](../../../integrate/inbound-rest/concept/response-templates-api.md#)**  
The Response Templates API provides endpoints to handle records in the Response Templates \[sn\_templated\_snip\_note\_template\] table.
-   **[Sales Agreement API](../../../integrate/inbound-rest/concept/sales_agreement-api.md#)**  
The Sales Agreement API provides methods for creating a new sales agreement and retrieving an existing sales agreement of a given sys\_id.
-   **[SAM-Software Usage Data Integration API](../../../integrate/inbound-rest/concept/sam_soft_us_int-api.md#)**  
The SAM-Software Usage Data Integration API provides endpoints to create and update records in the Software Usage \[samp\_sw\_usage\] table.
-   **[Scorecards API](../../../integrate/inbound-rest/concept/c_PerformanceAnalyticsAPI.md#)**  
The Scorecards API provides endpoints that enable you to query data about Performance Analytics indicators. The query parameters equate to the functions available on the Analytics Hub for drilling down into an indicator.
-   **[Script Debugger API](../../../integrate/inbound-rest/concept/scriptdebugger-api.md#)**  
The Script Debugger API provides endpoints to debug lines of server-side JavaScript code, such as business rules and script includes.
-   **[Service Catalog API](../../../integrate/inbound-rest/concept/c_ServiceCatalogAPI.md#)**  
The Service Catalog API provides endpoints that access Service Catalog configuration and actions from within a Service Portal.
-   **[Service Catalog Open API](../../../integrate/inbound-rest/concept/service-catalog-open-api.md#)**  
The Service Catalog Open API provides endpoints to create, update, retrieve, and delete service specifications and service categories.
-   **[Service Contract API](../../../integrate/inbound-rest/concept/servicecontract-api.md#)**  
The Service Contract API provides endpoints to create and retrieve service contract records.
-   **[Service Order Open API](../../../integrate/inbound-rest/concept/service-order-open-api.md#)**  
The Service Order Open API provides endpoints that enable a standardized mechanism for placing service orders.
-   **[Service Test Management Open API](../../../integrate/inbound-rest/concept/service-test-management-api.md#)**  
The Service Test Management Open API provides endpoints to create and retrieve service test definitions and service tests.
-   **[SG Services API](../../../integrate/inbound-rest/concept/sg_services-api.md#)**  
The SG Services API provides endpoints to create and manage application services and the upstream relationships between them.
-   **[SpendInt APIs](../../../integrate/inbound-rest/concept/spendint-api.md#)**  
SpendInt APIs are inbound REST APIs that enable external procurement systems to send catalog, pricing, order, shipment, and invoice data into ServiceNow Sourcing and Procurement Operations, synchronizing structured procurement data from third-party systems.
-   **[System for Cross-domain Identity Management \(SCIM\) API](../../../integrate/inbound-rest/concept/scim-api.md#)**  
The System for Cross-domain Identity Management \(SCIM\) API provides endpoints to create, read, update, and delete operations on users and groups using the SCIM protocol.
-   **[Table API](../../../integrate/inbound-rest/concept/c_TableAPI.md#)**  
The Table API provides endpoints that allow you to perform create, read, update, and delete \(CRUD\) operations on existing tables.
-   **[Technical Service Qualification Open API](../../../integrate/inbound-rest/concept/ts-qualification-api.md#)**  
The Technical Service Qualification Open API provides endpoints to check the availability of resources and services before submitting orders for fulfillment.
-   **[TISC API](../../../integrate/inbound-rest/concept/tisc-api.md#)**  
The TISC API provides endpoints to add and retrieve threat intelligence data in the Threat Intelligence Security Center \(TISC\) application.
-   **[TISC Intel Exchange API](../../../integrate/inbound-rest/concept/tisc-intel-ex-api.md#)**  
Enables external systems to share threat intelligence data with the Threat Intelligence Security Center \(TISC\) application.
-   **[TISC RPZ API](../../../integrate/inbound-rest/concept/tisc-rpz-api.md#)**  
The TISC RPZ API provides an endpoint to export domains and IP addresses in Response Policy Zone \(RPZ\) format.
-   **[TISC TAXII Server API](../../../integrate/inbound-rest/concept/taxii-server-api.md#)**  
Provides Trusted Automated Exchange of Intelligence Information \(TAXII\) server endpoints for sharing threat intelligence data in Threat Intelligence Security Center \(TISC\) from one ServiceNow instance to another.
-   **[Trouble Ticket Open API](../../../integrate/inbound-rest/concept/trouble-ticket-open-api.md#)**  
The Trouble Ticket Open API provides endpoints to create, update, and retrieve data from the Case \[sn\_customerservice\_case\], Incident \[incident\], and Service Problem Case \[sn\_sprb\_mgmt\_case\] tables.
-   **[User Role Inheritance API](../../../integrate/inbound-rest/concept/user-role-inheritance-api.md#)**  
The User Role Inheritance API provides endpoints that allow you to see the roles that a specific user inherited.
-   **[Verify Entitlements API](../../../integrate/inbound-rest/concept/verifyentitlements-api.md#)**  
The Verify Entitlements API provides endpoints that enable you to obtain a list of valid entitlements, details about the characteristics of entitlements, and an entitlement's latest usage information.
-   **[Virtual Agent Bot Integration API](../../../integrate/inbound-rest/concept/bot-api.md#)**  
The Virtual Agent Bot Integration API provides endpoints that allow users to integrate any chat interface or a bot ecosystem with the ServiceNow Virtual Agent and/or Live Agent.
-   **[Voice Interaction Resource API](../../../integrate/inbound-rest/concept/voice-interaction-resource-api.md#)**  
The Voice Interaction API provides endpoints to transcribe and store voice interactions between agents and callers during a telephone conversation. It works in conjunction with Virtual Agent and Live Agent chats.
-   **[Work Order Management API](../../../integrate/inbound-rest/concept/work-order-mgmt-api.md#)**  
The Work Order Management API provides endpoints to create, update, and retrieve work orders.
-   **[Workplace Connector Webhook API](../../../integrate/inbound-rest/concept/workplace_connector_webhook-api.md#)**  
The Workplace Connector Webhook API is a generic interface that enables data from different kinds of workplace hardware or sensors \(such as badging systems or occupancy sensors\) to be stored in Workplace Service Delivery tables.
-   **[Wrap Up API](../../../integrate/inbound-rest/concept/wrap-up-api.md#)**  
Provides endpoints for managing wrap-up functionality for external Contact Center as a Service \(CCaaS\) systems or ServiceNow AI Platform workspaces.
-   **[WSD Extra Service API](../../../integrate/inbound-rest/concept/wsd_extra_service-api.md#)**  
The Workplace Service Delivery \(WSD\) Extra Service API provides endpoints to retrieve extra services, such as location layouts and standard services of a workplace location.
-   **[WSD Extra Service Request API](../../../integrate/inbound-rest/concept/wsd_extra_serv_req-api.md#)**  
The Workplace Service Delivery \(WSD\) Extra Service Request API provides endpoints to manage extra service requests for reservations.
-   **[WSD Group Reservation API](../../../integrate/inbound-rest/concept/wsd_grp_reserv-api.md#)**  
The Workplace Service Delivery \(WSD\) Group Reservation API provides endpoints for managing group reservations.
-   **[WSD Multi Reservation API](../../../integrate/inbound-rest/concept/wsd_multi_reserv-api.md#)**  
The Workplace Service Delivery \(WSD\) Multi Reservation API provides endpoints for managing reservations with multiple workplace locations.
-   **[WSD Recurring Reservation API](../../../integrate/inbound-rest/concept/wsd_recur_reserv-api.md#)**  
The Workplace Service Delivery \(WSD\) Recurring Reservation API provides endpoints for managing reservations that occur at the same time, but have different dates.
-   **[WSD Reservable API](../../../integrate/inbound-rest/concept/wsd_reservable-api.md#)**  
The Workplace Service Delivery \(WSD\) Reservable API provides endpoints to retrieve details of a reservable, an entity that can be reserved, such as a workplace location, from a ServiceNow instance.
-   **[WSD Reservable V2 API](../../../integrate/inbound-rest/concept/wsd_reservable-V2-api.md#)**  
The Workplace Service Delivery \(WSD\) Reservable V2 API provides endpoints to retrieve details of a reservable, an entity that can be reserved, such as a workplace location, from a ServiceNow instance.
-   **[WSD Reservable Module API](../../../integrate/inbound-rest/concept/wsd_reservable_module-api.md#)**  
The Workplace Service Delivery \(WSD\) Reservable Module API provides endpoints to retrieve details of a reservable module from a ServiceNow instance.
-   **[WSD Reservation API](../../../integrate/inbound-rest/concept/wsd_reservation-api.md#)**  
The Workplace Service Delivery \(WSD\) Reservation API provides endpoints for managing workplace reservations.
-   **[WSD Reservation Invitees API](../../../integrate/inbound-rest/concept/wsd_reservation_invitees-api.md#)**  
The Workplace Service Delivery \(WSD\) Reservation Invitees API provides endpoints to add invitees to reservations, fetch invitees of a reservation, and reassign invitees of a reservation.
-   **[WSD Search API](../../../integrate/inbound-rest/concept/wsd_search-api.md#)**  
The Workplace Service Delivery \(WSD\) Search API provides endpoints to search for available locations and workplace items such as reservables, reservable modules, and available shifts.
-   **[WSD Shift API](../../../integrate/inbound-rest/concept/wsd_shift-api.md#)**  
The Workplace Service Delivery \(WSD\) Shift API provides an endpoint that returns shift time spans for a specified date and time.

**Parent Topic:**[API reference](api-reference.md)

