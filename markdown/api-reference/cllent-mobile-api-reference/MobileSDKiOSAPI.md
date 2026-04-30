---
title: Mobile SDK API reference - iOS
description: The Mobile SDK for iOS provides the classes necessary to interface iOS-based devices with the ServiceNow platform.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Mobile SDK API reference, API reference, API implementation and reference]
---

# Mobile SDK API reference - iOS

The Mobile SDK for iOS provides the classes necessary to interface iOS-based devices with the ServiceNow platform.

It provides classes that enable you to create feature services such as chat, REST API interface, GraphQL, and web access, that allow you to create interactive applications on any iOS device.

For additional information on how to implement specific use cases using this API, see the [Mobile SDK Developer Guide - iOS](../../../../../integrate/guides/mobile_sdk/mobile_sdk-ios/concept/mobsdk-ios-overview.md).

<table id="table_qgj_tg2_vpb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="mobile_SDK_ios-NowAttachmentMetadata_State"><td>

NowAttachmentMetadata.State

</td><td>

Attachment metadata state.Possible values:

-   available
-   conditionally
-   none
-   pending
-   unavailable

</td></tr><tr id="mobile_SDK_ios-NowSDKError"><td>

NowSDKError

</td><td>

Errors that can be thrown from the NowSDK module.Values

-   configurationError
-   missingAuthorizationProvider
-   missingPermissionDelegate

