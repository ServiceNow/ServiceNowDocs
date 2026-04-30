---
title: Browse APIs by product
description: Find APIs to use with your ServiceNow products.
locale: en-US
release: zurich
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 68
breadcrumb: [API reference, API implementation and reference]
---

# Browse APIs by product

Find APIs to use with your ServiceNow products.

Browse the table below to view which Server, REST, and Client APIs are supported by a specific ServiceNow product. All products and APIs display by default in alphabetical order. To see only APIs of those products you are interested in, select one or more product names in the **Product** filter drop-down on this page. Once you select a product in the filter, only the APIs for your selection\(s\) display in the table. Clear filter criteria by deselecting options in the filter drop-down.

In the APIs column, simply hover over a link to read a short description about an API's functionality, or click the link to view its full reference documentation. An asterisk\* indicates that the API is offered in all ServiceNow products.

<table id="table_acd_tw1_tvb" class="custom-rows"><thead><tr><th class="filter">

Product

</th><th>

APIs

</th></tr></thead><tbody><tr><td>

Advanced Work Assignment

</td><td>

-   **Server**
    -   [Agent - Global](../../../app-store/dev_portal/API_reference/Agent/concept/c_AgentAPI.md#)
    -   [Queue - Global](../../../app-store/dev_portal/API_reference/Queue_global/concept/c_QueueAPI.md#)
    -   [Queue - Scoped](../../../app-store/dev_portal/API_reference/Queue/concept/QueueScopedAPI.md#)
-   **REST**
    -   [AWA Agent API](../../../integrate/inbound-rest/concept/agent-api.md#)
    -   [AWA Manual Assignment API](../../../integrate/inbound-rest/concept/awa_manual_assign-api.md#)
    -   [AWA Inbox Actions API](../../../integrate/inbound-rest/concept/awa-inbox-actions-api.md#)
    -   [AWA Routing API](../../../integrate/inbound-rest/concept/queue-api.md#)

</td></tr><tr><td>

Agent Client Collector

</td><td>

-   **Server**
    -   [AccAgentsAPI - Scoped](../../../app-store/dev_portal/API_reference/AccAgentsAPI/concept/AccAgentsAPIAPIScoped.md#)
    -   [AccCheckDefsAPI - Scoped](../../../app-store/dev_portal/API_reference/AccCheckDefsAPI/concept/AccCheckDefsAPIAPIScoped.md#)
    -   [AgentNowHandler - Scoped](../../../app-store/dev_portal/API_reference/AgentNowHandler/concept/AgentNowHandlerAPIScoped.md#)
    -   [CheckDefinitionTestBuilder - Scoped](../../../app-store/dev_portal/API_reference/CheckDefinitionTestBuilder/concept/CheckDefinitionTestBuilderAPIScope.md#)
    -   [CheckInstanceTestBuilder - Scoped](../../../app-store/dev_portal/API_reference/CheckInstanceTestBuilder/concept/CheckInstanceTestBuilderAPIScoped.md#)
-   **REST**
    -   [Agent Client Collector API](../../../integrate/inbound-rest/concept/agnt_clnt_cll-api.md#)
    -   [Push Metrics API](../../../integrate/inbound-rest/concept/push-metrics-MID-server.md#)

</td></tr><tr><td>

Agent Workspace

</td><td>

-   **Client**

[GlideAgentWorkspace \(g\_aw\)](../../../app-store/dev_portal/API_reference/GlideAgentWorkspace/concept/GlideAgentWorkspaceAPI.md#)


</td></tr><tr><td>

AI Search

</td><td>

-   **Server**
    -   [GeniusResultAnswer - Scoped](../../../app-store/dev_portal/API_reference/GeniusResultAnswerScoped/concept/GeniusResultAnswerScopedAPI.md#)
    -   [GeniusResultContext - Scoped](../../../app-store/dev_portal/API_reference/GeniusResultContextScoped/concept/GeniusResultContextScopedAPI.md#)
-   **REST**
    -   [AI Search External User Mapping API](../../../integrate/inbound-rest/concept/ext-user-mapping-api.md#)
    -   [External Content Ingestion API](../../../integrate/inbound-rest/concept/external-content-ingestion-api.md#)

</td></tr><tr><td>

Automation Center

</td><td>

-   **REST**

[Automation Center API](../../../integrate/inbound-rest/concept/auto-api.md#)


</td></tr><tr><td>

Change Management

</td><td>

-   **Server**

[ChangeCollisionHelper - Global](../../../app-store/dev_portal/API_reference/ChangeCollisionHelper/concept/c_ChangeCollisionHelperAPI.md#)

[ChangeSuccess - Scoped](../../../app-store/dev_portal/API_reference/ChangeSuccess/concept/ChangeSuccessScopedAPI.md#)

-   **REST**

[Change Management API](../../../integrate/inbound-rest/concept/change-management-api.md#)


</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   **Server**
    -   [CIRelatedList - Global](../../../app-store/dev_portal/API_reference/CIRelatedList/concept/c_CIRelatedListAPI.md#)
    -   [CIUtils - Global](../../../app-store/dev_portal/API_reference/CIUtils/concept/c_CIUtilsAPI.md#)
    -   [CMDBDuplicateTaskUtils - Global](../../../app-store/dev_portal/API_reference/CMDBDuplicateTaskUtilsAPI/concept/CMDBDuplicateTaskUtilsAPI.md#)
    -   [CMDBDuplicateTemplateUtil - Global](../../../app-store/dev_portal/API_reference/CMDBDuplicateTemplateUtils/concept/CMDBDuplicateTemplateUtilAPI.md#)
    -   [CMDBGroupAPI - Scoped](../../../app-store/dev_portal/API_reference/CMDBGroupAPIScoped/concept/c_CMDBGroupAPIScoped.md#)
    -   [CMDBQueryBuilderAPI - Global](../../../app-store/dev_portal/API_reference/CMDBQueryBuilderAPI/concept/CMDBQueryBuilderAPI.md#)
    -   [CMDBTransformUtil - Global](../../../app-store/dev_portal/API_reference/CMDBTransformUtil/concept/c_CMDBTransformUtilAPI.md#)
    -   [CMDBUtil - Global](../../../app-store/dev_portal/API_reference/CMDBUtil/concept/c_CMDBUtilAPI.md#)
    -   [DuplicateTemplate - Scoped](../../../app-store/dev_portal/API_reference/DuplicateTemplateScoped/concept/DuplicateTemplateScopedAPI.md#)
    -   [IdentificationEngine - Scoped](../../../app-store/dev_portal/API_reference/IdentificationEngineScoped/concept/IdentificationEngineScopedAPI.md#)
    -   [IdentificationEngineScriptableApi - Global](../../../app-store/dev_portal/API_reference/IdentificationEngineScriptableApi/concept/c_IdentEngineScriptAPI.md#)
    -   [ProductInstance - Scoped, Global](../../../app-store/dev_portal/API_reference/ProductInstanceAPIBoth/concept/ProductInstanceBothAPI.md#)
    -   [StateManagementScriptableApi - Global](../../../app-store/dev_portal/API_reference/StateManagementScriptableApi/concept/StateManagementScriptableApi.md#)
-   **REST**
    -   [Application Service API](../../../integrate/inbound-rest/concept/application-service-api.md#)
    -   [CI Lifecycle Management API](../../../integrate/inbound-rest/concept/ci-lifecycle-management-api.md#)
    -   [CMDB Data Ingestion API](../../../integrate/inbound-rest/concept/cmdb-ingest-api.md#)
    -   [CMDB Instance API](../../../integrate/inbound-rest/concept/cmdb-instance-api.md#)
    -   [CMDB Meta API](../../../integrate/inbound-rest/concept/cmdb-meta-api.md#)
    -   [Identification and Reconciliation API](../../../integrate/inbound-rest/concept/c_IdentifyReconcileAPI.md#)
    -   [SG Services API](../../../integrate/inbound-rest/concept/sg_services-api.md#)

</td></tr><tr><td>

Cost Management

</td><td>

-   **Server**
    -   [ExpenseAllocation - Global](../../../app-store/dev_portal/API_reference/ExpenseAllocation/concept/c_ExpenseAllocationAPI.md#)
    -   [ExpenseLine - Global](../../../app-store/dev_portal/API_reference/ExpenseLine/concept/c_ExpenseLineAPI.md#)

</td></tr><tr><td>

Customer Service Management \(CSM\)

</td><td>

-   **REST**
    -   [Account API](../../../integrate/inbound-rest/concept/account-api.md#)
    -   [ActivitySubscriptions API](../../../integrate/inbound-rest/concept/actsub-api.md#)
    -   [Appointment API](../../../integrate/inbound-rest/concept/appointment-api.md#)
    -   [Case API](../../../integrate/inbound-rest/concept/case-api.md#)
    -   [Consumer API](../../../integrate/inbound-rest/concept/consumer-api.md#)
    -   [Contact API](../../../integrate/inbound-rest/concept/contact-api.md#)
    -       -   [CSM Attachment API](../../../integrate/inbound-rest/concept/attachment_csm-api.md#)
    -   [Customer Central API](../../../integrate/inbound-rest/concept/cust_central-api.md#)
    -   [Entitlement API](../../../integrate/inbound-rest/concept/entitlement-api.md#)
    -   [Install Base Item API](../../../integrate/inbound-rest/concept/integrations-api.md#)
    -   [openframe API](../../../integrate/inbound-rest/concept/openframe-api.md#)
    -   [Order API](../../../integrate/inbound-rest/concept/order_csm-api.md#)
    -   [Service Contract API](../../../integrate/inbound-rest/concept/servicecontract-api.md#)
    -   [Verify Entitlements API](../../../integrate/inbound-rest/concept/verifyentitlements-api.md#)
    -   [Party Management Open API](../../../integrate/inbound-rest/concept/tmf-party-management-open-api.md#)
-   **Server**
    -   [LeadtoCashCore - Scoped](../../../app-store/dev_portal/API_reference/LeadtoCashCoreScoped/concept/LeadToCashCoreAPI.md#)
    -   [NotifyJsTelephonyDriver - Global](../../../app-store/dev_portal/API_reference/NotifyJsTelephonyDriver/concept/NotifyJsTelephonyDriverAPI.md#)
    -   [NotifyPhoneNumber - Global](../../../app-store/dev_portal/API_reference/NotifyPhoneNumber/concept/c_NotifyPhoneNumberAPI.md#)
    -   [NotifyPhoneNumber - Scoped](../../../app-store/dev_portal/API_reference/NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#)
    -   [NotifySMS - Global](../../../app-store/dev_portal/API_reference/NotifySMS/concept/NotifySMSAPI.md#)
    -   [NotifyNow \(Legacy\) - Global](../../../app-store/dev_portal/API_reference/NotifyNow/concept/c_NotifyNow.md#)
    -   [NotifyUtil - Global](../../../app-store/dev_portal/API_reference/NotifyUtil/concept/NotifyUtilAPI.md#)
    -   [PDAutomationProvider - Scoped, Global](../../../app-store/dev_portal/API_reference/PDAutomationProviderBoth/concept/PDAutomationProviderBothAPI.md#)
    -   [SMSPreferenceHandlerSNC - Scoped, Global](../../../app-store/dev_portal/API_reference/SMSPreferenceHandler/concept/SMSPreferenceHandlerAPI.md#)
-   **Client**

[openFrameAPI - Client](../../../app-store/dev_portal/API_reference/openFrameAPI/concept/c_openFrameAPI.md#)


</td></tr><tr><td>

DevOps

</td><td>

-   **Server**
    -   [DevOpsOrchestrationToolIntegrationHandler - Scoped](../../../app-store/dev_portal/API_reference/DevOpsOrchToolIntHandlerScoped/concept/DevOpsOrchToolIntHandlerScopedAPI.md#)
    -   [CdmQuery - Scoped](../../../app-store/dev_portal/API_reference/CdmQuery/concept/CdmQueryScopedAPI.md#)
-   **REST**
    -   [CdmApplicationsApi](../../../integrate/inbound-rest/concept/applications-api.md#)
    -   [CdmChangesetsApi](../../../integrate/inbound-rest/concept/changesets-api.md#)
    -   [CdmEditorApi](../../../integrate/inbound-rest/concept/editor-api.md#)
    -   [CdmPoliciesApi](../../../integrate/inbound-rest/concept/policies-api.md#)
    -   [CdmSharedLibraryApi](../../../integrate/inbound-rest/concept/shared_libraries-api.md#)
    -   [CdmSnapshotApi](../../../integrate/inbound-rest/concept/snapshot-api.md#)
    -   [CdmVersionApi](../../../integrate/inbound-rest/concept/versions-api.md#)
    -   [DevOps API](../../../integrate/inbound-rest/concept/devops-api.md#)
    -   [DevOps Config API](../../../integrate/inbound-rest/concept/devops-config-api.md#)

</td></tr><tr><td>

Discovery

</td><td>

-   **Server**
    -   [AbstractReconciler - Global](../../../app-store/dev_portal/API_reference/AbstractReconciler/concept/c_AbstractReconciler.md#)
    -   [APCHandler - Global](../../../app-store/dev_portal/API_reference/APCHandler/concept/c_APCHandlerAPI.md#)
    -   [ApcPduOutletReconciler - Global](../../../app-store/dev_portal/API_reference/ApcPduOutletReconciler/concept/c_ApcPduOutletReconcilerAPI.md#)
    -   [CIData - Global](../../../app-store/dev_portal/API_reference/CIData/concept/c_CIDataAPI.md#)
    -   [CIIdentification - Global](../../../app-store/dev_portal/API_reference/CIIdentification/concept/c_CIIdentificationAPI.md#)
    -   [CIIdentifierResult - Global](../../../app-store/dev_portal/API_reference/CIIdentifierResult/concept/c_CIIdentifierResultAPI.md#)
    -   [CimCIData - Global](../../../app-store/dev_portal/API_reference/CimCIData/concept/c_CimCIDataAPI.md#)
    -   [CimIDSensor - Global](../../../app-store/dev_portal/API_reference/CimIDSensorAPI/concept/c_CimIDSensorAPI.md#)
    -   [CimInstanceToken - Global](../../../app-store/dev_portal/API_reference/CimInstanceToken/concept/c_CimInstanceTokenAPI.md#)
    -   [CimProbe - Global](../../../app-store/dev_portal/API_reference/CimProbe/concept/c_CimProbeAPI.md#)
    -   [CimProbeResult - Global](../../../app-store/dev_portal/API_reference/CimProbeResult/concept/c_CimProbeResultAPI.md#)
    -   [ClassifierProbes - Global](../../../app-store/dev_portal/API_reference/ClassifierProbes/concept/c_ClassifierProbesAPI.md#)
    -   [DiscoveryAPI - Scoped](../../../app-store/dev_portal/API_reference/DiscoveryAPIScoped/concept/c_DiscoveryAPIScopedAPI.md#)
    -   [IDResult - Global](../../../app-store/dev_portal/API_reference/IDResult/concept/c_IDResultAPI.md#)
    -   [IPAddress - Scoped, Global](../../../app-store/dev_portal/API_reference/IPAddress/concept/IPAddressAPIBoth.md#)\*
    -   [IPAddressFixup - Global](../../../app-store/dev_portal/API_reference/IPAddressFixup/concept/c_IPAddressFixupAPI.md#)
    -   [IPService - Global](../../../app-store/dev_portal/API_reference/IPService/concept/c_IPServiceAPI.md#)
    -   [QuickRanges - Global](../../../app-store/dev_portal/API_reference/QuickRanges/concept/c_QuickRangesAPI.md#)
    -   [ReportCiStatusOutputJS - Scoped](../../../app-store/dev_portal/API_reference/ReportCiStatusOutputJSScoped/concept/c_ReportCiStatusOutputJSScopedAPI.md#)
    -   [RoundingInterval - Global](../../../app-store/dev_portal/API_reference/RoundingInterval/concept/c_RoundingIntervalAPI.md#)
    -   [SerialNumberManager - Global](../../../app-store/dev_portal/API_reference/SerialNumberManager/concept/c_SerialNumberManagerAPI.md#)
    -   [ServiceRegistryQuery - Global](../../../app-store/dev_portal/API_reference/ServiceRegistryQuery/concept/c_ServiceRegistryQueryAPI.md#)
    -   [ShazzamLaunch - Global](../../../app-store/dev_portal/API_reference/ShazzamLaunch/concept/c_ShazzamLaunchAPI.md#)
    -   [ShazzamResult - Global](../../../app-store/dev_portal/API_reference/ShazzamResult/concept/c_ShazzamResultAPI.md#)
    -   [ShazzamScanner - Global](../../../app-store/dev_portal/API_reference/ShazzamScanner/concept/c_ShazzamScannerAPI.md#)
    -   [SLPServiceRegistryQuery - Global](../../../app-store/dev_portal/API_reference/SLPServiceRegistryQuery/concept/c_SLPServiceRegistryQueryAPI.md#)
    -   [SNMPGatherDocParts - Global](../../../app-store/dev_portal/API_reference/SNMPGatherDocParts/concept/c_SNMPGatherDocPartsAPI.md#)
    -   [SNMPNetworkInterfaces - Global](../../../app-store/dev_portal/API_reference/SNMPNetworkInterfaces/concept/c_SNMPNetworkInterfacesAPI.md#)
    -   [SNMPResponse - Global](../../../app-store/dev_portal/API_reference/SNMPResponse/concept/c_SNMPResponseAPI.md#)
    -   [StartDiscovery - Global](../../../app-store/dev_portal/API_reference/StartDiscovery/concept/c_StartDiscoveryAPI.md#)
    -   [JSUtil - Global](../../../app-store/dev_portal/API_reference/JSUtil/concept/c_JSUtilAPI.md#)
    -   [UPSHandler - Global](../../../app-store/dev_portal/API_reference/UPSHandler/concept/c_UPSHandlerAPI.md#)
    -   [VMUtils - Global](../../../app-store/dev_portal/API_reference/VMUtils/concept/c_VMUtilsAPI.md#)\*
    -   [WindowsOSNameHelper - Global](../../../app-store/dev_portal/API_reference/WindowsOSNameHelper/concept/c_WindowsOSNameHelperAPI.md#)\*
    -   [XMLUtilJS - Global](../../../app-store/dev_portal/API_reference/XMLUtilJS/concept/c_XMLUtilJSAPI.md#)

</td></tr><tr><td>

Document Services

</td><td>

-   **Server**
    -   [Cell - Scoped, Global](../../../app-store/dev_portal/API_reference/CellBoth/concept/CellBothAPI.md#)
    -   [Color - Scoped, Global](../../../app-store/dev_portal/API_reference/ColorBoth/concept/ColorBothAPI.md#)
    -   [Document - Scoped, Global](../../../app-store/dev_portal/API_reference/DocumentBoth/concept/DocumentBothAPI.md#)
    -   [DocumentListEntryService - Scoped, Global](../../../app-store/dev_portal/API_reference/DocumentListEntryService/concept/DocumentListEntryServiceBothAPI.md#)
    -   [DocumentListService - Scoped, Global](../../../app-store/dev_portal/API_reference/DocumentListService/concept/DocumentListServiceBothAPI.md#)
    -   [DocumentReferenceService - Scoped, Global](../../../app-store/dev_portal/API_reference/DocumentReferenceService/concept/DocumentReferenceServiceBothAPI.md#)
    -   [DocumentService - Scoped, Global](../../../app-store/dev_portal/API_reference/DocumentService/concept/DocumentServiceBothAPI.md#)
    -   [DocumentVersionService - Scoped, Global](../../../app-store/dev_portal/API_reference/DocumentVersionService/concept/DocumentVersionServiceBothAPI.md#)
    -   [Line - Scoped, Global](../../../app-store/dev_portal/API_reference/LineBoth/concept/LineBothAPI.md#)
    -   [logger - Global](../../../app-store/dev_portal/API_reference/Logger/concept/c_Logger.md#)
    -   [Paragraph - Scoped, Global](../../../app-store/dev_portal/API_reference/ParagraphBoth/concept/ParagraphBothAPI.md#)
    -   [PDFGenerationAPI - Scoped, Global](../../../app-store/dev_portal/API_reference/PDFGenerationAPIBoth/concept/PDFGenerationAPIBothAPI.md#)
    -   [PdfMergeSignRequestor - Scoped, Global](../../../app-store/dev_portal/API_reference/PdfMergeSignRequestorBoth/concept/PdfMergeSignRequestorBothAPI.md#)
    -   [PdfPage - Scoped, Global](../../../app-store/dev_portal/API_reference/PdfPageBoth/concept/PdfPageBothAPI.md#)
    -   [Image - Scoped, Global](../../../app-store/dev_portal/API_reference/ImageBoth/concept/ImageBothAPI.md#)
    -   [Style - Scoped, Global](../../../app-store/dev_portal/API_reference/StyleBoth/concept/StyleBothAPI.md#)
    -   [SVGToPDFConversionAPI - Scoped, Global](../../../app-store/dev_portal/API_reference/SVGToPDFConversionAPIBoth/concept/SVGToPDFConversionAPBothAPI.md#)
    -   [SystemDocument - Scoped, Global](../../../app-store/dev_portal/API_reference/SystemDocument/concept/SystemDocumentBothAPI.md#)
    -   [SystemDocumentList - Scoped, Global](../../../app-store/dev_portal/API_reference/SystemDocumentList/concept/SystemDocumentListBothAPI.md#)
    -   [SystemDocumentListEntry - Scoped, Global](../../../app-store/dev_portal/API_reference/SystemDocumentListEntry/concept/SystemDocumentListEntryBothAPI.md#)
    -   [SystemDocumentVersion - Scoped, Global](../../../app-store/dev_portal/API_reference/SystemDocumentVersion/concept/SystemDocumentVersionBothAPI.md#)
    -   [Table - Scoped, Global](../../../app-store/dev_portal/API_reference/TableBoth/concept/TableBothAPI.md#)

</td></tr><tr><td>

Dynamic Translation

</td><td>

-   **Client**

[DynamicTranslation - Client](../../../app-store/dev_portal/API_reference/DynamicTranslation/concept/DynamicTranslation.md#)

-   **Server**

[DynamicTranslation - Scoped](../../../app-store/dev_portal/API_reference/DynamicTranslation/concept/DynamicTranslation.md#)


</td></tr><tr><td>

EMR Help

</td><td>

-   **REST**

[Remote help request API](../../../integrate/inbound-rest/concept/remote_help_request-api.md#)


</td></tr><tr><td>

Event Management

</td><td>

-   **Server**
    -   [Event - Global](../../../app-store/dev_portal/API_reference/Event/concept/EventAPI.md#)
    -   [IEventSender - Global](../../../app-store/dev_portal/API_reference/IEventSender/concept/IEventSenderAPI.md#)
    -   [SNEventSenderProvider - Global](../../../app-store/dev_portal/API_reference/SNEventSenderProvider/concept/SNEventSenderProviderAPI.md#)

</td></tr><tr><td>

Workflow Studio

</td><td>

-   **Client**

[GlideFlow - Client](../../../app-store/dev_portal/API_reference/GlideFlow/concept/GlideFlowAPI.md#)

-   **Server**
    -   [ActivityHistoryRecord - Global](../../../app-store/dev_portal/API_reference/ActivityHistoryRecord/concept/c_ActivityHistoryRecordAPI.md#)
    -   [FlowAPI - Scoped, Global](../../../app-store/dev_portal/API_reference/ScriptableFlowAPI/concept/ScriptableFlowAPI.md#)
    -   [FlowScriptAPI - Scoped](../../../app-store/dev_portal/API_reference/FlowScript/concept/FlowScriptAPI.md#)
    -   [Flow - Scoped \(deprecated\)](../../../app-store/dev_portal/API_reference/FlowScoped/concept/FlowScopedAPI.md#)
    -   [JSONStreamingAPI - Scoped](../../../app-store/dev_portal/API_reference/JSONStreamingAPI/concept/JSONStreamingAPIScopedAPI.md#)
    -   [JSONStreamingBuilder - Scoped](../../../app-store/dev_portal/API_reference/JSONStreamingBuilder/concept/JSONStreamingBuilderScopedAPI.md#)
    -   [Producer - Scoped \(deprecated\)](../../../app-store/dev_portal/API_reference/Producer/concept/ProducerScopedAPI.md#)
    -   [ProducerV2 - Scoped](../../../app-store/dev_portal/API_reference/ProducerV2/concept/ProducerV2ScopedAPI.md#)
    -   [ScriptableDataStream - Scoped, Global](../../../app-store/dev_portal/API_reference/ScriptableDataStream/concept/ScriptableDataStreamAPI.md#)
    -   [ScriptableFlowRunner - Scoped](../../../app-store/dev_portal/API_reference/ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#)
    -   [ScriptableFlowRunnerResult - Scoped](../../../app-store/dev_portal/API_reference/ScriptableFlowRunnerResultScoped/concept/ScriptableFlowRunnerResultScopedAPI.md#)
    -   [Subflow - Scoped \(deprecated\)](../../../app-store/dev_portal/API_reference/SubflowScoped/concept/SubflowScopedAPI.md#)
    -   [XMLStreamingAPI - Scoped](../../../app-store/dev_portal/API_reference/XMLStreamingAPI/concept/XMLStreamingAPIScopedAPI.md#)
    -   [XMLStreamingBuilder - Scoped](../../../app-store/dev_portal/API_reference/XMLStreamingBuilder/concept/XMLStreamingBuilderScopedAPI.md#)

</td></tr><tr><td>

Glide API – Attachments and files

</td><td>

-   **Server**
    -   [GlideEmailOutbound - Scoped](../../../app-store/dev_portal/API_reference/GlideEmailOutboundScoped/concept/c_GlideEmailOutboundScopedAPI.md#)
    -   [GlideExcelParser - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideExcelParserScoped/concept/GlideExcelParserScopedAPI.md#)
    -   [GlideJsonPath - Global](../../../app-store/dev_portal/API_reference/GlideJsonPath/concept/GlideJsonPathAPI.md#)
    -   [GlideScriptableInputStream - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideScriptableInputStreamScoped/concept/c_GlideScriptableInpStrmScopedAPI.md)
    -   [GlideSysAttachment - Global](../../../app-store/dev_portal/API_reference/GlideSysAttachmentGlobal/concept/GlideSysAttachmentGlobalAPI.md#)
    -   [GlideSysAttachment - Scoped](../../../app-store/dev_portal/API_reference/GlideSysAttachmentScoped/concept/c_GlideSysAttachmentScopedAPI.md#)
    -   [GlideSystem - Scoped](../../../app-store/dev_portal/API_reference/glideSystemScoped/concept/c_GlideSystemScopedAPI.md#)
    -   [GlideSystem - Global](../../../app-store/dev_portal/API_reference/GlideSystem/concept/c_GlideSystemAPI.md#)
    -   [GlideTextReader - Scoped](../../../app-store/dev_portal/API_reference/GlideTextReaderScoped/concept/c_GlideTextReaderScopedAPI.md#)
    -   [GlideXMLUtil - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideXMLUtilScoped/concept/GlideXMLUtilScopedAPI.md#)

</td></tr><tr><td>

Glide API - Client-server communication

</td><td>

-   **Server**
    -   [action - Scoped, Global](../../../app-store/dev_portal/API_reference/Action/concept/ActionAPIBoth.md#)
    -   [GlideappCalculationHelper - Global](../../../app-store/dev_portal/API_reference/GlideappCalculationHelper/concept/GlideappCalcHelperAPI.md#)
    -   [GlideApplicationProperty - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideApplicationProperty/concept/GlideApplicationProperty.md#)
    -   [GlideHTTPRequest - Global](../../../app-store/dev_portal/API_reference/GlideHTTPRequest/concept/GlideHTTPRequestAPI.md#)
    -   [GlideHTTPResponse - Global](../../../app-store/dev_portal/API_reference/GlideHTTPResponse/concept/GlideHTTPResponseAPI.md#)
    -   [GlideScriptedProcessor - Scoped](../../../app-store/dev_portal/API_reference/GlideScriptedProcessorScoped/concept/c_GlideScriptedProcessorScopedAPI.md#)
    -   [GlideServletRequest - Scoped](../../../app-store/dev_portal/API_reference/GlideServletRequestScoped/concept/c_GlideServletRequestScopedAPI.md#)
    -   [GlideServletResponse - Scoped](../../../app-store/dev_portal/API_reference/GlideServletResponseScoped/concept/c_GlideServletResponseScopedAPI.md#)
    -   [GlideSystem - Global](../../../app-store/dev_portal/API_reference/GlideSystem/concept/c_GlideSystemAPI.md#)
    -   [GlideSystem - Scoped](../../../app-store/dev_portal/API_reference/glideSystemScoped/concept/c_GlideSystemScopedAPI.md#)
    -   [GlideURI - Global](../../../app-store/dev_portal/API_reference/GlideURIGlobal/concept/GlideURIGlobalAPI.md#)
    -   [GlideURI - Scoped](../../../app-store/dev_portal/API_reference/GlideURIScoped/concept/c_GlideURIScopedAPI.md#)
-   **Client**
    -   [GlideAjax - Client](../../../app-store/dev_portal/API_reference/GlideAjax/concept/c_GlideAjaxAPI.md#)
    -   [GlideURLV3 - Client](../../../app-store/dev_portal/API_reference/GlideURLV3/concept/c_GlideURLV3API.md#)

</td></tr><tr><td>

Glide API - Currency

</td><td>

-   **Server**
    -   [GlideCurrencyConfig - Scoped](../../../app-store/dev_portal/API_reference/GlideCurrencyConfig/concept/GlideCurrencyConfigScopedAPI.md#)
    -   [GlideCurrencyConverter - Scoped](../../../app-store/dev_portal/API_reference/GlideCurrencyConverter/concept/GlideCurrencyConverterScopedAPI.md#)
    -   [GlideCurrencyExchangeValue - Scoped](../../../app-store/dev_portal/API_reference/GlideCurrencyExchangeValue/concept/GlideCurrencyExchangeValueScopedAPI.md#)
    -   [GlideCurrencyFormatter - Scoped](../../../app-store/dev_portal/API_reference/GlideCurrencyFormatter/concept/GlideCurrencyFormatterScopedAPI.md#)
    -   [GlideCurrencyParser - Scoped](../../../app-store/dev_portal/API_reference/GlideCurrencyParser/concept/GlideCurrencyParserScopedAPI.md#)
    -   [GlideCurrencyValue - Scoped](../../../app-store/dev_portal/API_reference/GlideCurrencyValue/concept/GlideCurrencyValueScopedAPI.md#)
    -   [GlideElementCurrency2 - Scoped](../../../app-store/dev_portal/API_reference/GlideElementCurrency2/concept/GlideElementCurrency2ScopedAPI.md#)

</td></tr><tr><td>

Glide API – Database operations and parsing data

</td><td>

-   **Server**
    -   [GlideAggregate - Global](../../../app-store/dev_portal/API_reference/GlideAggregate/concept/c_GlideAggregateAPI.md#)
    -   [GlideAggregate - Scoped](../../../app-store/dev_portal/API_reference/glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#)
    -   [GlideDBFunctionCaseBuilder - Global](../../../app-store/dev_portal/API_reference/GlideDBFunctionCaseBuilder/concept/GlideDBFunctionCaseBuilderAPI.md#)
    -   [GlideFilter - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideFilterScoped/concept/c_GlideFilterScopedAPI.md#)
    -   [GlideQuery - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideQuery/concept/GlideQueryGlobalAPI.md#)
    -   [GlideQueryCondition - Global](../../../app-store/dev_portal/API_reference/GlideQueryCondition/concept/c_GlideQueryConditionAPI.md#)
    -   [GlideQueryCondition - Scoped](../../../app-store/dev_portal/API_reference/glideQueryConditionScoped/concept/c_GlideQueryConditionScopedAPI.md#)
    -   [GlideRecord - Global](../../../app-store/dev_portal/API_reference/GlideRecord/concept/c_GlideRecordAPI.md#)
    -   [GlideRecord - Scoped](../../../app-store/dev_portal/API_reference/glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)
    -   [GlideRecordUtil - Global](../../../app-store/dev_portal/API_reference/GlideRecordUtil/concept/c_GlideRecordUtilAPI.md#)
    -   [GlideSystem - Global](../../../app-store/dev_portal/API_reference/GlideSystem/concept/c_GlideSystemAPI.md#)
    -   [GlideSystem - Scoped](../../../app-store/dev_portal/API_reference/glideSystemScoped/concept/c_GlideSystemScopedAPI.md#)
    -   [GlideUser - Global](../../../app-store/dev_portal/API_reference/GlideUser_global/concept/GUserAPI.md#)
    -   [GlideUser - Scoped](../../../app-store/dev_portal/API_reference/glideUserScoped/concept/c_GlideUserScopedAPI.md#)
    -   [Optional - Scoped, Global](../../../app-store/dev_portal/API_reference/Optional/concept/OptionalGlobalAPI.md#)
-   **Client**
    -   [GlideRecord - Client](../../../app-store/dev_portal/API_reference/GlideRecordClientSide/concept/c_GlideRecordClientSideAPI.md#)
    -   [GlideUser - Client](../../../app-store/dev_portal/API_reference/GlideUser/concept/c_GlideUserAPI.md#)
    -   [GlideUser \(Next Experience\) - Client](../../../app-store/dev_portal/API_reference/GlideUserNX/concept/GlideUserAPINX.md#)
    -   [i18N - Client](../../../app-store/dev_portal/API_reference/i18NV3/concept/c_i18NV3API.md#)
-   **REST**
    -   [Aggregate API](../../../integrate/inbound-rest/concept/c_AggregateAPI.md#)
    -   [Table API](../../../integrate/inbound-rest/concept/c_TableAPI.md#)

</td></tr><tr><td>

Glide API – Date and time

</td><td>

-   **Server**
    -   [DateTimeUtils - Global](../../../app-store/dev_portal/API_reference/DateTimeUtils/concept/c_DateTimeUtilsAPI.md#)
    -   [GlideCalendarDateTime - Scoped \(deprecated\)](../../../app-store/dev_portal/API_reference/GlideCalendarDateTime/concept/GlideCalendarDateTimeAPI.md#)
    -   [GlideDate - Global](../../../app-store/dev_portal/API_reference/GlideDate/concept/GlideDateAPI.md#)
    -   [GlideDate - Scoped](../../../app-store/dev_portal/API_reference/glideDateScoped/concept/c_GlideDateScopedAPI.md#)
    -   [GlideDateTime - Global](../../../app-store/dev_portal/API_reference/GlideDateTime/concept/c_GlideDateTimeAPI.md#)
    -   [GlideDateTime - Scoped](../../../app-store/dev_portal/API_reference/glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#)
    -   [GlideDuration - Scoped](../../../app-store/dev_portal/API_reference/glideDurationScoped/concept/c_GlideDurationScopedAPI.md#)
    -   [GlideImportSetTransformMap - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideImportSetTransformMap/concept/GlideImportSetTransformMapAPI.md#)
    -   [GlideMultiRecurrence - Scoped](../../../app-store/dev_portal/API_reference/GlideMultiRecurrence/concept/GlideMultiRecurrenceScopedAPI.md#)
    -   [GlideSchedule - Scoped](../../../app-store/dev_portal/API_reference/GlideScheduleScoped/concept/c_GlideScheduleScopedAPI.md#)
    -   [GlideSystem - Global](../../../app-store/dev_portal/API_reference/GlideSystem/concept/c_GlideSystemAPI.md#)
    -   [GlideSystem - Scoped](../../../app-store/dev_portal/API_reference/glideSystemScoped/concept/c_GlideSystemScopedAPI.md#)
    -   [GlideTime - Scoped](../../../app-store/dev_portal/API_reference/glideTimeScoped/concept/c_GlideTimeScopedAPI.md#)
    -   [GlideTimeline - Global](../../../app-store/dev_portal/API_reference/GlideTimeline/concept/c_GlideTimelineAPI.md#)
    -   [GlideTimelineItem - Global](../../../app-store/dev_portal/API_reference/GlideTimelineItem/concept/c_GlideTimelineItemAPI.md#)
-   **Client**
    -   [StopWatch - Client](../../../app-store/dev_portal/API_reference/StopWatch/concept/c_StopWatchAPI.md#)
    -   [StopWatch \(Next Experience\) - Client](../../../app-store/dev_portal/API_reference/StopWatchNX/concept/StopWatchAPINX.md#)

</td></tr><tr><td>

Glide API - Debug

</td><td>

-   **Server**
    -   [GlideScopedEvaluator - Global](../../../app-store/dev_portal/API_reference/glideEvaluator/concept/GlideEvaluatorAPI.md#)
    -   [GlideScopedEvaluator - Scoped](../../../app-store/dev_portal/API_reference/glideEvaluatorScoped/concept/c_GlideEvaluatorScopedAPI.md#)
    -   [GlideSystem - Global](../../../app-store/dev_portal/API_reference/GlideSystem/concept/c_GlideSystemAPI.md#)
    -   [GlideSystem - Scoped](../../../app-store/dev_portal/API_reference/glideSystemScoped/concept/c_GlideSystemScopedAPI.md#)
    -   [GSLog - Scoped, Global](../../../app-store/dev_portal/API_reference/GSLogBoth/concept/GSLogBoth.md#)

</td></tr><tr><td>

Glide API – Fields, forms, and lists

</td><td>

-   **Server**
    -   [GlideElement - Global](../../../app-store/dev_portal/API_reference/GlideElement_global/concept/c_GlideElementAPI.md#)
    -   [GlideElement - Scoped](../../../app-store/dev_portal/API_reference/glideElement/concept/c_GlideElementScopedAPI.md#)
    -   [GlideElementDescriptor - Scoped, Global](../../../app-store/dev_portal/API_reference/glideElementDescriptor/concept/c_GlideElementDescriptorScopedAPI.md#)
    -   [GlideGeoPoint - Global](../../../app-store/dev_portal/API_reference/GlideGeoPoint/concept/GlideGeopointGlobalAPI.md#)
    -   [GlideListProperties - Global](../../../app-store/dev_portal/API_reference/GlideListProperties/concept/GlideListPropertiesAPI.md#)
    -   [GlideSysListControl - Scoped](../../../app-store/dev_portal/API_reference/GlideSysListControlScoped/concept/c_GlideSysListControlScoped.md#)
    -   [GlideTableHierarchy - Scoped](../../../app-store/dev_portal/API_reference/GlideTableHierarchyScoped/concept/c_GlideTableHierarchyScopedAPI.md#)
-   **Client**
    -   [GlideDocument - Client](../../../app-store/dev_portal/API_reference/GlideDocumentV3/concept/c_GlideDocumentV3API.md#)
    -   [GlideForm \(g\_form\) - Client](../../../app-store/dev_portal/API_reference/GlideForm/concept/c_GlideFormAPI.md#)
    -   [GlideForm \(Next Experience\) - Client](../../../app-store/dev_portal/API_reference/GlideFormNX/concept/GlideFormAPINX.md#)
    -   [GlideList2 \(g\_list\) - Client](../../../app-store/dev_portal/API_reference/GlideList2/concept/c_GlideList2API.md#)
    -   [GlideList \(Next Experience\) - Client](../../../app-store/dev_portal/API_reference/GlideListClientNowEx/concept/GlideListClientAPINEx.md#)
    -   [GlideListV3 \(g\_list\) - Client \(deprecated\)](../../../app-store/dev_portal/API_reference/GlideListV3/concept/c_GlideListV3API.md#)

</td></tr><tr><td>

Glide API – Import set transformer

</td><td>

-   **Server**
    -   [GlideImportLog - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideImportLog/concept/GlideImportLogAPI.md#)
    -   [GlideImportSetRun - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideImportSetRun/concept/GlideImportSetRunAPI.md#)
    -   [GlideImportSetTable - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideImportSetTable/concept/GlideImportSetTableAPI.md#)
    -   [GlideImportSetTransformer - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideImportSetTransformer/concept/GlideImportSetTransformerAPI.md#)
    -   [GlideImportSetTransformMap - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideImportSetTransformMap/concept/GlideImportSetTransformMapAPI.md#)

</td></tr><tr><td>

Glide API - Localization

</td><td>

-   **Server**
    -   [NumberFormatter - Scoped, Global](../../../app-store/dev_portal/API_reference/NumberFormatterBoth/concept/NumberFormatterBoth.md#)
    -   [GlideElement - Scoped](../../../app-store/dev_portal/API_reference/glideElement/concept/c_GlideElementScopedAPI.md#)
        -   getDisplayValueLang\(\)
        -   getLabelLang\(\)

</td></tr><tr><td>

Glide API - Messages

</td><td>

-   **Server**
    -   [GlideDigest - Scoped](../../../app-store/dev_portal/API_reference/GlideDigestScoped/concept/c_GlideDigestScopedAPI.md#)
    -   [GlideSystem - Global](../../../app-store/dev_portal/API_reference/GlideSystem/concept/c_GlideSystemAPI.md#)
    -   [GlideSystem - Scoped](../../../app-store/dev_portal/API_reference/glideSystemScoped/concept/c_GlideSystemScopedAPI.md#)
    -   [GlideTransformLog - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideTransformLog/concept/GlideTransformLogAPI.md#)
-   **Client**
    -   [GlideDialogWindow - Client \(deprecated\)](../../../app-store/dev_portal/API_reference/GlideDialogWindow/concept/c_GlideDialogWindowAPI.md#)
    -   [GlideNotification - Client](../../../app-store/dev_portal/API_reference/GlideNotificationV3/concept/c_GlideNotificationV3API.md#)

</td></tr><tr><td>

Glide API - Mobile

</td><td>

-   **Client**

[Mobile GlideForm \(g\_form\) - Client](../../../app-store/dev_portal/API_reference/MobileGlideForm/concept/c_MobileGlideForm_API.md#)


</td></tr><tr><td>

Glide API - OAuth

</td><td>

-   **Server**
    -   [GlideOAuthClient - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideOAuthClient/concept/c_GlideOAuthClient.md#)
    -   [GlideOAuthClientRequest - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideOAuthClientRequest/concept/c_GlideOAuthClientRequest.md#)
    -   [GlideOAuthClientResponse - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideOAuthClientResponse/concept/c_GlideOAuthClientResponse.md#)
    -   [GlideOAuthToken - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideOAuthClientToken/concept/c_GlideOAuthToken.md#)

</td></tr><tr><td>

Glide API - Security

</td><td>

-   **Server**
    -   [GlideCertificateEncryption - Global](../../../app-store/dev_portal/API_reference/GlideCertificateEncryption/concept/c_GlideCertificateEncryptionAPI.md#)
    -   [GlideEncrypter - Global \(deprecated\)](../../../app-store/dev_portal/API_reference/GlideEncrypter/concept/GlideEncrypterAPI.md#)
    -   [GlideSecureRandomUtil - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideSecureRandomUtilScoped/concept/c_GlideSecureRandomUtilScopedAPI.md#)
    -   [GlideSecurityUtils - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideSecurityUtilsScoped/concept/GlideSecurityUtilsScopedAPI.md#)

</td></tr><tr><td>

Glide API – System

</td><td>

-   **Server**
    -   [GlideEventManager - Global](../../../app-store/dev_portal/API_reference/GlideEventManagerGlobal/concept/GlideEventManagerGlobalAPI.md#)
    -   [GlideImpersonate - Global](../../../app-store/dev_portal/API_reference/GlideImpersonate/concept/GlideImpersonateAPI.md#)
    -   [GlideLocale - Scoped](../../../app-store/dev_portal/API_reference/GlideLocaleScoped/concept/c_GlideLocaleScopedAPI.md#)
    -   [GlidePluginManager - Scoped](../../../app-store/dev_portal/API_reference/GlidePluginManagerScoped/concept/c_GlidePluginManagerScopedAPI.md#)
    -   [GlideScriptedExtensionPoint - Scoped](../../../app-store/dev_portal/API_reference/GlideScriptedExtensionPointAPI/concept/GlideScriptedExtPtScopedAPI.md#)
    -   [GlideSession - Global](../../../app-store/dev_portal/API_reference/GlideSession/concept/c_GlideSessionAPI.md#)
    -   [GlideSession - Scoped](../../../app-store/dev_portal/API_reference/GlideSessionScoped/concept/c_GlideSessionScopedAPI.md#)
    -   [GlideStringUtil - Scoped, Global](../../../app-store/dev_portal/API_reference/GlideStringUtilScoped/concept/GlideStringUtilScopedAPI.md#)
    -   [GlideSystem - Global](../../../app-store/dev_portal/API_reference/GlideSystem/concept/c_GlideSystemAPI.md#)
    -   [GlideSystem - Scoped](../../../app-store/dev_portal/API_reference/glideSystemScoped/concept/c_GlideSystemScopedAPI.md#)
    -   [GlideSystemRunLevel - Global](../../../app-store/dev_portal/API_reference/GlideSystemRunLevel/concept/GlideSystemRunLevelAPIGlobal.md#)
-   **Client**

[GlideGuid - Client](../../../app-store/dev_portal/API_reference/GlideGuidV3/concept/c_GlideGuidV3API.md#)


</td></tr><tr><td>

Glide API - UI – Classic UI

</td><td>

-   **Server**

[GlideUICompatibility - Scoped](../../../app-store/dev_portal/API_reference/GlideUICompatibilityScoped/concept/c_GlideUICompatibilityScopedAPI.md#)

-   **Client**
    -   [GlideList2 \(g\_list\) - Client](../../../app-store/dev_portal/API_reference/GlideList2/concept/c_GlideList2API.md#)
    -   [GlideMenu \(g\_menu and g\_item\) - Client](../../../app-store/dev_portal/API_reference/GlideMenu/concept/c_GlideMenuAPI.md#)
    -   [GlideModalForm - Client](../../../app-store/dev_portal/API_reference/GlideModalFormClientsideV3/concept/c_GlideModalFormV3API.md#)
    -   [GlideModal - Client](../../../app-store/dev_portal/API_reference/GlideModalClientSideV3/concept/c_GlideModalV3API.md#)
    -   [GlideNavigation - Client](../../../app-store/dev_portal/API_reference/GlideNavigationV3/concept/c_GlideNavigationV3API.md#)
    -   [GlideUIScripts - Client](../../../app-store/dev_portal/API_reference/GlideUIScripts/concept/GUIScriptsAPI.md#)

</td></tr><tr><td>

Glide API – UI – Next Experience

</td><td>

-   **Client**
    -   [GlideList \(Next Experience\) - Client](../../../app-store/dev_portal/API_reference/GlideListClientNowEx/concept/GlideListClientAPINEx.md#)
    -   [PolarisUI - Scoped](../../../app-store/dev_portal/API_reference/PolarisUIScoped/concept/PolarisUIScopedAPI.md#)
    -   [GlideModal \(Next Experience\) - Client](../../../app-store/dev_portal/API_reference/GlideModalClientNX/concept/GModClientAPINX.md#)
    -   [g\_modal \(Next Experience\) - Client](../../../app-store/dev_portal/API_reference/g_modalNX/concept/g_modalClientAPINX.md#)
    -   [GlideNavigation \(Next Experience\) - Client](../../../app-store/dev_portal/API_reference/GlideNavigationClientNX/concept/GlideNavigationClientAPINX.md#)

</td></tr><tr><td>

Field Service Management

</td><td>

-   **REST**

[Appointment API](../../../integrate/inbound-rest/concept/appointment-api.md#)

[Appointment Open API](../../../integrate/inbound-rest/concept/appointment-open-api.md#)


</td></tr><tr><td>

HR Service Delivery

</td><td>

-   **Server**
    -   [hr\_ActivitySet - Scoped](../../../app-store/dev_portal/API_reference/hr_ActivitySet/concept/hr_ActivitySetAPI.md#)
    -   [hr\_ActivityUtils - Scoped](../../../app-store/dev_portal/API_reference/hr_ActivityUtils/concept/hr_ActivityUtilsAPI.md#)
    -   [hr\_Utils - Scoped](../../../app-store/dev_portal/API_reference/hr_Utils/concept/hr_UtilsAPI.md#)
-   **REST**

[HR REST API](../../../integrate/inbound-rest/concept/hr-core-api.md#)


</td></tr><tr><td>

Instance Scan

</td><td>

-   **Server**
    -   [Findings - Scoped, Global](../../../app-store/dev_portal/API_reference/Findings/concept/FindingsAPI.md#)
    -   [LinterCheckAstNode - Scoped, Global](../../../app-store/dev_portal/API_reference/LinterCheckAstNode/concept/LinterCheckAstNodeAPIBoth.md#)

</td></tr><tr><td>

Integration Hub

</td><td>

-   **Server**

[PersonalAuthAPI - Scoped](../../../app-store/dev_portal/API_reference/PersonalAuthAPI/concept/PersonalAuthAPIScoped.md#)

-   **REST**

[Continuous Integration/Continuous Delivery \(CICD\) API](../../../integrate/inbound-rest/concept/cicd-api.md#)


</td></tr><tr><td>

IT Operations Management

</td><td>

-   **Server**
    -   [Cloud Services Catalog API](../../../integrate/inbound-rest/concept/cs-catalog-api.md#)
    -   [GenericUPSAlarmsReconciler - Global](../../../app-store/dev_portal/API_reference/GenericUPSAlarmsReconciler/concept/c_GenericUPSAlarmsReconcilerAPI.md#)
    -   [GenericUPSBypassReconciler - Global](../../../app-store/dev_portal/API_reference/GenericUPSBypassReconciler/concept/c_GenericUPSBypassReconcilerAPI.md#)
    -   [GenericUPSInputsReconciler - Global](../../../app-store/dev_portal/API_reference/GenericUPSInputsReconciler/concept/c_GenericUPSInputsReconcilerAPI.md#)
    -   [GenericUPSOutputsReconciler - Global](../../../app-store/dev_portal/API_reference/GenericUPSOutputsReconciler/concept/c_GenericUPSOutputsReconcilerAPI.md#)
    -   [LSOFParser - Global](../../../app-store/dev_portal/API_reference/LSOFParser/concept/c_LSOFParserAPI.md#)
    -   [NetwareHandler - Global](../../../app-store/dev_portal/API_reference/NetwareHandler/concept/c_NetwareHandlerAPI.md#)
    -   [ProbeHandlerCim - Global](../../../app-store/dev_portal/API_reference/ProbeHandlerCim/concept/c_ProbeHandlerCimAPI.md#)
    -   [ProbeHandlerMulti - Global](../../../app-store/dev_portal/API_reference/ProbeHandlerMulti/concept/c_ProbeHandlerMultiAPI.md#)
    -   [ProbeHandlerSNMP - Global](../../../app-store/dev_portal/API_reference/ProbeHandlerSNMP/concept/c_ProbeHandlerSNMPAPI.md#)
    -   [ProbeHandlerWMI - Global](../../../app-store/dev_portal/API_reference/ProbeHandlerWMI/concept/c_ProbeHandlerWMIAPI.md#)

</td></tr><tr><td>

IT Service Management

</td><td>

-   **Server**
    -   [CIActionEngine - Scoped](../../../app-store/dev_portal/API_reference/CIAction/concept/CIActionScopedAPI.md#)
    -   [OCRosterSpanApprovalUtil - Global](../../../app-store/dev_portal/API_reference/OCRosterSpanApprovalUtil/concept/c_OCRosterSpanApprovalUtilAPI.md#)
    -   [OCRotation - Global](../../../app-store/dev_portal/API_reference/OCRotation/Concept/c_OCRotation.md#)
    -   [OCRotationV2 - Global](../../../app-store/dev_portal/API_reference/OCRotationV2/Concept/c_OCRotationV2.md#)
    -   [OCRotaICalendarSNC - Global](../../../app-store/dev_portal/API_reference/OCRotaICalendarSNC/concept/c_OCRotaICalendarSNCAPI.md#)
    -   [OCRotaICalendar - Global](../../../app-store/dev_portal/API_reference/OCRotaICalendar/concept/c_OCRotaICalendarAPI.md)
    -   [OCRotaMember - Global](../../../app-store/dev_portal/API_reference/OCRotaMember/concept/c_OCRotaMemberAPI.md#)
    -   [OnCallContactPreferenceUtil - Global](../../../app-store/dev_portal/API_reference/OnCallContactPreferenceUtil/concept/c_OnCallContactPreferenceUtilAPI.md#)
    -   [OnCallRotation - Global](../../../app-store/dev_portal/API_reference/OnCallRotation/concept/c_OnCallRotationAPI.md#)
    -   [OCSeriesEventGenerator - Global](../../../app-store/dev_portal/API_reference/OCSeriesEventGenerator/concept/c_OCSeriesEventGeneratorAPI.md#)
    -   [OCTimer - Global](../../../app-store/dev_portal/API_reference/OCTimer/concept/c_OCTimerAPI.md#)
    -   [RemedialActionEngine - Scoped](../../../app-store/dev_portal/API_reference/RemedialAction/concept/RemedialActionScopedAPI.md#)
    -   [Proactive Engagement API](../../../integrate/inbound-rest/concept/proactive-engagement-api.md#)

</td></tr><tr><td>

Knowledge Management

</td><td>

-   **REST**

[Knowledge Management REST API](../../../integrate/inbound-rest/concept/knowledge-api.md#)


</td></tr><tr><td>

Lead Management

</td><td>

-   **Server**
    -   [LeadAPIHelperOOB - Scoped](../../../app-store/dev_portal/API_reference/LeadAPIHelperOOB/concept/LeadAPIHelperOOBAPI.md#)
    -   [LeadAPIProcessUtilOOB - Scoped](../../../app-store/dev_portal/API_reference/LeadAPIProcessUtilOOB/concept/LeadAPIProcessUtilOOBAPI.md#)
    -   [LeadAPIValidationUtilOOB - Scoped](../../../app-store/dev_portal/API_reference/LeadAPIValidationUtilOOB/concept/LeadAPIValidationUtilOOBAPI.md#)
-   **REST**

[lead API](../../../integrate/inbound-rest/concept/lead-api.md#)


</td></tr><tr><td>

MetricBase

</td><td>

-   **Server**
    -   [Client - Scoped, Global](../../../app-store/dev_portal/API_reference/ClientScoped/concept/ClientScopedAPI.md#)
    -   [Data - Scoped, Global](../../../app-store/dev_portal/API_reference/DataScoped/concept/DataScopedAPI.md#)
    -   [DataBuilder - Scoped, Global](../../../app-store/dev_portal/API_reference/DataBuilderScoped/concept/DataBuilderScopedAPI.md#)
    -   [MetricInfo - Scoped, Global](../../../app-store/dev_portal/API_reference/MetricInfo/concept/MetricInfoBoth.md#)
    -   [Transformer - Scoped, Global](../../../app-store/dev_portal/API_reference/TransformerScoped/concept/TransformerScopedAPI.md#)
    -   [TransformPart - Scoped, Global](../../../app-store/dev_portal/API_reference/TransformPartScoped/concept/TransformPartScopedAPI.md#)
    -   [TransformResult - Scoped, Global](../../../app-store/dev_portal/API_reference/TransformResultScoped/concept/TransformResultScopedAPI.md#)
-   **REST**

[MetricBase Time Series API](../../../integrate/inbound-rest/concept/Clotho-Time-Series-API.md#)


</td></tr><tr><td>

MID Server

</td><td>

-   **Server**
    -   [AgentMetrics - Global](../../../app-store/dev_portal/API_reference/AgentMetrics/concept/c_AgentMetricsAPI.md#)
    -   [JavascriptProbe - Global](../../../app-store/dev_portal/API_reference/JavascriptProbe/concept/c_JavascriptProbeAPI.md#)
    -   [MIDServer - Global](../../../app-store/dev_portal/API_reference/MIDServer/concept/c_MIDServerAPI.md#)
    -   [MIDServerAjax - Global](../../../app-store/dev_portal/API_reference/MIDServerAjax/concept/c_MIDServerAjaxAPI.md#)
    -   [MIDServerCluster - Global](../../../app-store/dev_portal/API_reference/MIDServerCluster/concept/c_MIDServerClusterAPI.md#)
    -   [MIDServerFileSync - Global](../../../app-store/dev_portal/API_reference/MIDServerFileSync/concept/c_MIDServerFileSyncAPI.md#)
    -   [MIDServerFinder - Global](../../../app-store/dev_portal/API_reference/MIDServerFinder/concept/c_MIDServerFinderAPI.md#)
    -   [MIDServerManage - Global](../../../app-store/dev_portal/API_reference/MIDServerManage/concept/c_MIDServerManageAPI.md#)
    -   [MIDServerSelector - Global](../../../app-store/dev_portal/API_reference/MIDServerSelector/concept/c_MIDServerSelectorAPI.md#)
    -   [MonitorMIDServer - Global](../../../app-store/dev_portal/API_reference/MonitorMIDServer/concept/c_MonitorMIDServerAPI.md#)

</td></tr><tr><td>

Mobile Platform

</td><td>

-   **Client**
    -   [m\_form - Client](../../../app-store/dev_portal/API_reference/m_form/concept/m_formClientAPI.md#)
    -   [MobileScriptIncludeCaller - Client](../../../app-store/dev_portal/API_reference/MobileScriptIncludeCaller/concept/MobileScriptInclCallerClientAPI.md#)

</td></tr><tr><td>

Notifications

</td><td>

-   **Server**

[TemplatePrinter - Scoped](../../../app-store/dev_portal/API_reference/TemplatePrinterScoped/concept/c_TemplatePrinterScopedAPI.md#)

-   **REST**
    -   [Email API](../../../integrate/inbound-rest/concept/email-api.md#)
    -   [Push Installation API](../../../integrate/inbound-rest/concept/pushinstallation-api.md#)

</td></tr><tr><td>

ServiceNow AI Platform

</td><td>

-   **Server**
    -   [AbstractDBObject - Global](../../../app-store/dev_portal/API_reference/AbstractDBObject/concept/c_AbstractDBObject.md#)
    -   [AbstractScriptProcessor - Global](../../../app-store/dev_portal/API_reference/AbstractScriptProcessor/concept/c_AbstractScriptProcessorAPI.md#)
    -   [AbstractTimelineSchedulePage - Global](../../../app-store/dev_portal/API_reference/AbstractTimelineSchedulePage/concept/c_AbstractTimelineSchedulePage.md#)
    -   [action - Scoped, Global](../../../app-store/dev_portal/API_reference/Action/concept/ActionAPIBoth.md#)
    -   [ArrayUtil - Global](../../../app-store/dev_portal/API_reference/ArrayUtil/concept/c_ArrayUtilAPI.md#)
    -   [AssessmentCreation - Global](../../../app-store/dev_portal/API_reference/AssessmentCreation/concept/c_AssessmentCreation.md#)
    -   [AutomationException - Global](../../../app-store/dev_portal/API_reference/AutomationException/concept/c_AutomationException.md#)
    -   [Console - Scoped, Global](../../../app-store/dev_portal/API_reference/Console/concept/ConsoleAPI.md#)
    -   [Conversation - Scoped](../../../app-store/dev_portal/API_reference/Conversation/concept/c_ConversationScopedAPI.md#)
    -   [Conversation Member API](../../../integrate/inbound-rest/concept/conversation-member-api.md#)
    -   [CriteriaEvaluator - Global](../../../app-store/dev_portal/API_reference/CriteriaEvaluator/concept/c_CriteriaEvaluatorAPI.md#)
    -   [CSVParser - Scoped](../../../app-store/dev_portal/API_reference/CSVParserScoped/concept/CSVParserScopedAPI.md#)
    -   [DSCScriptableAPI - Global](../../../app-store/dev_portal/API_reference/DSCScriptableAPI/concept/DSCScriptableAPI.md#)
    -   [DurationCalculator - Global](../../../app-store/dev_portal/API_reference/DurationCalculator/concept/c_DurationCalculatorAPI.md#)
    -   [DynamicSchemaAPI - Global](../../../app-store/dev_portal/API_reference/DynamicSchemaAPI/concept/DynamicSchemaAPI.md#)
    -   [Fetch - Scoped, Global](../../../app-store/dev_portal/API_reference/Fetch/concept/FetchAPI.md#)
    -   [Fetch Headers - Scoped, Global](../../../app-store/dev_portal/API_reference/Fetch/concept/Fetch.HeadersAPI.md#)
    -   [Fetch Response - Scoped,Global](../../../app-store/dev_portal/API_reference/Fetch/concept/Fetch.ResponseAPI.md#)
    -   [Fetch Request - Scoped, Global](../../../app-store/dev_portal/API_reference/Fetch/concept/Fetch.RequestAPI.md#)
    -   [Fetch RequestInit - Scoped, Global](../../../app-store/dev_portal/API_reference/Fetch/concept/Fetch.RequestInitAPI.md#)
    -   [FormInfoHeader - Global](../../../app-store/dev_portal/API_reference/FormInfoHeader/concept/c_FormInfoHeaderAPI.md#)
    -   [GeniusResultAnswer - Scoped](../../../app-store/dev_portal/API_reference/GeniusResultAnswerScoped/concept/GeniusResultAnswerScopedAPI.md#)
    -   [GeniusResultContext - Scoped](../../../app-store/dev_portal/API_reference/GeniusResultContextScoped/concept/GeniusResultContextScopedAPI.md#)
    -   [GSLog - Scoped, Global](../../../app-store/dev_portal/API_reference/GSLogBoth/concept/GSLogBoth.md#)
    -   [GlideDynamicAttributeStore - Global](../../../app-store/dev_portal/API_reference/GlideDynamicAttributeStore/concept/GlideDynamicAttStoreAPI.md#)
    -   [GlideElementDynamicAttributeStore - Global](../../../app-store/dev_portal/API_reference/GlideElementDynamicAttributeStore/concept/GlideElementDynamicAttStoreAPI.md#)
    -   [HistoryWalker - Scoped, Global](../../../app-store/dev_portal/API_reference/HistoryWalkerScoped/concept/HistoryWalkerScopedAPI.md#)
    -   [HostnameJS - Global](../../../app-store/dev_portal/API_reference/HostnameJS/concept/c_HostnameJSAPI.md#)
    -   [HttpRequestData - Scoped](../../../app-store/dev_portal/API_reference/HttpRequestData/concept/HttpRequestDataAPI.md#)
    -   [HttpRequestAuthedData - Scoped](../../../app-store/dev_portal/API_reference/HttpRequestAuthedData/concept/HttpRequestAuthedDataAPI.md#)
    -   [ICalUtilSNC - Global](../../../app-store/dev_portal/API_reference/ICalUtilSNC/concept/c_ICalUtilSNCAPI.md#)
    -   [Interaction - Scoped](../../../app-store/dev_portal/API_reference/Interaction/concept/InteractionScopedAPI.md#)
    -   [j2js - Global](../../../app-store/dev_portal/API_reference/j2js/concept/c_J2jsAPI.md#)
    -   [JSON - Global](../../../app-store/dev_portal/API_reference/JSON/concept/c_JSONAPI.md#)
    -   [JSON - Scoped](../../../app-store/dev_portal/API_reference/JSONScoped/concept/JSONScopedAPI.md#)
    -   [JSONParser - Global \(deprecated\)](../../../app-store/dev_portal/API_reference/JSONParser/concept/c_JSONParserAPI.md#)
    -   [Messaging - Scoped](../../../app-store/dev_portal/API_reference/Messaging/concept/MessagingScopedAPI.md#)
    -   [MobileDeepLinkGenerator - Global](../../../app-store/dev_portal/API_reference/MobileDeepLinkGenerator/concept/MobileDeepLinkGeneratorAPI.md#)
    -   [NameValuePairs - Global](../../../app-store/dev_portal/API_reference/NameValuePairs/concept/c_NameValuePairsAPI.md#)
    -   [Notify - Global](../../../app-store/dev_portal/API_reference/Notify/concept/c_NotifyAPI.md#)
    -   [NotifyScoped - Scoped](../../../app-store/dev_portal/API_reference/NotifyScoped/concept/notifyScopedAPI.md#)
    -   [NotifyAction - Global](../../../app-store/dev_portal/API_reference/NotifyAction/concept/c_NotifyActionApi.md#)
    -   [NotifyConferenceUtil - Scoped, Global](../../../app-store/dev_portal/API_reference/NotifyConferenceUtils/concept/NotifyConferenceUtils.md#)
    -   [OrderGuide - Scoped](../../../app-store/dev_portal/API_reference/OrderGuideScoped/concept/OrderGuideScopedAPI.md#)
    -   [PreferenceDestination - Scoped, Global](../../../app-store/dev_portal/API_reference/PreferenceDestination/concept/PreferenceDestinationBothAPI.md#)
    -   [Preferences - Scoped, Global](../../../app-store/dev_portal/API_reference/Preferences/concept/PreferencesBothAPI.md#)
    -   [RecordToHTML - Global](../../../app-store/dev_portal/API_reference/RecordToHTML/concept/c_RecordToHTMLAPI.md#)
    -   [Omnichannel Callback API](../../../integrate/inbound-rest/concept/omichannel-callback-api.md#)
    -   [RenderProperties - Global](../../../app-store/dev_portal/API_reference/RenderProperties/concept/RenderProperties-API.md#)
    -   [RenderProperties - Scoped](../../../app-store/dev_portal/API_reference/RenderPropertiesScoped/concept/RenderProperties-Scoped-API.md#)
    -   [RequestAuthAPI - Scoped](../../../app-store/dev_portal/API_reference/RequestAuthAPI/concept/RequestAuthAPI.md#)
    -   [../../../Chunk2057639958.md\#](../../../Chunk2057639958.md#)
    -   [../../../Chunk2057639958.md\#](../../../Chunk2057639958.md#)
    -   [RESTAPIRequestBody - Scoped, Global](../../../app-store/dev_portal/API_reference/ScriptableServiceRequestBody/concept/c_ScriptableServiceRequestBody.md#)
    -   [RESTAPIResponse - Scoped, Global](../../../app-store/dev_portal/API_reference/ScriptableServiceResponseBuilder/concept/c_ScriptableServiceResponseBuilder.md#)
    -   [RESTAPIResponseStream - Scoped, Global](../../../app-store/dev_portal/API_reference/ScriptableServiceResponseStreamWriter/concept/c_ScriptableServiceRespStreamWriter.md#)
    -   [RESTMessageV2 - Scoped, Global](../../../app-store/dev_portal/API_reference/RESTMessageV2/concept/c_RESTMessageV2API.md#)
    -   [RESTResponseV2 - Scoped, Global](../../../app-store/dev_portal/API_reference/RESTResponseV2/concept/c_RESTResponseV2API.md#)
    -   [RTETransformer - Scoped](../../../app-store/dev_portal/API_reference/RTETransformer/concept/RTETransScopedAPI.md#)
    -   [ScopedCacheManager - Scoped](../../../app-store/dev_portal/API_reference/ScopedCacheManager/concept/ScopedCacheManagerAPI.md#)
    -   [v\_record - Scoped, Global](../../../app-store/dev_portal/API_reference/v_record/concept/v_recordAPI.md#)
    -   [SentimentAnalyser - Scoped](../../../app-store/dev_portal/API_reference/SentimentAnalyserScoped/concept/SentimentAnalyserScoped.md#)
    -   [SOAPMessageV2 - Scoped, Global](../../../app-store/dev_portal/API_reference/SOAPMessageV2/concept/c_SOAPMessageV2API.md#)
    -   [SOAPResponseV2 - Scoped, Global](../../../app-store/dev_portal/API_reference/SOAPResponseV2/concept/c_SOAPResponseV2API.md#)
    -   [Stream - Scoped, Global](../../../app-store/dev_portal/API_reference/Stream/concept/StreamGlobalAPI.md#)
    -   [SummaryTableWriter - Global](../../../app-store/dev_portal/API_reference/SummaryTableWriterScriptInclude/concept/c_SummaryTableWriter.md#)
    -   [TableUtils - Global](../../../app-store/dev_portal/API_reference/TableUtils/concept/c_TableUtilsAPI.md#)
    -   [TaskStateUtil - Global](../../../app-store/dev_portal/API_reference/TaskStateUtil/concept/c_TaskStateUtil.md#)
    -   [TimelineSpan - Global](../../../app-store/dev_portal/API_reference/TimelineSpan/context/c_TimelineSpan.md#)
    -   [Transformer - Scoped, Global](../../../app-store/dev_portal/API_reference/TransformerScripted/concept/TransformerScriptedAPI.md#)
    -   [TransformerDefinition - Scoped, Global](../../../app-store/dev_portal/API_reference/TransformerDefinition/concept/TransformerDefinitionAPI.md#)
    -   [TransformerRuleList - Scoped, Global](../../../app-store/dev_portal/API_reference/TransformerRuleList/concept/TransformerRuleListAPI.md#)
    -   [UserCriteria - Scoped](../../../app-store/dev_portal/API_reference/UserCriteriaScoped/concept/c_UserCriteriaScoped.md#)
    -   [v\_query – Scoped, Global](../../../app-store/dev_portal/API_reference/v_query/concept/v_queryAPI.md#)
    -   [v\_record - Scoped, Global](../../../app-store/dev_portal/API_reference/v_record/concept/v_recordAPI.md#)
    -   [v\_table – Scoped, Global](../../../app-store/dev_portal/API_reference/v_table/concept/v_tableAPI.md#)
    -   [VoiceTranscriptObject - Scoped](../../../app-store/dev_portal/API_reference/VoiceTranscriptObjectScoped/concept/VoiceTranscriptObjectScopedAPI.md#)
    -   [XMLDocument2 - Scoped, Global](../../../app-store/dev_portal/API_reference/XMLDocument2ScopedAPI/concept/c_XMLDocument2ScopedAPI.md#)
    -   [XMLNode - Scoped, Global](../../../app-store/dev_portal/API_reference/XMLNodeScopedAPI/concept/c_XMLNodeScopedAPI.md#)
    -   [XMLNodeIterator - Scoped](../../../app-store/dev_portal/API_reference/XMLNodeIteratorScopedAPI/concept/c_XMLNodeIteratorScopedAPI.md#)
    -   [AuthCredential - Scoped](../../../app-store/dev_portal/API_reference/AuthCredential/concept/AuthCredentialAPI.md#) Only available within the `sn_auth` namespace.
-   **REST**
    -   [Aggregate API](../../../integrate/inbound-rest/concept/c_AggregateAPI.md#)
    -   [Attachment API](../../../integrate/inbound-rest/concept/c_AttachmentAPI.md#)
    -   [Batch API](../../../integrate/inbound-rest/concept/batch-api.md#)
    -   [Import Set API](../../../integrate/inbound-rest/concept/c_ImportSetAPI.md#)
    -   [Response Templates API](../../../integrate/inbound-rest/concept/response-templates-api.md#)
    -   [Sales Agreement API](../../../integrate/inbound-rest/concept/sales_agreement-api.md#)
    -   [Script Debugger API](../../../integrate/inbound-rest/concept/scriptdebugger-api.md#)
    -   [Table API](../../../integrate/inbound-rest/concept/c_TableAPI.md#)
-   **Client**
    -   [g\_service\_catalog - Client](../../../app-store/dev_portal/API_reference/g_service_catalog/concept/g_service_catalogClientAPI.md#)
    -   [Guided Tours - Client](../../../app-store/dev_portal/API_reference/guided_tours/concept/guided_toursAPI.md#)
    -   [NotifyClient - Client](../../../app-store/dev_portal/API_reference/Notify2WebRTCClient/concept/c_Notify2WebRTCClient.md#)
    -   [NotifyOnTaskClient - Client](../../../app-store/dev_portal/API_reference/NotifyOnTaskClient/concept/NotifyOnTaskClient.md#)
    -   [ScriptLoader - Client](../../../app-store/dev_portal/API_reference/ScriptLoader/concept/c_ScriptLoaderAPI.md#)

</td></tr><tr><td>

ServiceNow AI Platform Legacy Capabilities

</td><td>

-   **Server**
    -   [ConnectActionResponse - Global](../../../app-store/dev_portal/API_reference/ConnectActionResponse/concept/c_ConnectActionResponseAPI.md#)
    -   [GlideConversation - Global](../../../app-store/dev_portal/API_reference/GlideConversation/concept/c_GlideConversationAPI.md#)

</td></tr><tr><td>

ServiceNow AI Platform - Security

</td><td>

-   **Server**
    -   [OAuthUtil - Global](../../../app-store/dev_portal/API_reference/OAuthUtil/concept/c_OAuthUtilScriptInclude.md#)
    -   [SCIM2Client - Scoped](../../../app-store/dev_portal/API_reference/SCIM2Client/concept/SCIM2ClientAPI.md#)
    -   [SCIM2ClientUtil - Scoped](../../../app-store/dev_portal/API_reference/SCIM2ClientUtil/concept/SCIM2ClientUtilAPI.md#)
    -   [StandardCredentialsProvider - Scoped, Global](../../../app-store/dev_portal/API_reference/StardardCredentialsProvider/Concept/standard-credentials-provider-api.md#)
    -   [CertificateEncryption - Scoped](../../../app-store/dev_portal/API_reference/CertificateEncryptionScoped/concept/c_CertificateEncryptionScopedAPI.md#)
    -   [ConnectionInfo - Scoped, Global](../../../app-store/dev_portal/API_reference/ConnectionInfo/Concept/connection-info-api.md#)
    -   [ConnectionInfoProvider - Scoped, Global](../../../app-store/dev_portal/API_reference/ConnectionInfoProvider/Concept/connection-info-provider-api.md#)
    -   [KMFCryptoOperation - Scoped, Global](../../../app-store/dev_portal/API_reference/KMFCryptoOperationBoth/concept/KMFCryptoOperationBothAPI.md#)
    -   [DCManager - Global](../../../app-store/dev_portal/API_reference/DCManager/concept/DCManagerAPIGlobal.md#)
    -   [ScopedDCManager - Scoped](../../../app-store/dev_portal/API_reference/DCManagerScoped/concept/DCManagerAPIScoped.md#)
-   **REST**
    -   [Data Classification API](../../../integrate/inbound-rest/concept/data-classification-api.md#)
    -   [System for Cross-domain Identity Management \(SCIM\) API](../../../integrate/inbound-rest/concept/scim-api.md#)
    -   [User Role Inheritance API](../../../integrate/inbound-rest/concept/user-role-inheritance-api.md#)
-   **Client**

[ScopedSessionDomain - Client](../../../app-store/dev_portal/API_reference/ScopedSessionDomain/concept/ScopedSessionDomainAPI.md#)


</td></tr><tr><td>

Order Management for Telecommunications, Media, and Technology

</td><td>

-   **Server**
    -   [EventProcessorUtilOOB - Scoped](../../../app-store/dev_portal/API_reference/EventProcessorUtilOOB/concept/EventProcessorUtilOOBScopedAPI.md#)
    -   [EventQueueProcessorOOB - Scoped](../../../app-store/dev_portal/API_reference/EventQueueProcessorOOB/concept/EventQueueProcessorOOBScopedAPI.md#)
    -   [HermesEventPublisherOOB - Scoped](../../../app-store/dev_portal/API_reference/HermesEventPublisherOOB/concept/HermesEventPublishOOBScopedAPI.md#)
    -   [OpenMessageBusEventPublisherOOB - Scoped](../../../app-store/dev_portal/API_reference/OpenMessageBusEventPublisherOOB/concept/OpenMsgBusEvtPubScopedAPI.md#)
    -   [TMFTopicEventAPIUtilOOB - Scoped](../../../app-store/dev_portal/API_reference/TMFTopicEventAPIUtilOOB/concept/tmftopiceventapiutiloobScopedAPI.md#)
    -   [TopicAPIUtilsOOB - Scoped](../../../app-store/dev_portal/API_reference/TopicAPIUtilsOOB/concept/TopicAPIUtilsOOBAPIScoped.md#)
    -   [TopicSubscriptionUtilOOB - Scoped](../../../app-store/dev_portal/API_reference/TopicSubscriptionUtilOOB/concept/TopicSubscriptionUtilAPIScoped.md#)
    -   [TopicUtilOOB - Scoped](../../../app-store/dev_portal/API_reference/TopicUtilOOB/concept/TopicUtilOOBAPIScoped.md#)
    -   [TroubleTicketNotificationUtilOOB - Scoped](../../../app-store/dev_portal/API_reference/TroubleTicketNotificationUtilOOB/concept/TroubleTicketNotifScopedAPI.md#)
-   **REST**
    -   [Alarm Management Open API](../../../integrate/inbound-rest/concept/alarm-open-api.md#)
    -   [Event Notification Management Open API](../../../integrate/inbound-rest/concept/event_open-api.md#)
    -   [Product Catalog Open API](../../../integrate/inbound-rest/concept/product-catalog-open-api.md#)
    -   [Product Inventory Open API](../../../integrate/inbound-rest/concept/product-inventory-open-api.md#)
    -   [Product Order Open API](../../../integrate/inbound-rest/concept/tmf622_product_ordering-api.md#)
    -   [Service Catalog Open API](../../../integrate/inbound-rest/concept/service-catalog-open-api.md#)
    -   [Service Order Open API](../../../integrate/inbound-rest/concept/service-order-open-api.md#)
    -   [Service Test Management Open API](../../../integrate/inbound-rest/concept/service-test-management-api.md#)
    -   [Technical Service Qualification Open API](../../../integrate/inbound-rest/concept/ts-qualification-api.md#)
    -   [Trouble Ticket Open API](../../../integrate/inbound-rest/concept/trouble-ticket-open-api.md#)

</td></tr><tr><td>

Performance Analytics

</td><td>

-   **Server**
    -   [PADomainUtils - Global](../../../app-store/dev_portal/API_reference/PADomainUtils/concept/c_PADomainUtils.md#)
    -   [PAScorecard - Scoped](../../../app-store/dev_portal/API_reference/PAScorecard/concept/PAScorecard.md#)
    -   [PASnapshot - Scoped](../../../app-store/dev_portal/API_reference/PASnapshot/concept/PASnapshot.md#)
-   **REST**

[Scorecards API](../../../integrate/inbound-rest/concept/c_PerformanceAnalyticsAPI.md#)


</td></tr><tr><td>

Predictive Intelligence

</td><td>

-   **Server**
    -   [ClassificationSolution - Global](../../../app-store/dev_portal/API_reference/ClassificationSolution/concept/ClassificationSolutionAPI.md#)
    -   [ClassificationSolutionStore - Global](../../../app-store/dev_portal/API_reference/ClassificationSolutionStore/concept/ClassificationSolutionStoreAPI.md#)
    -   [ClassificationSolutionVersion - Global](../../../app-store/dev_portal/API_reference/ClassificationSolutionVersion/concept/ClassificationSolutionVersionAPI.md#)
    -   [ClusteringSolution - Global](../../../app-store/dev_portal/API_reference/ClusteringSolution/concept/ClusteringSolutionAPI.md#)
    -   [ClusteringSolutionStore - Global](../../../app-store/dev_portal/API_reference/ClusteringSolutionStore/concept/ClusteringSolutionStoreAPI.md#)
    -   [ClusteringSolutionVersion - Global](../../../app-store/dev_portal/API_reference/ClusteringSolutionVersion/concept/ClusteringSolutionVersionAPI.md#)
    -   [DatasetDefinition - Global](../../../app-store/dev_portal/API_reference/DatasetDefinition/concept/DatasetDefinitionAPI.md#)
    -   [Encoder - Global](../../../app-store/dev_portal/API_reference/Encoder/concept/EncoderAPI.md#)
    -   [EncoderStore - Global](../../../app-store/dev_portal/API_reference/EncoderStore/concept/EncoderStoreAPI.md#)
    -   [EncoderVersion - Global](../../../app-store/dev_portal/API_reference/EncoderVersion/concept/EncoderVersionAPI.md#)
    -   [MLPredictor - Global \(deprecated\)](../../../app-store/dev_portal/API_reference/MLPredictor/concept/c_MLPredictorAPI.md#)
    -   [MLSolution - Global](../../../app-store/dev_portal/API_reference/MLSolution/concept/MLSolutionAPI.md#)
    -   [MLSolutionFactory - Global](../../../app-store/dev_portal/API_reference/MLSolutionFactory/concept/MLSolutionFactoryAPI.md#)
    -   [MLSolutionResult - Global \(deprecated\)](../../../app-store/dev_portal/API_reference/MLSolutionResult/concept/MLSolutionResultAPI.md#)
    -   [MLSolutionUtil - Global](../../../app-store/dev_portal/API_reference/MLSolutionUtil/concept/MLSolutionUtilAPI.md#)
    -   [PredictabilityEstimate - Global](../../../app-store/dev_portal/API_reference/PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#)
    -   [PredictabilityEstimateStore - Global](../../../app-store/dev_portal/API_reference/PredictabilityEstimateStore/concept/PredictabilityEstimateStoreAPI.md#)
    -   [PredictabilityEstimateVersion - Global](../../../app-store/dev_portal/API_reference/PredictabilityEstimateVersion/concept/PredictabilityEstimateVersionAPI.md#)
    -   [RegressionSolution - Global](../../../app-store/dev_portal/API_reference/RegressionSolution/concept/RegressionSolutionAPI.md#)
    -   [RegressionSolutionStore - Global](../../../app-store/dev_portal/API_reference/RegressionSolutionStore/concept/RegressionSolutionStoreAPI.md#)
    -   [RegressionSolutionVersion - Global](../../../app-store/dev_portal/API_reference/RegressionSolutionVersion/concept/RegressionSolutionVersionAPI.md#)
    -   [SimilaritySolution - Global](../../../app-store/dev_portal/API_reference/SimilaritySolution/concept/SimilaritySolutionAPI.md#)
    -   [SimilaritySolutionStore - Global](../../../app-store/dev_portal/API_reference/SimilaritySolutionStore/concept/SimilaritySolutionStoreAPI.md#)
    -   [SimilaritySolutionVersion - Global](../../../app-store/dev_portal/API_reference/SimilaritySolutionVersion/concept/SimilaritySolutionVersionAPI.md#)
-   **REST**

[Predictive Intelligence API](../../../integrate/inbound-rest/concept/agent-intelligence-api.md#)


</td></tr><tr><td>

Proactive Triggers

</td><td>

-   **Server**

[ProactiveTriggerAPI - Scoped](../../../app-store/dev_portal/API_reference/ProactiveTriggerAPI/concept/ProactiveTriggerScopedAPI.md#)


</td></tr><tr><td>

Sourcing and Procurement Operations

</td><td>

-   **REST**

[SpendInt APIs](../../../integrate/inbound-rest/concept/spendint-api.md#)


</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   **Server**

[CostPlanBatchOperations - Global](../../../app-store/dev_portal/API_reference/CostPlanBatchOperations/concept/CostPlanBatchOperationsAPI.md#)

-   **REST**

[Project Portfolio Management API](../../../integrate/inbound-rest/concept/ppm-api.md#)


</td></tr><tr><td>

Sales Agreement Management

</td><td>

-   **REST**

[Sales Agreement API](../../../integrate/inbound-rest/concept/sales_agreement-api.md#)


</td></tr><tr><td>

Security Operations

</td><td>

-   **REST**

[TISC API](../../../integrate/inbound-rest/concept/tisc-api.md#)


</td></tr><tr><td>

Service Exchange

</td><td>

-   **Server**

[CSBScratchpadUtil - Scoped](../../../app-store/dev_portal/API_reference/CSBScratchpadUtil/concept/CSBScratchpadUtilScopedAPI.md#)

[sb - Scoped, Global](../../../app-store/dev_portal/API_reference/PSBPublicAPIUtil/concept/PSBPublicAPIUtilBoth.md#)

[PSBScratchpadUtil - Scoped](../../../app-store/dev_portal/API_reference/PSBScratchpadUtil/concept/PSBScratchpadUtilScopedAPI.md#)


</td></tr><tr><td>

Service Catalog

</td><td>

-   **Server**
    -   [CatalogClientScript - Scoped](../../../app-store/dev_portal/API_reference/CatalogClientScriptScoped/concept/c_CatalogClientScriptScoped.md#)
    -   [CatalogItemVariable - Scoped](../../../app-store/dev_portal/API_reference/CatalogItemVariable/concept/c_CatalogItemVariable.md#)
    -   [CatalogItemVariableSet - Scoped](../../../app-store/dev_portal/API_reference/CatalogItemVariableSet/concept/c_CatalogItemVariableSet.md#)
    -   [CatalogItemVariableSetM2M - Scoped](../../../app-store/dev_portal/API_reference/CatalogItemVariableSetM2M/concept/c_CatalogItemVariableSetM2M.md#)
    -   [CatalogJS - Scoped](../../../app-store/dev_portal/API_reference/CatalogJS/concept/CatalogJSScopedAPI.md#)
    -   [CatalogSearch - Scoped](../../../app-store/dev_portal/API_reference/CatalogSearchScoped/concept/c_CatalogSearchScoped.md#)
    -   [CatCategory - Scoped](../../../app-store/dev_portal/API_reference/CatCategory/concept/c_CatCategory.md#)
    -   [CatItem - Scoped](../../../app-store/dev_portal/API_reference/CatItem/concept/c_CatItem.md#)
    -   [CartJS - Scoped](../../../app-store/dev_portal/API_reference/CartJSScoped/concept/c_CartJSScoped.md#)
-   **REST**

[Service Catalog API](../../../integrate/inbound-rest/concept/c_ServiceCatalogAPI.md#)


</td></tr><tr><td>

Service Level Management

</td><td>

-   **Server**

[SLARepair - Global](../../../app-store/dev_portal/API_reference/SLARebuilder/concept/c_SLARepair.md#)


</td></tr><tr><td>

Service Mapping

</td><td>

-   **Server**

[BusinessServiceManager - Global](../../../app-store/dev_portal/API_reference/BusinessServiceManager/concept/BusinessServiceManagerAPI.md#)


</td></tr><tr><td>

ServiceNow Voice

</td><td>

-   **REST**
    -   [CTI API](../../../integrate/inbound-rest/concept/cti-api.md#)
    -   [CTIOperationRequest - Scoped, Global](../../../app-store/dev_portal/API_reference/CTIOperationRequest/concept/CTIOperationRequestAPI.md#)
    -   [CTIOperationResponse - Scoped, Global](../../../app-store/dev_portal/API_reference/CTIOperationResponse/concept/CTIOperationResponseAPI.md#)

</td></tr><tr><td>

Service Portal

</td><td>

-   **Server**
    -   [GlideSPScriptable - Scoped](../../../app-store/dev_portal/API_reference/GlideSPScriptableScoped/concept/c_GlideSPScriptableScopedAPI.md#)
    -   [GlideSPSearchAnalytics - Global](../../../app-store/dev_portal/API_reference/GlideSPSearchAnalytics/concept/GlideSPSearchAnalyticsAPI.md#)
    -   [GlideSPUtil - Global](../../../app-store/dev_portal/API_reference/GlideSPUtil/concept/GlideSPUtilAPI.md#)
    -   [SPScriptedFacet - Scoped](../../../app-store/dev_portal/API_reference/SPScriptedFacet/concept/SPScriptedFacetScopedAPI.md#)
    -   [SPScriptedFacetService - Scoped](../../../app-store/dev_portal/API_reference/SPScriptedFacetService/concept/SPScriptedFacetServiceScopedAPI.md#)
    -   [SPSEOUtilsSNC - Global](../../../app-store/dev_portal/API_reference/SPSEOUtilsSNC/concept/SPSEOUtilsSNCAPI.md#)
    -   [SPWidgetAccessControl - Global](../../../app-store/dev_portal/API_reference/SPWidgetAccessControlGlobal/concept/SPWidgetAccessControlGlobalAPI.md#)
-   **Client**
    -   [spAriaUtil](../../../app-store/dev_portal/API_reference/spAriaUtil/concept/spAriaUtil-API.md#)
    -   [spContextManager](../../../app-store/dev_portal/API_reference/spContextManager/concept/spContextManagerAPI.md#)
    -   [spModal](../../../app-store/dev_portal/API_reference/SPModal/concept/SPModal-API.md#)
    -   [spUtil - Client](../../../app-store/dev_portal/API_reference/spUtil/concept/spUtilAPI.md#)
    -   [SNAnalytics - Client](../../../app-store/dev_portal/API_reference/SNAnalytics/concept/SNAnalyticsClientAPI.md#)

</td></tr><tr><td>

Skills Management

</td><td>

-   **Server**
    -   [SkillDeterminationUtils - Scoped](../../../app-store/dev_portal/API_reference/SkillDeterminationUtils/concept/SkillDeterminationUtilsAPI.md#)
    -   [UserSkillAnalyzer - Global](../../../app-store/dev_portal/API_reference/UserSkillAnalyzer/concept/UserSkillAnalyzerAPI.md#)
    -   [UserSkillRanking - Global](../../../app-store/dev_portal/API_reference/UserSkillRanking/concept/UserSkillRankingAPI.md#)

</td></tr><tr><td>

Software Asset Management

</td><td>

-   **REST**

[SAM-Software Usage Data Integration API](../../../integrate/inbound-rest/concept/sam_soft_us_int-api.md#)


</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

-   **REST**

[Resource Inventory Open API](../../../integrate/inbound-rest/concept/resource-inventory-api.md#)


</td></tr><tr><td>

UI Builder

</td><td>

-   **Client**
    -   [api - UI Builder](../../../app-store/dev_portal/API_reference/api/concept/apiAPI.md#)
    -   [DecisionTableAPI - Scoped, Global](../../../app-store/dev_portal/API_reference/DecisionTableAPI/concept/DecisionTableAPI.md#)
    -   [helpers - UI Builder](../../../app-store/dev_portal/API_reference/helpers/concept/helpersAPI.md#)
    -   [PlaybookExperience - Scoped](../../../app-store/dev_portal/API_reference/PlaybookExperienceScoped/concept/PlaybookExperienceScopedAPI.md#)

</td></tr><tr><td>

Universal Request

</td><td>

-   **Server**

[UniversalRequestUtilsSNC - Scoped](../../../app-store/dev_portal/API_reference/UniversalRequestUtilsSNC/concept/UniversalRequestUtilsSNCScopedAPI.md#)


</td></tr><tr><td>

Universal Task

</td><td>

-   **Server**

[UniversalTaskUtils - Scoped, Global](../../../app-store/dev_portal/API_reference/UniversalTaskUtils/concept/UniversalTaskUtilsBothAPI.md#)


</td></tr><tr><td>

Virtual Agent

</td><td>

-   **REST**
    -   [CCCIF Media Resource API](../../../integrate/inbound-rest/concept/cccif-api.md#)
    -   [Virtual Agent Bot Integration API](../../../integrate/inbound-rest/concept/bot-api.md#)
    -   [Voice Interaction Resource API](../../../integrate/inbound-rest/concept/voice-interaction-resource-api.md#)
    -   [Omnichannel Callback API](../../../integrate/inbound-rest/concept/omichannel-callback-api.md#)
-   **Server**

[ProactiveTriggerAPI - Scoped](../../../app-store/dev_portal/API_reference/ProactiveTriggerAPI/concept/ProactiveTriggerScopedAPI.md#)


</td></tr><tr><td>

Workflow \(legacy\)

</td><td>

-   **Server**
    -   [WalkWorkflow - Global](../../../app-store/dev_portal/API_reference/Walkworkflow/concept/c_WalkWorkflowAPI.md#)
    -   [WFActivityHandler - Global](../../../app-store/dev_portal/API_reference/WFACtivityHandler/concept/c_WFACtivityHandlerAPI.md#)
    -   [Workflow - Global](../../../app-store/dev_portal/API_reference/Workflow/concept/c_Workflow_api.md#)
    -   [Workflow - Scoped](../../../app-store/dev_portal/API_reference/WorkflowScoped/concept/c_WorkflowScopedAPI.md#)
    -   [WorkflowDuration - Global](../../../app-store/dev_portal/API_reference/WorkflowDuration/concept/c_WorkflowDurationAPI.md#)
    -   [WorkflowModelManager - Global](../../../app-store/dev_portal/API_reference/WorkflowModelManager/context/c_WorkflowModelManagerAPI.md#)
    -   [WorkflowModelManagerAjax - Global](../../../app-store/dev_portal/API_reference/WorkflowModelManagerAjax/concept/c_WorkflowModelManagerAjaxAPI.md#)
    -   [WorkflowScheduler - Global](../../../app-store/dev_portal/API_reference/WorkflowScheduler/concept/c_WorkflowSchedulerAPI.md#)
    -   [WorkflowTimeline - Global](../../../app-store/dev_portal/API_reference/WorkflowTimeLine/concept/c_WorkflowTimelineAPI.md#)

</td></tr><tr><td>

Workplace Service Delivery

</td><td>

-   **REST**
    -   [Workplace Connector Webhook API](../../../integrate/inbound-rest/concept/workplace_connector_webhook-api.md#)
    -   [WSD Extra Service Request API](../../../integrate/inbound-rest/concept/wsd_extra_serv_req-api.md#)
    -   [WSD Extra Service API](../../../integrate/inbound-rest/concept/wsd_extra_service-api.md#)
    -   [WSD Group Reservation API](../../../integrate/inbound-rest/concept/wsd_grp_reserv-api.md#)
    -   [WSD Multi Reservation API](../../../integrate/inbound-rest/concept/wsd_multi_reserv-api.md#)
    -   [WSD Recurring Reservation API](../../../integrate/inbound-rest/concept/wsd_recur_reserv-api.md#)
    -   [WSD Reservable API](../../../integrate/inbound-rest/concept/wsd_reservable-api.md#)
    -   [WSD Reservation API](../../../integrate/inbound-rest/concept/wsd_reservation-api.md#)
    -   [WSD Reservation Invitees API](../../../integrate/inbound-rest/concept/wsd_reservation_invitees-api.md#)
    -   [WSD Search API](../../../integrate/inbound-rest/concept/wsd_search-api.md#)
    -   [WSD Shift API](../../../integrate/inbound-rest/concept/wsd_shift-api.md#)

</td></tr></tbody>
</table>