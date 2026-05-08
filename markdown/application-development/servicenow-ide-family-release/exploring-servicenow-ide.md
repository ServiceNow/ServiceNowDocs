---
title: Exploring the ServiceNow IDE
description: Learn about developing applications in source code in the ServiceNow IDE.
locale: en-US
release: australia
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Exploring the ServiceNow IDE

Learn about developing applications in source code in the ServiceNow IDE.

## ServiceNow IDE overview

The ServiceNow IDE is an implementation of Visual Studio Code for the Web on the ServiceNow AI Platform. With the ServiceNow IDE, you can get started building applications quickly using familiar tools and industry-standard development practices. The ServiceNow IDE has many of the same features as Visual Studio Code, including type safety, IntelliSense, dependency enforcement, code search, and source control integration.

![The ServiceNow IDE homepage with the user's workspaces listed.](../image/servicenow-ide-welcome.png "ServiceNow IDE home page")

In the ServiceNow IDE, you can create applications in source code using ServiceNow Fluent to define application metadata \[sys\_metadata\]. To see a side-by-side visual representation of your changes in real time, you can open the application metadata in other ServiceNow AI Platform user interfaces embedded within the ServiceNow IDE.

Optionally, you can create JavaScript modules and use third-party libraries to organize and reuse code within an application scope. With Now Assist for Code, you can use the Code autocomplete skill to generate code suggestions for scripts in an application in the ServiceNow IDE. For more information, see Generate code with autocomplete.

In the background, this functionality is enabled by the ServiceNow SDK application packaging service, which builds applications in the ServiceNow IDE.

**Note:** You can use Build Agent to help you create and edit applications in the ServiceNow IDE. For more information, see [Build Agent](../../build-agent/concept/build-agent.md).

## ServiceNow IDE workflow

The following infographic shows the workflow for developers to get started developing applications with the ServiceNow IDE.

![Process for using the ServiceNow IDE to develop applications in source code. For details, refer to the following description.](../image/servicenow-ide-workflow.png "Developing applications with the ServiceNow IDE")

1.  Depending on the authentication method, an administrator or developer configures the credentials needed to connect to their Git provider.
    -   To use OAuth 2.0 authentication, an administrator configures an OAuth 2.0 application registry in their Git provider and on the instance.
    -   To use basic authentication, a developer generates a personal access token from their Git provider.
2.  From their Git provider, a developer creates a dedicated Git repository for an application.
3.  From the ServiceNow IDE, the developer configures their Git credentials.
4.  The developer creates a ServiceNow IDE workspace to organize applications.
5.  The developer creates an application or converts an existing applicationfrom the ServiceNow IDE.
6.  The developer initializes a local Git repository for the application and pushes it to the remote repository they created to manage the application in source control.
7.  The developer can define application metadata in source code using ServiceNow Fluent, create custom JavaScript modules, or use third-party libraries.
8.  When metadata changes are detected, the developer synchronizes the application to download and transform changes to metadata from other interfaces into source code.
9.  After saving their changes, they build the application, which compiles the source code and transforms it into application metadata.
10. When the build is complete, the developer can view their changes reflected in other embedded ServiceNow AI Platform user interfaces without leaving the ServiceNow IDE.
11. The developer stages, commits, and pushes their changes to the Git repository.
12. From the ServiceNow IDE, other developers can clone the repository, create branches, and begin collaborating on the application.

Other users can modify the application metadata at the same time as developers modify the source code. Developers can reuse module code in other modules or scripts within the application.

## ServiceNow IDE benefits

<table id="table_onb_vvg_z1c"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Develop applications in an IDE based on Visual Studio Code on the ServiceNow AI Platform

</td><td>

[ServiceNow IDE user interface](servicenow-ide-user-interface.md#)

</td><td>

Developers

</td></tr><tr><td>

Write source code to define the metadata that makes up ServiceNow applications

</td><td>

[ServiceNow Fluent](../../servicenow-sdk/concept/servicenow-fluent.md)[Define application metadata in code with ServiceNow Fluent in the ServiceNow IDE](../task/define-metadata-code-fluent-ide.md)

</td><td>

Developers

</td></tr><tr><td>

Organize and reuse code within an application scope with custom JavaScript modules and third-party JavaScript utilities

</td><td>

[JavaScript modules and third-party libraries](../../servicenow-sdk/concept/javascript-modules-third-party-libraries.md)[Create and use JavaScript modules in applications in the ServiceNow IDE](../task/create-use-javascript-modules-ide.md)

[Use third-party libraries in applications in the ServiceNow IDE](../task/use-third-party-libraries-ide.md)

</td><td>

Developers

</td></tr><tr><td>

Collaborate on applications with users of different skill sets

</td><td>

[Build and install an application in the ServiceNow IDE](../task/build-applications-servicenow-ide.md)

</td><td>

Developers

</td></tr><tr><td>

Integrate source control with your Git provider of choice

</td><td>

[Integrating source control with the ServiceNow IDE](integrating-source-control-servicenow-ide.md)

</td><td>

Developers, Administrators

</td></tr></tbody>
</table>