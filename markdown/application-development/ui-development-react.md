---
title: User interface development with React
description: Develop a user interface \(UI\) with the React library to build a full-stack application in source code.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-18"
reading_time_minutes: 5
breadcrumb: [Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# User interface development with React

Develop a user interface \(UI\) with the React library to build a full-stack application in source code.

## Overview of UI development with React

React is an industry-standard web framework for building UI components that you use to develop and render custom user interfaces. A React component is a self-contained, reusable JavaScript function, such as a button, and supports JavaScript \(JS/JSX\) and TypeScript \(TS/TSX\) syntax. For general information about React, see the [React documentation](https://react.dev/learn) on the react.dev website.

With the ServiceNow IDE or ServiceNow SDK, you can use React in your scoped application to create a UI page in ServiceNow Fluent code. The ServiceNow Fluent UI Page API refers to an HTML entry point \(`index.html`\) that loads the page at the endpoint provided. After building and installing the application on an instance, the static assets are stored in the appropriate tables. For an example of a React application in source code, see the [ServiceNow SDK examples](https://github.com/ServiceNow/sdk-examples) GitHub repository. To get started using React, select one of the React templates when creating an application with the ServiceNow IDE or ServiceNow SDK.

**Note:** You can use some Next Experience Components in a React application with the React Wrapper Component Library Node Package Manager \(npm\) package on the [public npm registry](https://www.npmjs.com/package/@servicenow/react-components). To use the React Wrapper Component Library in an application, you can use Build Agent or you must install it from the ServiceNow IDE or ServiceNow SDK. For more information, see [Use third-party libraries with the ServiceNow IDE](../../servicenow-ide/task/use-third-party-libraries-ide.md) or [Use third-party libraries with the ServiceNow SDK](../task/use-third-party-libraries.md).

## UI development process

The following list is a high-level overview of the process to develop a React application with the ServiceNow IDE or ServiceNow SDK:

1.  Create an application and select one of the React templates.

    The application includes the files and directories required for React development.

2.  In the `src/client` directory, add client assets for a user interface, such as an HTML entry point \(`index.html`\), client scripts, and style sheets. The `index.html` file must contain the `<script>` tag as the JavaScript entry point.
3.  Define a UI page \[sys\_ui\_page\] in code with the ServiceNow Fluent UI Page API. In the `now.ts` file that contains the UI page definition, you import the HTML and refer to it from the html property of the UiPage object.
4.  Build the application to execute a pre-build Rollup script that bundles dependencies and packages the client assets in the `src/client` directory before executing the rest of the build process. The standard Rollup build process and plugins are used as the default JavaScript bundler.

    Static assets are output to the `dist/static` directory.

5.  Install the application to add the static assets to the application files \[sys\_metadata\] in the appropriate tables: UX Asset \[sys\_ux\_lib\_asset\], Images \[db\_image\], and UX Theme Asset \[sys\_ux\_theme\_asset\] tables. These tables support adding files as attachments.

    **Important:** UI development with React is an experimental feature due to how content is served from an instance and the content types and tables that are currently supported.


## Limitations

-   The UI page HTML should be modified only in source code. Changes to the HTML of a UI page \[sys\_ui\_page\] on an instance aren't synchronized into source code and are likely to result in unintended behavior.
-   Audio, video, and WASM content types aren't supported.
-   The maximum file size of uploaded attachments is limited by the size configured with **com.glide.attachment.max\_size** system property. For more information, see [Maximum allowed attachment size \[Updated in Security Center 1.3\]](https://www.servicenow.com/docs/access?context=sc-max-allowed-attachment-size&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
-   Output paths must be deterministic.
-   Pre-loading content linked from HTML isn't supported \(`rel="preload"`\).
-   Relative style sheets linked from HTML aren't supported \(`rel="stylesheet"`\). Import style sheets into code instead \(`@import 'path/to/style-sheet'`\).
-   Relative imports in CSS aren't supported.
-   CSS modules aren't supported.
-   Only hash routing is supported by UI pages.
-   Server-side rendering and React server components aren't supported.

## UI page development with React

In a `.now.ts` file in the `src/fluent` directory, a UI page is defined in ServiceNow Fluent code. The HTML of the page is imported from the `index.html` file in the `src/client` directory.

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

In the `index.html` file, the `<script>` tag refers to the `main.jsx` file in the `src/client` directory.

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

In the `main.jsx` file, the imports required for rendering the page and the main application component are included and the entry point of the React application is defined.

```javascript
//main.jsx
import React from 'react'
import ReactDOM from 'react-dom/client'
import App from './app'

const rootElement = document.getElementById('root')
if (rootElement) {
    ReactDOM.createRoot(rootElement).render(
        <React.StrictMode>
            <App />
        </React.StrictMode>
    )
}
```

After building and installing the application, you can open the page from the endpoint provided in the UiPage object \(`https://<instance>/<scope>_incident_manager.do`\), which displays an interface for creating and managing incidents.

![An example UI page for Incident Response Management created with React](../image/servicenow-sdk-react-ui-page.png "Example of a UI page created with React")

**Related topics**  


[UI Page API - ServiceNow Fluent](../reference/fluent-ui-page-api.md#)

[ServiceNow Fluent](servicenow-fluent.md)

