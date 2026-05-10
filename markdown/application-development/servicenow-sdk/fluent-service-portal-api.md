---
title: Service Portal API - ServiceNow Fluent
description: The Service Portal API defines custom widgets \[sp\_widget\] for portal pages.Create a custom widget \[sp\_widget\] to include on a portal page.Create an Angular Provider \[sp\_angular\_provider\] to reuse components in multiple widgets and improve portal performance.Create a widget dependency \[sp\_dependency\] to link JavaScript and CSS files to widgets and use third-party libraries, external style sheets, or Angular modules.Create a CSS include \[sp\_css\_include\] to reference a style sheet or external CSS in a widget dependency.Create a JS include \[sp\_js\_include\] to reference a UI script or external JavaScript code in a widget dependency.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Service Portal API - ServiceNow Fluent

The Service Portal API defines custom widgets \[sp\_widget\] for portal pages.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about portals, see [Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/c_ServicePortal.md).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## SPWidget object

Create a custom widget \[sp\_widget\] to include on a portal page.

For general information about creating custom widgets, see [Developing custom widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/widget-dev-guide.md).

<table id="table_egv_ymg_kfc" class="parameters"><thead><tr><th>

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

name

</td><td>

String

</td><td>

Required. A name for the widget.

</td></tr><tr><td>

category

</td><td>

String

</td><td>

The type of widget.Valid values:

-   standard
-   otherApplications
-   custom
-   sample
-   knowledgeBase
-   servicePortal
-   serviceCatalog

Default: custom

</td></tr><tr><td>

clientScript

</td><td>

Script

</td><td>

A client-side script that defines the AngularJS controller. This property supports inline JavaScript or a reference to another file in the application that contains a script. Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

Default:

```javascript
api.controller=function() { /* widget controller */ var c = this;};
```

</td></tr><tr><td>

serverScript

</td><td>

Script

</td><td>

A server-side script that sets the initial widget state, sends data to the widget's client script using the `data` object, or runs server-side queries. This property supports inline JavaScript or a reference to another file in the application that contains a script. Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

Default:

```javascript
(function () { /* populate the 'data' object */ /* e.g., data.table = $sp.getValue('table'); */ })();
```

</td></tr><tr><td>

controllerAs

</td><td>

String

</td><td>

A variable for a reference to the controller in the directive's scope. The client script accesses the server data object using the `c.data` variable by default.Default: c

</td></tr><tr><td>

htmlTemplate

</td><td>

String

</td><td>

The body HTML code that defines what is rendered when the page is shown. It can contain either static XHTML, dynamically generated content defined as Jelly, or call script includes and UI Macros. This property supports a reference to another file in the application that contains HTML or inline HTML.Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide inline HTML, use string literals or template literals for multiple lines of code: `'HTML' or `HTML``.

Default:

```xml
<div><!-- your widget template --></div>
```

</td></tr><tr><td>

customCss

</td><td>

String

</td><td>

The CSS or SCSS that defines the widget style. This property supports a reference to another file in the application that contains CSS or inline CSS. Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide inline CSS, use string literals or template literals for multiple lines of code: `'CSS' or `CSS``.

</td></tr><tr><td>

dataTable

</td><td>

String

</td><td>

The table in which to store widget instance options. To define a custom option schema, you can add fields to a table that extends the Widget Instance \[sp\_instance\] table and set your widget to use the extension table as a data source. For more information, see [Store instance options in a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/c_WidgetInstanceOptions.md).Default: sp\_instance

</td></tr><tr><td>

demoData

</td><td>

String or Object

</td><td>

Data that demonstrates the widget functionality. This property supports inline strings, a reference to another file in the application that contains JSON, or inline JSON serializable objects.Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide inline JSON, use an object with key and value pairs: `{ key: value }`.

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of the widget and its purpose.

</td></tr><tr><td>

docs

</td><td>

Reference

</td><td>

