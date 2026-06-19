---
title: Mobile SDK - Android
description: The Mobile SDK for Android provides the classes necessary to interface Android devices with the ServiceNow platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/cllent-mobile-api-reference/MobileSDKAndroidAPI.html
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Mobile SDK API reference, API reference, API implementation and reference]
---

# Mobile SDK - Android

The Mobile SDK for Android provides the classes necessary to interface Android devices with the ServiceNow platform.

-   **[AuthorizationToken class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/AuthorizationTokenAndroidAPI.md)**  
The AuthorizationToken class provides the authorization token provided by the host application. Used by the NowSDK to authorize access to a specified ServiceNow instance for the currently logged in user.
-   **[Call interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/CallAndroidInterface.md)**  
The Call interface represents a request that is prepared for processing.
-   **[FetchConfiguration class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/FetchConfigAndroidAPI.md)**  
The FetchConfiguration class provides the ability to define the configuration for fetching records from the associatedServiceNow table.
-   **[FieldReadConfiguration class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/FieldReadConfigAndroidAPI.md)**  
The FieldReadConfiguration class provides the ability to define what fields to return or not return in a response record.
-   **[FieldWriteOptions structure - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/FieldWriteOptionsAndroidAPI.md)**  
The FieldWriteOptions class provides functions that set the options for updating or creating fields in a record on a ServiceNow instance.
-   **[Filter class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/FilterAndroidAPI.md)**  
The Filter class provides the ability to configure filters that define the data to return in the return results of a REST endpoint query.
-   **[NotSupportedPushError class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NotSupportedPushErrorAndroidAPI.md)**  
A function from the NotSupportedPushError class is thrown when the NowPushSDK cannot process the push notification request. When this type of error is thrown, you must parse and handle the push notification outside of the MobileSDK framework.
-   **[NowAnalyticsSDK interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowAnalyticsAndroidInterface.md)**  
The NowAnalyticsSDK interface provides functions that enable you to configure analytics properties, user settings, and events for managing a collection of user analytics data.
-   **[NowAPIService interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowAPIServiceAndroidInterface.md)**  
The NowAPIService interface provides the ability to perform requests on a specified ServiceNow REST API.
-   **[NowAttachment class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowAttachmentAndroidAPI.md)**  
The NowAttachment class provides an object that contains an attachment and its associated metadata.
-   **[NowAttachmentMetadata class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowAttachmentMetadataAndroidAPI.md)**  
The NowAttachmentMetadata class provides functions that enable you to encode and manage attachment metadata.
-   **[NowAttachmentService interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowAttachServiceAndroidInterface.md)**  
The NowAttachmentService interface provides functions that enable the manipulation of file attachments and their associated metadata.
-   **[NowChatConfiguration class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowChatOptionsAndroid.md)**  
The NowChatConfiguration class enables you to configure options on a chat session, such as showing a prompt before closing a chat window, disabling features while using chat, applying different conversation options when using chat, and configuring UI components in NowChat.
-   **[NowChatSDK class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowChatSDKAndroidAPI.md)**  
The NowChatService class provides the function necessary to create a NowChatService that interacts with NowChat. NowChat provides the ability to embed Live Agent and Virtual Agent within your application.
-   **[NowChatSdkCallbacks interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowChatSdkCallbacksAndroidInt.md)**  
The NowChatSdkCallbacks interface provides functions that enable callbacks for host applications to configure or handle actions from the NowChatSDK.
-   **[NowChatService class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowChatServiceAndroidAPI.md)**  
The NowChatService class provides functions that enable you to launch the NowChat activity and set error configurations.
-   **[NowChatTheme interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowChatThemeColorsAndroidInterface.md)**  
The NowChatTheme interface defines default colors for the elements in the Live Agent and Virtual Agent chat UI.
-   **[NowDataSDK class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowDataSDKAndroidAPI.md)**  
The NowDataSDK class provides functions that enable the creation and initialization of various features services such as NowGraphQLService, NowAttachmentService, NowTableService, and NowAPIService.
-   **[NowGraphQLService interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowGQLServiceAndroidInterface.md)**  
The NowGraphQLService interface provides functions that allow you to make GraphQL requests to your ServiceNow through its GraphQL API.
-   **[NowPushPayload interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowPushPayloadAndroidInterface.md)**  
The NowPushPayload interface defines the push notification payload that the NowSDK implements.
-   **[NowPushSDK class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowPushSDKAndroidAPI.md)**  
The NowPushSDK class provides the function necessary to create a `NowPushService` that enables the sending of unsolicited \(push\) notifications to Android devices.
-   **[NowPushService class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowPushServiceAndroidAPI.md)**  
The NowPushService class provides functions that enable interaction with the Push Notification service.
-   **[NowSDK - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowSDKAndroidAPI.md)**  
The NowSDK class is a singleton that provides the public API for the NowSDK. This class is the gateway to all Android SDK feature services.
-   **[NowSDKAuthorizationProviding interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowSDKAuthProvidingAndroidInterface.md)**  
The NowSDKAuthorizationProviding interface provides a function that configures the link to the ServiceNow instance for which authorization is needed and any associated callbacks.
-   **[NowSDKConfiguration class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowSDKConfigurationAndroidAPI.md)**  
The NowSDKConfiguration class contains configuration information needed to initialize the NowSDK.
-   **[NowServiceConfiguration class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowServiceConfigurationAndroidAPI.md)**  
The NowServiceConfiguration class enables you to configure the ServiceNow instance URL and package name for a feature service.
-   **[NowServiceError class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowServiceErrorAndroidAPI.md)**  
The NowServiceError sealed class that returns NowSDK errors.
-   **[NowTableService interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowTableServiceAndroidInterface.md)**  
The NowTableService interface provides functions that enable you to create, read, delete, and update records within a table on a ServiceNow instance.
-   **[NowWebTheme interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowWebThemeAndroidInterface.md)**  
The NowWebTheme interface provides properties that enable you to override the colors used within web pages hosted on your ServiceNow instance in a native web view.
-   **[NowWebSDK class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowWebSDKAndroidAPI.md)**  
The NowWebSDK class provides a single function that enables you to load web pages hosted on your ServiceNow instance in a native web view and Cabrillo. It automatically handles user authentication and session management instead of forcing users to log into the instance through a login web page.
-   **[NowWebService class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowWebServiceAndroidAPI.md)**  
The NowWebService class provides a function that launches a NowWebActivity that hosts a web view.
-   **[NowWebViewServiceDelegate interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowWebViewServiceDelAndroidAPI.md)**  
The NowWebViewServiceDelegate API provides callbacks for notification of issues within the NowWebService processing such as when a flow ends or a navigation fails.
-   **[Paginator class - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/PaginatorAndroidAPI.md)**  
The Paginator class provides functions for paging through the return results passed back by a REST endpoint call, such as those returned by the NowTableService class.

**Parent Topic:**[Mobile SDK API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/api-mobile_sdk.md)

