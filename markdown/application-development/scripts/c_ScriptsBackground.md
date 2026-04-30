---
title: Scripts - Background module
description: Administrators can use the Scripts - Background module to run arbitrary JavaScript code from the server.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server-side scripting, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Scripts - Background module

Administrators can use the Scripts - Background module to run arbitrary JavaScript code from the server.

The Scripts - Background module consists of the following components.

-   Text box to enter JavaScript.
-   Selector to specify the application scope.
-   **Run script** button.
-   List of available scopes.
-   **Record for rollback?** check box. Selected by default. Creates a rollback context for the script execution. After the script is run, click the **Script execution and recovery available here** link to go to the **Script Execution History** form where you can rollback the script.
-   **Execute in sandbox?** check box. Allows script to run with sandbox like restrictions. If checked, data cannot be inserted, updated, or deleted.
-   **Execute as scriptlet?** check box. Allows the script to execute as a scriplet, which gives the script access to the global scope and any server-side functionality or objects. If the check box is not selected, the script executes in global scope, but does not have access to any server-side functionality or objects.
-   **Cancel after 4 hours** check box. Selected by default. Cancels the script execution if it continues running after four hours.

When a script is run, the instance displays results, information, and error messages at the top of the screen.

**Important:** Running free-form JavaScript can cause system disruption or data loss. Do not run free-form scripts from a production instance.

To stop a transaction, see [View and kill active transaction](https://www.servicenow.com/docs/access?context=t_ViewAndKillAnActiveTransaction&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

For examples of scripts you could run, see [Useful scripts](../../useful-scripts/concept/usefulScripts.md).

**Parent Topic:**[Server-side scripting](c_ServerScripting.md)