The variable identifier of the Service Portal documentation \[sp\_documentation\] that provides additional information about the widget and its purpose. To define Service Portal documentation, see [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

fields

</td><td>

Array

</td><td>

A list of column names from the data table to use in the widget option schema.

</td></tr><tr><td>

hasPreview

</td><td>

Boolean

</td><td>

Flag that indicates whether you can preview the widget from the Widget Editor.Valid values:

-   true: You can preview the widget from the Widget Editor.
-   false: You can't preview the widget from the Widget Editor.

Default: false

</td></tr><tr><td>

id

</td><td>

String

</td><td>

A unique ID for the widget. The ID can't contain spaces.

</td></tr><tr><td>

linkScript

</td><td>

Script

</td><td>

A link function that uses AngularJS to directly manipulate the DOM. This property supports inline JavaScript or a reference to another file in the application that contains a script.Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

Default:

```javascript
function link(scope, element, attrs, controller) { }
```

</td></tr><tr><td>

roles

</td><td>

Array

</td><td>

A list of variable identifiers of Role objects or names of roles that can access the widget. For more information, see [Role API - ServiceNow Fluent](role-api-now-ts.md#).

</td></tr><tr><td>

optionSchema

</td><td>

Array

</td><td>

A list of parameters that a Service Portal administrator \(sp\_admin\) can configure for a widget instance. The widget option schema supports reusing a widget and uniquely configuring instances of the widget on different pages. For more information, see [Widget option schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/c_WidgetInstanceOptions.md).```javascript
optionSchema: [
  {
    name: 'String',
    label: 'String',
    section: 'String',
    type: 'String',
    defaultValue: 'String',
    hint: 'String'
  },
...
]
```

-   name: Required. The name of the parameter.
-   label: Required. A label for the parameter that appears in the widget instance options.
-   section: Required. The section of the widget instance options in which the parameter appears.

Valid values:

    -   data
    -   behavior
    -   documentation
    -   presentation
    -   other
-   type: Required. The data type of the parameter.

Valid values:

    -   string
    -   boolean
    -   integer
    -   reference
    -   choice
    -   fieldList
    -   fieldName
    -   glideList
    -   glyphIcon
-   defaultValue: The default value of the parameter.
-   hint: A short description of the parameter that displays as tooltip when hovering over it.

</td></tr><tr><td>

public

</td><td>

Boolean

</td><td>

Flag that indicates whether the widget is available to unauthenticated users.Valid values:

-   true: Unauthenticated users can access the widget.
-   false: Only authenticated users can access the widget.

Default: false

</td></tr><tr><td>

dependencies

</td><td>

Array

</td><td>

A list of variable identifiers of SPWidgetDependency objects or names or sys\_ids of dependencies for the widget. For more information, see [SPWidgetDependency object](fluent-service-portal-api.md#).

</td></tr><tr><td>

angularProviders

</td><td>

Array

</td><td>

A list of variable identifiers of SPAngularProvider objects or names or sys\_ids of Angular providers for the widget. For more information, see [SPAngularProvider object](fluent-service-portal-api.md#).

</td></tr><tr><td>

templates

</td><td>

Array

</td><td>

A list of Angular ng-templates \[sp\_ng\_template\] to associate with the widget. Angular ng-templates contain content that is rendered only when you instruct it to render.```javascript
templates: [
  {
    $id: Now.ID['String' or Number]
    id: 'String'
    htmlTemplate: 'HTML' or `HTML` 
  },
  ...
]
```

-   $id: Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id.

Format: `Now.ID['String' or Number]`

-   id: Required. The ID of the Angular ng-template.
-   htmlTemplate: Required. The HTML template content. This property supports a reference to another file in the application that contains HTML or inline HTML.

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
</table>```javascript
import { SPWidget } from '@servicenow/sdk/core'

SPWidget({
    $id: 'my_simple_widget',
    name: 'My Simple Widget',
    category: 'knowledgeBase',
    clientScript: Now.include('./client.js'),
    serverScript: Now.include('./server.js'),
    controllerAs: '$ctrl',
    customCss: Now.include('./custom_css.css'),
    dataTable: 'sp_instance',
    demoData: { message: 'Hello, World!' },
    description: 'This is a test widget',
    docs: widgetDoc,
    htmlTemplate: Now.include('./template.html'),
    fields: ['color', 'class_name'],
    hasPreview: true,
    id: 'my-simple-widget',
    linkScript: Now.include('./link.client.js'),
    optionSchema: [
        {
            name: 'my_option',
            label: 'My Option',
            type: 'string',
            section: 'behavior'
        }
    ],
    roles: [manager, 'admin'],
})
```

## SPAngularProvider object

Create an Angular Provider \[sp\_angular\_provider\] to reuse components in multiple widgets and improve portal performance.

<table id="table_egv_ymg_kfc" class="parameters"><thead><tr><th>

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

name

</td><td>

String

</td><td>

Required. A name for the Angular provider.

</td></tr><tr><td>

clientScript

</td><td>

Script

</td><td>

A client-side script to reuse in widgets.This property supports inline JavaScript or a reference to another file in the application that contains a script. Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

type

</td><td>

String

</td><td>

The type of Angular provider.Valid values:

-   directive
-   factory
-   service

Default: directive

</td></tr><tr><td>

requires

</td><td>

Array

</td><td>

A list of variable identifiers of other SPAngularProvider objects or names or sys\_ids of Angular providers.

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
</table>```javascript
import { SPAngularProvider } from '@servicenow/sdk/core'
const OTHER_ANGULAR_PROVIDER = 'd11f285fe069e1f119b44bd05c0770aa'

SPAngularProvider({
    $id: 'my_angular_provider',
    name: 'my_angular_provider',
    clientScript: Now.include('my_angular_provider.client.js'),
    type: 'directive',
    requires: [OTHER_ANGULAR_PROVIDER]
})
```

## SPWidgetDependency object

Create a widget dependency \[sp\_dependency\] to link JavaScript and CSS files to widgets and use third-party libraries, external style sheets, or Angular modules.

Dependencies are loaded asynchronously from the server when needed. Widgets can have as many or as few dependencies as needed. However, the more you add, the more content a widget must download to render on the page. Keep dependencies as small as possible for more efficient load times. For more information, see [Create a widget dependency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/widget-dependencies.md).

<table id="table_egv_ymg_kfc" class="parameters"><thead><tr><th>

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

name

</td><td>

String

</td><td>

Required. The name of the widget dependency.

</td></tr><tr><td>

angularModuleName

</td><td>

String

</td><td>

The name of the Angular module to load if the JS include is an Angular module.

</td></tr><tr><td>

includeOnPageLoad

</td><td>

Boolean

</td><td>

Flag that indicates when the dependency loads on a page.Valid values:

-   true: The dependency loads with the initial page load.
-   false: The dependency loads only when the linked widget is loaded on a page.

Default: false

</td></tr><tr><td>

cssIncludes

</td><td>

Array

</td><td>

A list of variable identifiers of CssInclude objects or sys\_ids of CSS includes and their order. For more information, see [CssInclude object](fluent-service-portal-api.md#).```javascript
cssIncludes: [
  {
    order: Number,
    include: 'String' or Reference,
  },
  ...
]
```

</td></tr><tr><td>

jsIncludes

</td><td>

Array

</td><td>

A list variable identifiers of JsInclude objects or sys\_ids of JS includes and their order. For more information, see [JsInclude object](fluent-service-portal-api.md#).```javascript
jsIncludes: [
  {
    order: Number,
    include: 'String' or Reference,
  },
  ...
]
```

</td></tr><tr><td>

portalsForPageLoad

</td><td>

Array

</td><td>

A list of sys\_ids of portals \[sp\_portal\] that load the widget dependency. If empty, the dependency is included on the page load for all portals.

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
</table>```javascript
import { SPWidgetDependency } from '@servicenow/sdk/core'

SPWidgetDependency({
    $id: 'samplejs',
    name: 'Sample',
    angularModuleName: 'samplejs',
    includeOnPageLoad: true,
    portalsForPageLoad: ['b4572a48262a16df3032b48cef75a853', 'fe12dbbed14bd3f712f0787141c2f656'],
    cssIncludes: [
        {
            order: 100,
            include: localCss,
        },
        {
            order: 200,
            include: '94112ccb0fb3c2ed072b01d3cb401196',
        },
    ],
    jsIncludes: [
        {
            order: 100,
            include: localJs,
        },
        {
            order: 200,
            include: 'f8af18a5e6c71a3702c4f2038b43cf62',
        },
    ],
})
```

## CssInclude object

Create a CSS include \[sp\_css\_include\] to reference a style sheet or external CSS in a widget dependency.

<table id="table_egv_ymg_kfc" class="parameters"><thead><tr><th>

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

name

</td><td>

String

</td><td>

Required. The name of the CSS include.

</td></tr><tr><td>

url

</td><td>

String

</td><td>

The URL to an external CSS file. This property is required if a style sheet isn't provided with the spCss property.

</td></tr><tr><td>

spCss

</td><td>

String

</td><td>

The sys\_id of a style sheet \[sp\_css\]. This property is required if an external CSS file isn't provided with the url property.

</td></tr><tr><td>

rtlCssUrl

</td><td>

String

</td><td>

The URL to an external right-to-left \(RTL\) CSS file for mirroring the direction of a widget when the session language is a right-to-left language, such as Hebrew. For more information, see [Styling for right-to-left languages in portals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/styling-right-to-left-languages.md).

</td></tr><tr><td>

lazyLoad

</td><td>

Boolean

</td><td>

Flag that indicates how to load the CSS Include. This property applies only if you use the spCSS property to specify a style sheet.Valid values:

-   true: The CSS include loads asynchronously to improve page load time.
-   false: The CSS include doesn't load asynchronously.

Default: false

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
</table>```javascript
import { CssInclude } from '@servicenow/sdk/core'

const localCss = CssInclude({
    $id: '22bcf16da81e2bc0340c53d50d531adf',
    name: 'Sample Styles',
    spCss: '50e3e32aa321b1c7d1945c5f423228bd',
})
```

## JsInclude object

Create a JS include \[sp\_js\_include\] to reference a UI script or external JavaScript code in a widget dependency.

<table id="table_egv_ymg_kfc" class="parameters"><thead><tr><th>

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

name

</td><td>

String

</td><td>

Required. The name of the JS include.

</td></tr><tr><td>

url

</td><td>

String

</td><td>

The URL to an external JavaScript file. The URL should be an absolute path. This property is required if a UI script isn't provided with the sysUiScript property.

</td></tr><tr><td>

sysUiScript

</td><td>

String

</td><td>

The sys\_id of a UI script \[sys\_ui\_script\]. This property is required if an external JavaScript file isn't provided with the url property.

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
</table>```javascript
import { JsInclude } from '@servicenow/sdk/core'

const localJs = JsInclude({
    $id: '98239e4eadfac88b01cce7daa23b6fc3',
    name: 'Sample Framework',
    sysUiScript: 'b67af05645f738df1f286bb3e9ecd55f',
})
```

