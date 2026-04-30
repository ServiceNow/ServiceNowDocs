---
title: Exploring the ServiceNow SDK
description: Learn about developing scoped applications in source code locally and installing changes on an instance with the ServiceNow SDK.
locale: en-US
release: zurich
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Exploring the ServiceNow SDK

Learn about developing scoped applications in source code locally and installing changes on an instance with the ServiceNow SDK.

## ServiceNow SDK overview

With the ServiceNow SDK, you can create and modify scoped applications locally in Visual Studio Code Desktop and install those applications on a non-production instance beginning with the Washington DC release. By developing applications locally, you can work offline and use features that are available in Visual Studio Code but not in the ServiceNow IDE.

In Visual Studio Code, you can develop scoped applications in source code using ServiceNow Fluent to define application metadata \[sys\_metadata\], write custom JavaScript modules, or add third-party libraries.

The ServiceNow SDK includes a command-line interface \(CLI\) for managing changes between an instance and a local application. Using simple CLI commands, you can authenticate to an instance, create or convert an application, transform application metadata \(XML\) into ServiceNow Fluent code, build and install the application on the instance, and more.

The ServiceNow SDK also serves as the application packaging service that builds applications in the ServiceNow IDE. For more information, see [Exploring the ServiceNow IDE](../../servicenow-ide/concept/exploring-servicenow-ide.md).

## ServiceNow SDK workflow

The following infographic shows the workflow for developers to get started developing applications with the ServiceNow SDK.

![Process for using the SDK in a local environment to develop applications and interface with an instance. For details, refer to the following description.](../image/sdk-workflow.png "Developing applications with the ServiceNow SDK")

1.  A developer installs the ServiceNow SDK locally. For more information, see [Install the ServiceNow SDK in an application](../task/install-servicenow-sdk.md).
2.  Using the CLI, the developer authenticates to a non-production instance to interface between their local environment and the instance with the `now-sdk auth` command. The developer must have the admin role on the instance.
3.  The developer creates a scoped application \(`now-sdk init`\) or converts an existing scoped application from the instance \(`now-sdk init --from`\) for use with the ServiceNow SDK.
4.  In Visual Studio Code, the developer can define application metadata in source code using ServiceNow Fluent, create custom JavaScript modules, or use third-party libraries.

    They can also download application and script dependencies from the instance to code against \(`now-sdk dependencies`\).

5.  The developer builds the application, which compiles the source code and transforms it into application metadata for the instance \(`now-sdk build`\).
6.  The developer installs the application on the instance \(`now-sdk install`\).
7.  Other users can continue to modify the application metadata on the instance, and developers can reuse the code from modules in other modules or scripts within the application.
8.  The developer downloads and transforms application metadata from the instance to get the latest updates to the application metadata locally \(`now-sdk transform`\), keeping it synchronized with the application on the instance.

You can manage applications in source control with your preferred Git provider. To develop a scoped application on another system with the ServiceNow SDK, other developers should clone the application from a remote GIt repository rather than downloading and transforming it from the instance.

## ServiceNow SDK benefits

<table id="table_ahd_34v_lzb"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Develop applications offline, outside of an instance in Visual Studio Code and manage them in source control with your preferred Git provider.

</td><td>

[Developing applications with the ServiceNow SDK](developing-applications-sdk.md)[Visual Studio Code documentation](https://code.visualstudio.com/docs)

</td><td>

Developers

</td></tr><tr><td>

Write source code to define the metadata that makes up ServiceNow applications

</td><td>

[ServiceNow Fluent](servicenow-fluent.md)

</td><td>

Developers

</td></tr><tr><td>

Organize and reuse code within scoped applications with custom JavaScript modules and third-party JavaScript utilities

</td><td>

[JavaScript modules and third-party libraries](javascript-modules-third-party-libraries.md)

</td><td>

Developers

</td></tr></tbody>
</table>