</td></tr></tbody>
</table>-   **[FetchConfiguration structure - iOS](../FetchConfiguration/concept/FetchConfigiOSStructure.md#)**  
The FetchConfiguration structure provides the ability to define the configuration for fetching records from your ServiceNow instance.
-   **[FieldReadConfiguration structure - iOS](../FieldReadConfiguration/concept/FieldReadConfigurationiOSStruct.md#)**  
The FieldReadConfiguration structure enables you to configure which fields to fetch from a ServiceNow instance table and in which format.
-   **[FieldWriteOptions class - iOS](../FieldWriteOptions/concept/FieldWriteOptionsiOSStruct.md#)**  
The FieldWriteOptions class provides functions that set the options for updating or creating fields in a record on a ServiceNow instance.
-   **[Filter structure - iOS](../Filter/concept/FilteriOSStructure.md#)**  
The Filter structure provides the ability to configure filters that define the data to return in the return results of a REST endpoint query.
-   **[NowAnalyticsService protocol - iOS](../NowAnalyticsService/concept/NowAnalyticsServiceiOSProtocol.md#)**  
The NowAnalyticsService protocol provides functions that enable you to configure analytics properties, user settings, and events for managing the collection of user analytics data.
-   **[NowAnalyticsServiceDelegate protocol - iOS](../NowAnalyticsServiceDelegate/concept/NowAnalyticsServiceDeliOSProtocol.md#)**  
The NowAnalyticsServiceDelegate protocol provides callback functions that provide information about the starting and ending of a user session and screen change detection.
-   **[NowAPIEndpoint protocol - iOS](../NowAPIEndpoint/concept/NowAPIEndpointiOSProtocol.md#)**  
The NowAPIEndpoint protocol provides an interface for accessing any publicly exposed ServiceNow REST APIs.
-   **[NowAPIService class - iOS](../NowAPIService/concept/NowAPIServiceiOSAPI.md#)**  
The NowAPIService class provides functions that enable you to perform requests to a specified ServiceNow REST API.
-   **[NowAttachment structure - iOS](../NowAttachment/concept/NowAttachmentiOSStructure.md#)**  
The NowAttachment structure provides functions that enable you to validate attachments by comparing their computed hash.
-   **[NowAttachmentMetadata structure - iOS](../NowAttachmentMetadata/concept/NowAttachmentMetadataiOSStructure.md#)**  
The NowAttachmentMetadata structure provides functions that enable you to encode and manage attachment metadata.
-   **[NowAttachmentService class - iOS](../NowAttachmentService/concept/NowAttachmentServiceiOSAPI.md#)**  
The NowAttachmentService class provides functions that enable you to upload and query attachments that are associated with records within a table on a ServiceNow instance.
-   **[NowAttachmentUploadConfiguration structure - iOS](../NowAttachmentUploadConfiguration/concept/NowAttachUploadConfigiOSStruct.md#)**  
The NowAttachmentUploadConfiguration structure enables you to define the configuration information for an attachment that you are uploading to your ServiceNow instance.
-   **[NowChat API - iOS](../NowChat/concept/NowChatiOSAPI.md#)**  
The NowChat API is a top-level global API that enables users to instantiate a NowChat service instance.
-   **[NowChatColoring protocol - iOS](../NowChatColoring/concept/NowChatColoringiOSProtocol.md#)**  
The NowChatColoring protocol defines default colors for the elements in the Live Agent and Virtual Agent chat UI.
-   **[NowChatConfiguration - iOS](../NowChatOptions/concept/NowChatOptionsiOS.md#)**  
The NowChatConfiguration class enables you to configure options on a chat session, such as showing a prompt before closing a chat window, disabling features while using chat, applying different conversation options when using chat, and configuring UI components in NowChat.
-   **[NowChatService class - iOS](../NowChatService/concept/NowChatServiceiOSAPI.md#)**  
The NowChatService class provides Virtual and Live Agent chat capabilities.
-   **[NowChatServiceDelegate protocol - iOS](../NowChatServiceDelegate/concept/NowChatServiceDelegateiOSProtocol.md#)**  
The NowChatServiceDelegate protocol provides callbacks for notification of actions within the NowChatService such as a request to open a URL or dismiss the chat view controller.
-   **[NowChatThemeable protocol - iOS](../NowChatThemeable/concept/NowChatThemeableiOSProtocol.md)**  
The NowChatThemeable protocol provides properties that enable you to override the colors used within chat pages hosted on your ServiceNow instance.
-   **[NowCoreService class - iOS](../NowCoreService/concept/NowCoreServiceiOSAPI.md#)**  
The NowCoreService class provides fundamental services to the various SDK feature services. This class should only be instantiated by NowSDK.
-   **[NowData framework - iOS](../NowData/concept/NowDataAPIiOS.md#)**  
The NowData framework contains methods that enable the instantiation of NowData services, such as NowGraphQLService, NowTableService, NowAPIService \(for custom APIs\), andNowAttachmentService.
-   **[NowGraphQLService class - iOS](../NowGraphQLService/concept/NowGraphQLServiceiOSAPI.md#)**  
The NowGraphQLService class provides functions that enable you to make requests using GraphQL queries against data on your ServiceNow instance through itsGraphQL REST API.
-   **[NowLoggingService class - iOS](../NowLoggingService/concept/NowLoggingServiceiOSAPI.md#)**  
The NowLoggingService class provides functions that provide logging capabilities to feature services with the NowSDK.
-   **[NowPush API - iOS](../NowPush/concept/NowPushiOSAPI.md#)**  
The NowPush API is a top-level global API that enables users to instantiate a NowPush service instance.
-   **[NowPushPayload protocol](../NowPushPayload/concept/NowPushPayloadiOSProtocol.md#)**  
NowPushPayload is a generic protocol you can use to define a push notification protocol within the `NowSDK` framework.
-   **[NowPushService class - iOS](../NowPushService/concept/NowPushServiceiOSAPI.md#)**  
The NowPushService class provides functions that enable interaction with the Push Notification service.
-   **[NowRecord class - iOS](../NowRecord/concept/NowRecordiOSAPI.md#)**  
The NowRecord class defines a model that represents a record in a table on a ServiceNow instance.
-   **[NowSDK framework - iOS](../NowSDK/concept/NowSDKAPIiOS.md#)**  
The NowSDK framework contains methods that enable the instantiation of various feature services.
-   **[NowSDKConfiguration class - iOS](../NowSDKConfiguration/concept/NowSDKConfigurationiOSAPI.md#)**  
The NowSDKConfiguration class contains configuration information needed to initialize the NowSDK.
-   **[NowService protocol - iOS](../NowService/concept/NowServiceiOSProtocol.md#)**  
The NowService protocol provides a single interface to the NowSDK for all feature services. It defines the configuration parameters needed to access your ServiceNow instance.
-   **[NowServiceConfiguration structure - iOS](../NowServiceConfiguration/concept/NowServiceConfigurationiOSStruct.md#)**  
The NowServiceConfiguration structure defines configuration information for a feature service.
-   **[NowTableService class - iOS](../NowTableService/concept/NowTableServiceiOSAPI.md#)**  
The NowTableService class provides functions that enable you to perform create, read, update, and delete operations on records of existing ServiceNow tables.
-   **[NowWeb API - iOS](../NowWeb/concept/NowWebiOSAPI.md#)**  
The NowWeb API is a top-level global API that enables uses to instantiate a NowWeb service instance.
-   **[NowWebColoring protocol - iOS](../NowWebColoring/concept/NowWebColoringiOSProtocol.md)**  
The NowWebColoring protocol provides default values for the colors used within web pages hosted on your ServiceNow instance in a native web view.
-   **[NowWebService class - iOS](../NowWebService/concept/NowWebServiceiOSAPI.md#)**  
The NowWebService class provides functions that enable the browsing of web pages on a ServiceNow instance.
-   **[NowWebThemeable protocol - iOS](../NowWebThemeable/concept/NowWebThemeableiOSProtocol.md)**  
The NowWebThemeable protocol provides properties that enable you to override the colors used within web pages hosted on your ServiceNow instance in a native web view.
-   **[NowWebViewController class - iOS](../NowWebViewController/concept/NWebViewControlleriOSAPI.md#)**  
The NowWebViewController class provides functions that enable you to manage a web viewer.
-   **[NowWebViewControllerDelegate protocol - iOS](../NowWebViewControllerDelegate/concept/NWViewControllerDelegateiOSProtocol.md#)**  
The NowWebViewControllerDelegate protocol provides callbacks for notification of issues within the NowWebViewController processing such as when a flow ends or a navigation fails.
-   **[Paginator API - iOS](../Paginator/concept/PaginatorIOSAPI.md#)**  
The Paginator class provides methods for iterating through a record set returned by a call to the ServiceNow Table API through the NowTableService. It is the object that is returned by the NowTableService paginator\(\) methods. Do not call this method outside of that environment.
-   **[SNMobileAnalytics API](../../SNMobileAnalytics/concept/SNMobileAnalytics.md#)**  
The SNMobileAnalytics API provides methods that you can call within a WebView using JavaScript. These methods enable you to push custom analytics data \(events, pages, and user properties\) to the User Experience Analytics for Service Portal dashboard.

**Parent Topic:**[Mobile SDK API reference](../../../../../build/applications/concept/api-mobile_sdk.md)

