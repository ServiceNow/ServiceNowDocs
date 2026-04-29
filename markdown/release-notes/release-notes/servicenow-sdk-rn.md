---
title: ServiceNow SDK release notes
description: The ServiceNow software development kit \(SDK\) enables developers to create scoped applications in source code locally in Visual Studio Code Desktop and upload changes to a ServiceNow instance. ServiceNow SDK was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# ServiceNow SDK release notes

The ServiceNow® software development kit \(SDK\) enables developers to create scoped applications in source code locally in Visual Studio Code Desktop and upload changes to a ServiceNow instance. ServiceNow SDK was enhanced and updated in the Australia release.

## ServiceNow SDK highlights for the Australia release

Create or convert applications in the global scope with instances on the Australia release.

See [ServiceNow SDK](https://www.servicenow.com/docs/access?context=servicenow-sdk-landing&version=australia&pubname=australia-application-development&ft:locale=en-US) for more information.

## Important information for upgrading ServiceNow SDK to Australia

To upgrade to the latest version of the ServiceNow SDK globally or within an application, see [Upgrade the ServiceNow SDK](https://www.servicenow.com/docs/access?context=upgrade-servicenow-sdk&version=australia&pubname=australia-application-development&ft:locale=en-US).

ServiceNow SDK version 4.4 supports integration with ServiceNow instances beginning with the Washington DC release.

On Windows systems, after upgrading to ServiceNow SDK version 4.3 or later, existing stored credentials aren’t supported due to the deprecation of Keytar. Users on Windows systems must add their user credentials again using the `now-sdk auth --add` command to authenticate with instances. For more information, see [Authenticating to a ServiceNow instance with the ServiceNow SDK](https://www.servicenow.com/docs/access?context=authenticate-instance-now-sdk&version=australia&pubname=australia-application-development&ft:locale=en-US).

**Important:** For minor releases of the ServiceNow SDK, see the [ServiceNow SDK release notes](https://github.com/ServiceNow/sdk/releases) on GitHub.

## New in the Australia release

-   **[Create and convert global applications](https://www.servicenow.com/docs/access?context=creating-applications-servicenow-sdk&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    Create and convert applications in the global scope that are accessible to other global applications with instances on the Australia release.

-   **[Move application metadata from the global scope into a global application](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    Transform application metadata \(XML\) in the global scope from an instance into ServiceNow Fluent source code to customize it in a local global application using the `now-sdk move` command.

-   **[Configure a default language for field labels](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=australia&pubname=australia-application-development&ft:locale=en-US#application-structure)**

    Configure a default language for field labels \[sys\_documentation\] in a table or column with the `tableDefaultLanguage` parameter in an application's `now.config.json` file.

-   **[Configure read-only options with the Table API](https://www.servicenow.com/docs/access?context=table-api-now-ts&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    Control the editability of read-only fields by configuring read-only options for a field with the readOnlyOption property in a Column object.


## Changed in this release

-   **[Flow API supports Service Catalog triggers and actions](https://www.servicenow.com/docs/access?context=fluent-flow-api&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    Use triggers and actions related to Service Catalog with the Flow API.

-   **[Access Control List API supports protection policies](https://www.servicenow.com/docs/access?context=acl-api-now-ts&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    Control whether someone can view or edit an access control list \(ACL\) with the protectionPolicy property in an ACL object.

-   **[Keys updated for static assets in full-stack applications](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    Static UX Assets \[sys\_ux\_lib\_asset\] in full-stack applications have updated keys in the `keys.ts` file. UX Asset sys\_ids aren’t changed.


## Activation information

The ServiceNow SDK is available as a Node Package Manager \(npm\) package from the [public npm registry](https://www.npmjs.com/package/@servicenow/sdk) and installed locally. For information about installing the ServiceNow SDK, see [Install the ServiceNow SDK in an application](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&version=australia&pubname=australia-application-development&ft:locale=en-US).

## Additional requirements

You must have Node.js and Node Package Manager \(npm\) installed to install the ServiceNow SDK. For more information, see [Install the ServiceNow SDK in an application](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&version=australia&pubname=australia-application-development&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[ServiceNow IDE](https://www.servicenow.com/docs/access?context=servicenow-ide-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    The ServiceNow IDE uses the ServiceNow SDK as its application packaging service to build applications, and the ServiceNow SDK provides the ServiceNow Fluent APIs for developing applications in source code in the ServiceNow IDE. Scoped applications created or converted with the ServiceNow SDK or ServiceNow IDE can be developed with either application.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

