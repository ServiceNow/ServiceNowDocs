---
title: UI Page API - ServiceNow Fluent
description: The UI Page API defines custom user interface \(UI\) pages \[sys\_ui\_page\] that display forms, dialogs, lists, and other UI components.Create a UI page \[sys\_ui\_page\] for a custom user interface.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# UI Page API - ServiceNow Fluent

The UI Page API defines custom user interface \(UI\) pages \[sys\_ui\_page\] that display forms, dialogs, lists, and other UI components.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

A UI page displays as a web page and can be added to a widget for use in dashboards. For general information about UI pages, see [UI pages](https://www.servicenow.com/docs/access?context=r_UIPages&version=australia&pubname=australia-api-reference&ft:locale=en-US).

You can develop a simple React application with the UI Page API. In the `src/client` directory, add static content files that define the HTML, client script, and styling of the page. From the UiPage object, refer to the page's HTML entry point \(`index.html`\). For more information, see [User interface development with React](../concept/ui-development-react.md).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## UiPage object

Create a UI page \[sys\_ui\_page\] for a custom user interface.

<table id="table_qyv_1pj_4fc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

endpoint

</td><td>

String

</td><td>

Required. The endpoint to access the web page. The endpoint value can't contain spaces.Format: `<scope>_<ui_page_name>.do`

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of the user interface and its purpose.

</td></tr><tr><td>

direct

</td><td>

Boolean

</td><td>

Flag that indicates whether to omit the standard HTML, CSS, and JavaScript for a UI page. For React UI pages, set this property to `true`.Valid values:

-   true: Omit the standard HTML, CSS, and JavaScript and provide custom CSS and JavaScript for the page.
-   false: Include the standard HTML, CSS, and JavaScript.

Default: false

</td></tr><tr><td>

html

</td><td>

String

</td><td>

The body HTML code that defines what is rendered when the page is shown. It can contain either static XHTML, dynamically generated content defined as Jelly, or call script includes and UI Macros. This property supports an alias to import an `index.html` file for React development, a reference to another file in the application that contains HTML, or inline JavaScript.**Note:** With React development and imported HTML, the html property of the UiPage object supports only one-way synchronization. After defining the HTML of a UI page in source code, if the HTML is modified outside of the source code, those changes aren't synchronized and reflected in the source code.

Format:

-   An alias to import the `index.html` file from the previous build for UI development with React. The alias can be any value and must also be imported in the `now.ts` file that contains the UiPage object: `import <alias> from 'path/to/index.html'`.
-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide inline HTML, use string literals or template literals for multiple lines of code: `'HTML' or `HTML``.

</td></tr><tr><td>

category

</td><td>

String

</td><td>

The type of UI page.Valid values:

-   general: The page is general purpose.
-   homepages: The page is used as a home page.
-   htmleditor: The page is used to insert HTML content.
-   kb: The page is used with a Knowledge Base.
-   cms: The page is used with the Content Management System \(CMS\).
-   catalog: The page is used with Service Catalog.

</td></tr><tr><td>

clientScript

</td><td>

Script

</td><td>

A script that runs in the browser, such as functions called by buttons. This script handles any required client-side processing needed, like setting focus to a field or other interactive DHTML features after a page is loaded. This property supports inline JavaScript or a reference to another file in the application that contains a script.Client scripts for the UI page are deployed to the browser within a `<script>` tag, so the content can similarly be defined within the HTML field. The clientScript property can be used instead to define these scripts concisely to maintain the Jelly and HTML manageability.

Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

processingScript

</td><td>

Script

</td><td>

A script that runs on the server when the page is submitted, which is useful if your page has a form defined with the `<g:ui_form/>` or `<g:form/>` tags. This property supports a function from a JavaScript module, a reference to another file in the application that contains a script, or inline JavaScript.Format:

-   For functions, use the name of a function, function expression, or default function exported from a JavaScript module and import it into the `.now.ts` file. For information about JavaScript modules, see [JavaScript modules and third-party libraries](../concept/javascript-modules-third-party-libraries.md).
-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>In this example of UI development with React, the HTML of the page is imported from the `index.html` file in the `src/client` directory.

```javascript
//incident-manager.now.ts
import '@servicenow/sdk/global'
import { UiPage } from '@servicenow/sdk/core'
import incidentPage from '../../client/index.html'

UiPage({
    $id: Now.ID['incident-manager-page'],
    endpoint: '<scope>_incident_manager.do',
    description: 'Incident Response Manager UI Page',
    category: 'general',
    html: incidentPage,
    direct: true,
})
```

In the `index.html` file, the `<script>` tag refers to the `main.jsx` file in the `src/client` directory, which contains the component code.

```xml
//index.html
<html>
<head>
  <title>Incident Response Manager</title>

  <!-- Initialize globals and Include ServiceNow's required scripts -->
  <sdk:now-ux-globals></sdk:now-ux-globals>

  <!-- Include your React entry point -->
  <script src="./main.jsx" type="module"></script>
</head>
<body>
  <div id="root"></div>
</body>
</html>
```

