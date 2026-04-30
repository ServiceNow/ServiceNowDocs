---
title: Developing applications with the ServiceNow IDE
description: Create and develop applications in source code with the ServiceNow IDE. Build applications to make your changes available across an instance and collaborate with users of any skill set.
locale: en-US
release: zurich
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Developing applications with the ServiceNow IDE

Create and develop applications in source code with the ServiceNow IDE. Build applications to make your changes available across an instance and collaborate with users of any skill set.

In the ServiceNow IDE, you create scoped applications or convert existing applicationsand develop them in source code using ServiceNow Fluent to define application metadata \[sys\_metadata\]. Optionally, you can create JavaScript modules and use third-party libraries to organize and reuse code within scoped applications.

When your changes are saved and ready, build an application to compile the source code to application metadata and make your changes available to users across the instance. As other users modify the application metadata, you can synchronize the changes into the source code.

Learn how to get started developing applications with the ServiceNow IDE in the following topics.

## System requirements

ServiceNow IDE uses the public npm registry \(`https://registry.npmjs.org`\) as its default package source. If your network blocks access to this registry, you must have access to an alternate registry to download packages and build applications in the ServiceNow IDE. If access to the public npm registry is blocked on your system, you must configure a private npm registry in your Package Manager user settings in the ServiceNow IDE. For more information, see [Install an npm package from a private registry with the ServiceNow IDE](../task/use-library-private-npm-registry.md).

-   **[Synchronizing applications in the ServiceNow IDE](synchronizing-applications.md)**  
Synchronizing an application in the ServiceNow IDE downloads and transforms application metadata into ServiceNow Fluent code.
-   **[Define application metadata in code with ServiceNow Fluent in the ServiceNow IDE](../task/define-metadata-code-fluent-ide.md)**  
Define application metadata in code with ServiceNow Fluent in the ServiceNow IDE.
-   **[Create and use JavaScript modules in applications in the ServiceNow IDE](../task/create-use-javascript-modules-ide.md)**  
Optimize your codebase by defining reusable code blocks with JavaScript modules in the ServiceNow IDE.
-   **[Use third-party libraries in applications in the ServiceNow IDE](../task/use-third-party-libraries-ide.md)**  
Call third-party libraries in your application to use existing open-source functionality with the ServiceNow IDE.
-   **[Create an application file from the Metadata Explorer](../task/create-application-file-servicenow-ide.md)**  
Create an application file in an embedded ServiceNow AI Platform user interface from the Metadata Explorer in the ServiceNow IDE.
-   **[Build and install an application in the ServiceNow IDE](../task/build-applications-servicenow-ide.md)**  
Build an application to compile its source code and install application changes across an instance from the ServiceNow IDE.

**Parent Topic:**[ServiceNow IDE](servicenow-ide-landing.md)

**Related topics**  


[Integrating source control with the ServiceNow IDE](integrating-source-control-servicenow-ide.md)

[ServiceNow Fluent API reference](../../servicenow-sdk/reference/servicenow-fluent-api-reference.md)

