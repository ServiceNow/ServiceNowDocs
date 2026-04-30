---
title: Digital interface form
description: Digital interfaces are provided as part of a business application, but they can also stand on their own. Interfaces provide a way for other business applications to interact with the applications.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Digital interface form

Digital interfaces are provided as part of a business application, but they can also stand on their own. Interfaces provide a way for other business applications to interact with the applications.

## Digital interface form fields

<table id="table_n14_btp_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and meaningful name of the digital interface. Enter a descriptive name that reflects the purpose of the interface.

</td></tr><tr><td>

Number

</td><td>

Number of the digital interface. This field is automatically generated with the DINTF prefix and can’t be edited.

</td></tr><tr><td>

Provider Business Application

</td><td>

Name of the provider business application that provides, manager, and owns the interface.**Note:** This attribute can be empty if there is no business application in your repository. If you are using open interfaces such as Weather or Financial Service, you are only aware of the interface and track it without a related business application.

</td></tr><tr><td>

Provider company

</td><td>

Name of the provider company.

</td></tr><tr><td>

Interface Type

</td><td>

Type of API used by the interface. This field helps to track whether the API is Public or Open.**Note:** For Public or Open APIs, there won’t be any Provider Business Application unless the Organization exposes it as an open interface.

Use the following options:

-   Open API
-   Partner API
-   Internal API

Public or Open APIs are available to anyone and can be used without any restrictions or license agreements.

Internal or Private APIs are available to authorized \(technical\) users only and can be used without any usage restrictions and regulations.

Partner APIs are available to authorized partners of an API provider. Usually, these APIs have special terms and conditions for usage.

</td></tr><tr><td>

Parent

</td><td>

Name of the parent interface.Often, interfaces are bundled or part of a composition. Because you can reference a digital interface on the digital integration, use the parent interface. The digital interfaces related to the parent interface are listed in the related list of the interface.

</td></tr><tr><td>

Version

</td><td>

Version of the interface. This field helps you to track which digital integrations are using which version of an interface.

</td></tr><tr><td>

Life Cycle Stage

</td><td>

Life cycle stage of the interface. Use the following options:-   Ideation
-   Design
-   Deploy
-   Operational
-   End of Life

</td></tr><tr><td>

Life Cycle Stage Status

</td><td>

Life cycle stage status of the interface. Each of the main life cycle stages can have one or more life cycle stage statuses. For example, a digital Interface in the operational stage might change status over time from In Use to In Maintenance to Pending Retirement. Use the following options:-   Ideation: Under Evaluation, Pilot
-   Design: Chartered, Design, Build
-   Deploy: Test
-   Operational: In Use, In Maintenance, Pending Retirement
-   End of Life: Retired, Obsolete

</td></tr><tr><td>

Model ID

</td><td>

Model ID of the interface. This field helps you to track the interface model.This is a reference to the Application Model table where you can manage your own variants of API models or types. For example, Table API, Attachment API, Aggregate API, and Process APIs. This optional field can be used to track the interface model. Depending on your use case, you can add new models and model categories.

</td></tr><tr><td>

Description

</td><td>

Description of the digital interface. Provide the high-level design aspects of the interface. You can provide the details such as how the digital interface adds value, how it should be designed, and how it’s intended to be used.

You can also describe different changes and capabilities according to version of the interface. It helps the Application owners and Architects to decide which interface version they want to use.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Business Owner|The owner of the business function, who owns the digital interface. It can be the same person who owns the parent business application.|
|IT Owner|The owner within the IT organization, who owns the digital interface. It can be the same person who owns the parent business application.|
|Supported By|Name of the Subject matter Expert \(SME\) or individual who provides support to the digital interface.|
|Support Group|Name of the group that provides support to the digital interface.|

<table id="table_gdl_xwt_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Protocol

</td><td>

Type of protocol used by the interface. API Protocols are the specifications that regulate the application. These protocols are used to integrate application programming interfaces with their software. Choices include REST, SOAP, LDAP, and so on.**Note:** This list is a non-exhaustive list and can be extended by adding your preferred values or hide the provided values.

</td></tr><tr><td>

Message Format

</td><td>

Format of the message in the interface. Choices include JSON, XML, CSV, and so on.**Note:** This list is a non-exhaustive list and can be extended by adding your preferred values or hide the provided values.

</td></tr></tbody>
</table><table id="table_jkt_zwt_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authentication Type

</td><td>

Type of authentication used to authenticate the interface. Use the following options:

-   Basic Auth
-   OpenID Connect
-   Certificate
-   WS-Security
-   LDAP
-   None
-   Other

You can use the system-provided authentication types or add yours.

</td></tr><tr><td>

Authorization Type

</td><td>

Type of authorization used to authorize the interface.Use the following options:

-   OAuth 2.0 Token
-   JWT Web Token
-   SAML 2.0 Token
-   Other
-   No authorization

You can use the system-provided authentication types or add yours.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Work notes|Comments about the interface.|

**Parent Topic:**[Enterprise Architecture Workspace reference](eaw-reference.md)

**Related topics**  


[Add or edit a digital interface in the EA Workspace](../../task/eaw-task/eaw-create-digital-interface.md)

