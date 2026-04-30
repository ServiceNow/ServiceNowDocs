---
title: Mobile SDK API reference - Android
description: The Mobile SDK for Android provides the classes necessary to interface Android devices with the ServiceNow platform.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Mobile SDK API reference, API reference, API implementation and reference]
---

# Mobile SDK API reference - Android

The Mobile SDK for Android provides the classes necessary to interface Android devices with the ServiceNow platform.

It provides classes that enable you to create feature services such as chat, REST API interface, GraphQL, and web access, that allow you to create interactive applications on any Android device.

For additional information on how to implement specific use cases using this API, see the [Mobile SDK Developer Guide - Android](../../../../../integrate/guides/mobile_sdk/mobile_sdk-android/concept/mobsdk-and-overview.md).

-   **[AuthorizationToken class - Android](../AuthorizationToken/concept/AuthorizationTokenAndroidAPI.md#)**  
The AuthorizationToken class provides the authorization token provided by the host application. Used by the NowSDK to authorize access to a specified ServiceNow instance for the currently logged in user.
-   **[Call interface - Android](../Call/concept/CallAndroidInterface.md#)**  
The Call interface represents a request that is prepared for processing.
-   **[FetchConfiguration class - Android](../FetchConfiguration/concept/FetchConfigAndroidAPI.md#)**  
The FetchConfiguration class provides the ability to define the configuration for fetching records from the associatedServiceNow table.
-   **[FieldReadConfiguration class - Android](../FieldReadConfiguration/concept/FieldReadConfigAndroidAPI.md#)**  
The FieldReadConfiguration class provides the ability to define what fields to return or not return in a response record.
-   **[FieldWriteOptions structure - Android](../FieldWriteOptions/concept/FieldWriteOptionsAndroidAPI.md#)**  
The FieldWriteOptions class provides functions that set the options for updating or creating fields in a record on a ServiceNow instance.
-   **[Filter API - Android](../Filter/concept/FilterAndroidAPI.md#)**  
The Filter class provides the ability to configure filters that define the data to return in the return results of a REST endpoint query.
-   **[NotSupportedPushError class - Android](../NotSupportedPushError/concept/NotSupportedPushErrorAndroidAPI.md#)**  
A function from the NotSupportedPushError class is thrown when the NowPushSDK cannot process the push notification request. When this type of error is thrown, you must parse and handle the push notification outside of the MobileSDK framework.
-   **[NowAnalyticsSDK interface - Android](../NowAnalytics/concept/NowAnalyticsAndroidInterface.md#)**  
The NowAnalyticsSDK interface provides functions that enable you to configure analytics properties, user settings, and events for managing a collection of user analytics data.
-   **[NowAPIService interface - Android](../NowAPIService/concept/NowAPIServiceAndroidInterface.md#)**  
The NowAPIService interface provides the ability to perform requests on a specified ServiceNow REST API.
-   **[NowAttachment class - Android](../NowAttachment/concept/NowAttachmentAndroidAPI.md#)**  
The NowAttachment class provides an object that contains an attachment and its associated metadata.
-   **[NowAttachmentMetadata class - Android](../NowAttachmentMetadata/concept/NowAttachmentMetadataAndroidAPI.md#)**  
The NowAttachmentMetadata class provides functions that enable you to encode and manage attachment metadata.
-   **[NowAttachmentService interface - Android](../NowAttachmentService/concept/NowAttachServiceAndroidInterface.md#)**  
The NowAttachmentService interface provides functions that enable the manipulation of file attachments and their associated metadata.
-   **[NowChatConfiguration - Android](../NowChatOptions/concept/NowChatOptionsAndroid.md#)**  
The NowChatConfiguration class enables you to configure options on a chat session, such as showing a prompt before closing a chat window, disabling features while using chat, applying different conversation options when using chat, and configuring UI components in NowChat.
-   **[NowChatSDK class - Android](../NowChatSDK/concept/NowChatSDKAndroidAPI.md#)**  
The NowChatService class provides the function necessary to create a NowChatService that interacts with NowChat. NowChat provides the ability to embed Live Agent and Virtual Agent within your application.
-   **[NowChatSdkCallbacks interface - Android](../NowChatSdkCallbacks/concept/NowChatSdkCallbacksAndroidInt.md#)**  
The NowChatSdkCallbacks interface provides functions that enable callbacks for host applications to configure or handle actions from the NowChatSDK.
-   **[NowChatService class - Android](../NowChatService/concept/NowChatServiceAndroidAPI.md#)**  
The NowChatService class provides functions that enable you to launch the NowChat activity and set error configurations.
-   **[NowChatTheme interface - Android](../NowChatTheme/concept/NowChatThemeColorsAndroidInterface.md)**  
The NowChatTheme interface defines default colors for the elements in the Live Agent and Virtual Agent chat UI.
-   **[NowDataSDK class - Android](../NowDataSDK/concept/NowDataSDKAndroidAPI.md#)**  
The NowDataSDK class provides functions that enable the creation and initialization of various features services such as NowGraphQLService, NowAttachmentService, NowTableService, and NowAPIService.
-   **[NowGraphQLService interface - Android](../NowGraphQLService/concept/NowGQLServiceAndroidInterface.md#)**  
The NowGraphQLService interface provides functions that allow you to make GraphQL requests to your ServiceNow through its GraphQL API.
-   **[NowPushPayload interface](../NowPushPayload/concept/NowPushPayloadAndroidInterface.md#)**  
The NowPushPayload interface defines the push notification payload that the NowSDK implements.
-   **[NowPushSDK class - Android](../NowPushSDK/concept/NowPushSDKAndroidAPI.md#)**  
The NowPushSDK class provides the function necessary to create a `NowPushService` that enables the sending of unsolicited \(push\) notifications to Android devices.
-   **[NowPushService class - Android](../NowPushService/concept/NowPushServiceAndroidAPI.md#)**  
The NowPushService class provides functions that enable interaction with the Push Notification service.
-   **[NowSDK - Android](../NowSDK/concept/NowSDKAndroidAPI.md#)**  
The NowSDK class is a singleton that provides the public API for the NowSDK. This class is the gateway to all Android SDK feature services.
-   **[NowSDKAuthorizationProviding interface - Android](../NowSDKAuthorizationProviding/concept/NowSDKAuthProvidingAndroidInterface.md#)**  
The NowSDKAuthorizationProviding interface provides a function that configures the link to the ServiceNow instance for which authorization is needed and any associated callbacks.
-   **[NowSDKConfiguration class - Android](../NowSDKConfiguration/concept/NowSDKConfigurationAndroidAPI.md#)**  
The NowSDKConfiguration class contains configuration information needed to initialize the NowSDK.
-   **[NowServiceConfiguration class - Android](../NowServiceConfiguration/concept/NowServiceConfigurationAndroidAPI.md)**  
The NowServiceConfiguration class enables you to configure the ServiceNow instance URL and package name for a feature service.
-   **[NowServiceError class - Android](../NowServiceError/concept/NowServiceErrorAndroidAPI.md#)**  
The NowServiceError sealed class that returns NowSDK errors.
-   **[NowTableService interface - Android](../NowTableService/concept/NowTableServiceAndroidInterface.md#)**  
The NowTableService interface provides functions that enable you to create, read, delete, and update records within a table on a ServiceNow instance.
-   **[NowWebTheme interface - Android](../NowWebTheme/concept/NowWebThemeAndroidInterface.md)**  
The NowWebTheme interface provides properties that enable you to override the colors used within web pages hosted on your ServiceNow instance in a native web view.
-   **[NowWebSDK class - Android](../NowWebSDK/concept/NowWebSDKAndroidAPI.md#)**  
The NowWebSDK class provides a single function that enables you to load web pages hosted on your ServiceNow instance in a native web view and Cabrillo. It automatically handles user authentication and session management instead of forcing users to log into the instance through a login web page.
-   **[NowWebService class - Android](../NowWebService/concept/NowWebServiceAndroidAPI.md#)**  
The NowWebService API provides a function that launches a NowWebActivity that hosts a web view.
-   **[NowWebViewServiceDelegate interface - Android](../NowWebViewServiceDelegate/concept/NowWebViewServiceDelAndroidAPI.md#)**  
The NowWebViewServiceDelegate API provides callbacks for notification of issues within the NowWebService processing such as when a flow ends or a navigation fails.
-   **[Paginator class - Android](../Paginator/concept/PaginatorAndroidAPI.md#)**  
The Paginator class provides functions for paging through the return results passed back by a REST endpoint call, such as those returned by the NowTableService class.

**Parent Topic:**[Mobile SDK API reference](../../../../../build/applications/concept/api-mobile_sdk.md)

