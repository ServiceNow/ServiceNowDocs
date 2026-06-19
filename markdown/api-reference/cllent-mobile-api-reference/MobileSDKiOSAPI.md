---
title: Mobile SDK - iOS
description: The Mobile SDK for iOS provides the classes necessary to interface iOS-based devices with the ServiceNow platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/cllent-mobile-api-reference/MobileSDKiOSAPI.html
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Mobile SDK API reference, API reference, API implementation and reference]
---

# Mobile SDK - iOS

The Mobile SDK for iOS provides the classes necessary to interface iOS-based devices with the ServiceNow platform.

-   **[FetchConfiguration structure - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/FetchConfigiOSStructure.md)**  
The FetchConfiguration structure provides the ability to define the configuration for fetching records from your ServiceNow instance.
-   **[FieldReadConfiguration structure - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/FieldReadConfigurationiOSStruct.md)**  
The FieldReadConfiguration structure enables you to configure which fields to fetch from a ServiceNow instance table and in which format.
-   **[FieldWriteOptions class - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/FieldWriteOptionsiOSStruct.md)**  
The FieldWriteOptions class provides functions that set the options for updating or creating fields in a record on a ServiceNow instance.
-   **[Filter structure - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/FilteriOSStructure.md)**  
The Filter structure provides the ability to configure filters that define the data to return in the return results of a REST endpoint query.
-   **[NowAnalyticsService protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowAnalyticsServiceiOSProtocol.md)**  
The NowAnalyticsService protocol provides functions that enable you to configure analytics properties, user settings, and events for managing the collection of user analytics data.
-   **[NowAnalyticsServiceDelegate protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowAnalyticsServiceDeliOSProtocol.md)**  
The NowAnalyticsServiceDelegate protocol provides callback functions that provide information about the starting and ending of a user session and screen change detection.
-   **[NowAPIEndpoint protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowAPIEndpointiOSProtocol.md)**  
The NowAPIEndpoint protocol provides an interface for accessing any publicly exposed ServiceNow REST APIs.
-   **[NowAPIService class - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowAPIServiceiOSAPI.md)**  
The NowAPIService class provides functions that enable you to perform requests to a specified ServiceNow REST API.
-   **[NowAttachment structure - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowAttachmentiOSStructure.md)**  
The NowAttachment structure provides functions that enable you to validate attachments by comparing their computed hash.
-   **[NowAttachmentMetadata structure - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowAttachmentMetadataiOSStructure.md)**  
The NowAttachmentMetadata structure provides functions that enable you to encode and manage attachment metadata.
-   **[NowAttachmentService class - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowAttachmentServiceiOSAPI.md)**  
The NowAttachmentService class provides functions that enable you to upload and query attachments that are associated with records within a table on a ServiceNow instance.
-   **[NowAttachmentUploadConfiguration structure - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowAttachUploadConfigiOSStruct.md)**  
The NowAttachmentUploadConfiguration structure enables you to define the configuration information for an attachment that you are uploading to your ServiceNow instance.
-   **[NowChat API - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowChatiOSAPI.md)**  
The NowChat API is a top-level global API that enables users to instantiate a NowChat service instance.
-   **[NowChatColoring protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowChatColoringiOSProtocol.md)**  
The NowChatColoring protocol defines default colors for the elements in the Live Agent and Virtual Agent chat UI.
-   **[NowChatConfiguration - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowChatOptionsiOS.md)**  
The NowChatConfiguration class enables you to configure options on a chat session, such as showing a prompt before closing a chat window, disabling features while using chat, applying different conversation options when using chat, and configuring UI components in NowChat.
-   **[NowChatService class - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowChatServiceiOSAPI.md)**  
The NowChatService class provides Virtual and Live Agent chat capabilities.
-   **[NowChatServiceDelegate protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowChatServiceDelegateiOSProtocol.md)**  
The NowChatServiceDelegate protocol provides callbacks for notification of actions within the NowChatService such as a request to open a URL or dismiss the chat view controller.
-   **[NowChatThemeable protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowChatThemeableiOSProtocol.md)**  
The NowChatThemeable protocol provides properties that enable you to override the colors used within chat pages hosted on your ServiceNow instance.
-   **[NowCoreService class - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowCoreServiceiOSAPI.md)**  
The NowCoreService class provides fundamental services to the various SDK feature services. This class should only be instantiated by NowSDK.
-   **[NowData framework - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowDataAPIiOS.md)**  
The NowData framework contains methods that enable the instantiation of NowData services, such as NowGraphQLService, NowTableService, NowAPIService \(for custom APIs\), andNowAttachmentService.
-   **[NowGraphQLService class - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowGraphQLServiceiOSAPI.md)**  
The NowGraphQLService class provides functions that enable you to make requests using GraphQL queries against data on your ServiceNow instance through itsGraphQL REST API.
-   **[NowLoggingService class - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowLoggingServiceiOSAPI.md)**  
The NowLoggingService class provides functions that provide logging capabilities to feature services with the NowSDK.
-   **[NowPush API - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowPushiOSAPI.md)**  
The NowPush API is a top-level global API that enables users to instantiate a NowPush service instance.
-   **[NowPushPayload protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowPushPayloadiOSProtocol.md)**  
NowPushPayload is a generic protocol you can use to define a push notification protocol within the `NowSDK` framework.
-   **[NowPushService class - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowPushServiceiOSAPI.md)**  
The NowPushService class provides functions that enable interaction with the Push Notification service.
-   **[NowRecord class - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowRecordiOSAPI.md)**  
The NowRecord class defines a model that represents a record in a table on a ServiceNow instance.
-   **[NowSDK framework - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowSDKAPIiOS.md)**  
The NowSDK framework contains methods that enable the instantiation of various feature services.
-   **[NowSDKConfiguration class - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowSDKConfigurationiOSAPI.md)**  
The NowSDKConfiguration class contains configuration information needed to initialize the NowSDK.
-   **[NowService protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowServiceiOSProtocol.md)**  
The NowService protocol provides a single interface to the NowSDK for all feature services. It defines the configuration parameters needed to access your ServiceNow instance.
-   **[NowServiceConfiguration structure - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowServiceConfigurationiOSStruct.md)**  
The NowServiceConfiguration structure defines configuration information for a feature service.
-   **[NowTableService class - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowTableServiceiOSAPI.md)**  
The NowTableService class provides functions that enable you to perform create, read, update, and delete operations on records of existing ServiceNow tables.
-   **[NowWeb API - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowWebiOSAPI.md)**  
The NowWeb API is a top-level global API that enables uses to instantiate a NowWeb service instance.
-   **[NowWebColoring protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowWebColoringiOSProtocol.md)**  
The NowWebColoring protocol provides default values for the colors used within web pages hosted on your ServiceNow instance in a native web view.
-   **[NowWebService class - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowWebServiceiOSAPI.md)**  
The NowWebService class provides functions that enable the browsing of web pages on a ServiceNow instance.
-   **[NowWebThemeable protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowWebThemeableiOSProtocol.md)**  
The NowWebThemeable protocol provides properties that enable you to override the colors used within web pages hosted on your ServiceNow instance in a native web view.
-   **[NowWebViewController class - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NWebViewControlleriOSAPI.md)**  
The NowWebViewController class provides functions that enable you to manage a web viewer.
-   **[NowWebViewControllerDelegate protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NWViewControllerDelegateiOSProtocol.md)**  
The NowWebViewControllerDelegate protocol provides callbacks for notification of issues within the NowWebViewController processing such as when a flow ends or a navigation fails.
-   **[Paginator API - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/PaginatorIOSAPI.md)**  
The Paginator class provides methods for iterating through a record set returned by a call to the ServiceNow Table API through the NowTableService. It is the object that is returned by the NowTableService paginator\(\) methods. Do not call this method outside of that environment.
-   **[SNMobileAnalytics API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/SNMobileAnalytics.md)**  
The SNMobileAnalytics API provides methods that you can call within a WebView using JavaScript. These methods enable you to push custom analytics data \(events, pages, and user properties\) to the Usage Insights for Service Portal dashboard.

**Parent Topic:**[Mobile SDK API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/api-mobile_sdk.md)

