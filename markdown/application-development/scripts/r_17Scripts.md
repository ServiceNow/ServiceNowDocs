---
title: Available script types
description: Scripts can be used in many places. The most important detail is whether the script runs on the client or the server.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2026-03-26"
reading_time_minutes: 5
breadcrumb: [Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Available script types

Scripts can be used in many places. The most important detail is whether the script runs on the client or the server.

<table id="table_j5z_ctr_sq"><thead><tr><th>

Script

</th><th>

Description

</th><th>

Runs on

</th></tr></thead><tbody><tr><td>

Access Control

</td><td>

Determines whether access will be granted for a specified operation to a specific entity.-   type of entity being secured
-   operation being secured
-   unique identifier describing the object

Can be defined by roles, conditional expressions or scripts.

</td><td>

server - script and any condition run on the server

</td></tr><tr><td>

[Ajax Scripts](https://www.servicenow.com/docs/access?context=p_AJAX&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

Enables the client to get data from the server to dynamically incorporate into a page without reloading the whole page.-   Ajax Client Scripts request that information be returned, or that action be taken, or sometimes both
-   Ajax Server Scripts fulfill Ajax Client Script requests

</td><td>

-   client - Ajax Client Scripts run on the client
-   server - Ajax Server Scripts run on the server

</td></tr><tr><td>

[Business Rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

Customizes system behavior-   runs when a database action occurs \(query, insert, update or delete\)
-   the script may run
    -   before or after the database action is performed \(runs as part of the database operation\)
    -   asynchronously \(at some point after the database operation\)
    -   on display \(when displaying the data in a form\)

</td><td>

server - script and any condition run on the server

</td></tr><tr><td>

[Service Catalog UI policies](https://www.servicenow.com/docs/access?context=c_ServiceCatalogUIPolicy&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

</td><td>

Defines the display of a variable set or a catalog item \(from the service catalog\).

</td><td>

-   client - scripts in the "execute if true" field or "execute if false" field run on the client
-   server - all conditions run on the server

</td></tr><tr><td>

[Client Scripts](https://www.servicenow.com/docs/access?context=client-scripts&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

Used for making changes to the appearance of forms, displaying different fields based on values that are entered or other custom display options.-   onLoad means the Client Script runs when the form or page is loaded
-   onChange means the Client Script runs when something specific gets changed AND also when the form or page loads
-   onSubmit means the Client Script runs when the form is submitted

Client Scripts can also be called by other scripts or modules, including UI policies.

</td><td>

client

</td></tr><tr><td>

[Script actions](https://www.servicenow.com/docs/access?context=r_ScriptActions&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)

</td><td>

Contains scripts which run when an event occurs, for example-   approval is cancelled
-   change is approved
-   problem is assigned

Can have a condition which must be true for the script to run. Commonly used to call a Script Include.

</td><td>

server - script and any condition run on the server

</td></tr><tr><td>

Script Includes

</td><td>

Contains scripts which can be functions or classes. These scripts run only when called by other scripts \(often Business Rules\).Any server script which is complicated or reusable should be a Script Include \(especially complicated Business Rules\).

</td><td>

server

</td></tr><tr><td>

[Transform maps](https://www.servicenow.com/docs/access?context=c_CreatingNewTransformMaps&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)

</td><td>

Used for importing data.-   defines mapping relationships between tables
-   can use Business Rules, other scripts and/or other options to import that data

Do not always include scripts.

</td><td>

server

</td></tr><tr><td>

[UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

</td><td>

Creates the ability to choose a specific action such as clicking a button or a link.UI Actions put these items on forms and lists:

-   buttons
-   links
-   context menu items
-   list choices

</td><td>

-   client - when the "Client" box is checked, the script in the script field runs on the client
-   server - when the "Client" box is unchecked, the script in the script field runs on the server
-   client - when the "Client" box is checked, the onClick script is available, which can contain any JavaScript but normally calls a function which is specified in the script field
-   server - all conditions run on the server

</td></tr><tr><td>

UI Context Menus

</td><td>

Defines which "right-click menu" will pop-up in which area, and the menu choices that will be available.**Note:** If you use a left-handed mouse configuration, right-click means "click the other button."

</td><td>

-   client - onShow scripts run on the client
-   client - action scripts run on the client
-   server - dynamic action scripts run on the server
-   server - all conditions run on the server

</td></tr><tr><td>

[UI macros](https://www.servicenow.com/docs/access?context=c_UIMacros&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

Contains modular, reusable components that can contain Jelly and are called by UI pages. They also contain different types of scripts and may be called multiple times on the same page.**Note:** Jelly turns XML into HTML.

</td><td>

-   server - the UI Macro itself executes on the Server
-   server - may contain content that runs on the server \(Jelly expressions or JavaScript inside Jelly constructs\)
-   client - may generate output that runs on the client \(embedded JavaScript within &lt;script&gt; tags\)

</td></tr><tr><td>

[UI Pages](https://www.servicenow.com/docs/access?context=r_UIPages&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

Used to create and display pages, forms, dialogs, lists and other UI components. Can be displayed on a standalone basis, or called as a usable component, as part of a larger page.Can contain

-   Client scripts
-   Processing scripts \(which are server scripts\)
-   HTML,
-   Jelly,
-   UI Macros
-   Other scripts

**Note:** Jelly turns XML into HTML.

</td><td>

-   server - Jelly XML runs on the server to produce HTML
-   client - HTML may contain embedded JavaScript that runs on the client
-   client - client scripts run on the client
-   server - processing scripts run on the server

</td></tr><tr><td>

UI Policies

</td><td>

Defines the behavior and visibility of fields on a form.-   mandatory
-   visible
-   read only

Use UI Policies rather than client scripts whenever possible.

-   UI Policies are always attached to one table
-   UI Policies often have a condition which must be true in order for them to run

</td><td>

-   client - scripts in the "execute if true" field or "execute if false" field run on the client
-   server - all conditions run on the server

</td></tr><tr><td>

UI Properties

</td><td>

Designates what the instance will look like.

</td><td>

-   server - properties set on the server
-   client - the results get rendered on the client

 no scripts

</td></tr><tr><td>

UI Scripts

</td><td>

Contains client scripts stored for re-use. Only used when called from other scripts.Not recommended for use.

</td><td>

client

</td></tr><tr><td>

[Validation Scripts](https://www.servicenow.com/docs/access?context=c_ValidateDateAndTime&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

Validates that values are in a specified format.For example, a validation script can verify that the only value allowed in a specific field is an integer.

</td><td>

client

</td></tr><tr><td>

[Workflow editor](https://www.servicenow.com/docs/access?context=workflow-editor&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)

</td><td>

Used to create or change a workflow. Scripts can be run at any point in a workflow, or different scripts can be run at different points.Scripts also can be found inside every workflow activity and can be modified \(although do so with extreme caution\).

</td><td>

server - script and any conditions run on the server

</td></tr></tbody>
</table>**Parent Topic:**[Scripting](../../topic/c_Script.md)

