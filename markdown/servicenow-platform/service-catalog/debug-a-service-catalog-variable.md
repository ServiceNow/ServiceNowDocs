---
title: Debug a Service Catalog variable
description: Monitor changes in the state and the value of a Service Catalog variable due to catalog client scripts, catalog UI policies, and catalog data lookups. You can diagnose and resolve issues related to such changes, and track client-side scripting errors on this tab.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Debugging Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Debug a Service Catalog variable

Monitor changes in the state and the value of a Service Catalog variable due to catalog client scripts, catalog UI policies, and catalog data lookups. You can diagnose and resolve issues related to such changes, and track client-side scripting errors on this tab.

## Before you begin

Role required: admin or catalog\_adminFeatures available for debugging Service Catalog issues including UI macro customization debugging; variable action logger; variable watcher; item diagnostic report

## Procedure

1.  Enable the JavaScript log and field watcher..

    1.  In the banner, click the settings icon \(![Settings icon](../image/Settings.png)\).

    2.  In the System Settings window, click the **Developer** tab.

    3.  Enable the **JavaScript Log and Field Watcher** option.

        The **JavaScript Log** and **Field Watcher** tabs are displayed in a pane at the bottom of the page. For information about JavaScript logs and fields watcher, see [JavaScript log](https://www.servicenow.com/docs/access?context=c_WritingToTheDebugLog&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) and [Field Watcher](https://www.servicenow.com/docs/access?context=c_FieldWatcher&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) .

    4.  Close the System Settings window.

2.  Navigate to **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**.

3.  In the Catalog Items list, select a catalog item to debug its variables, and click **Try it**.

4.  On the form, right-click a variable field label and select **Watch Variable**.

    The debug icon \(![Debug icon](../image/Debug.png)\) is displayed next to the variable, and the **Field Watcher** tab in the bottom pane is replaced with the **Variable Watcher** tab.

5.  Edit the fields on the **Variable Watcher** tab.

    |Field|Description|
    |-----|-----------|
    |Item|Current catalog item.|
    |Variable|Variable that is being watched.|
    |Type|[Type](../reference/r_VariableTypes.md) of the variable.|
    |Create roles|User type that can create values for the variable.|
    |Write roles|User type that can edit values for the variable.|
    |Read roles|User type that can read values for the variable.|
    |||
    |Reference|Reference table for the variable. Applicable for reference variables.|
    |Reference Qual|Qualifiers to restrict data that is available in the field. Applicable for list collector, lookup multiple choice, lookup select box, and reference variables.|
    |Attributes|Attributes of the variable.|
    |Delete roles|User type that can delete values for the variable.|
    |All|If selected, displays the action log of the variable due to catalog client scripts, data lookups, and catalog UI policies.|
    |Catalog Client Script|If selected, displays the action log of the variable due to catalog client scripts.|
    |Data lookup|If selected, displays the action log of the variable due to data lookups.|
    |Catalog UI Policy|If selected, displays the action log of the variable due to catalog UI policies.|

    ![Screenshot for the Variable Watcher tab](../image/VariableWatcherTab.png "Variable Watcher tab")

6.  To watch another variable, right-click that variable and select **Watch Variable**.

    **Note:** You can watch only one variable at a time.

7.  To stop watching a variable, right-click the variable and select **Unwatch Variable**.

8.  To clear the logs, click the Clear log icon \(![Icon to clear log](../image/ClearLog.png) \).

9.  To resize the pane, click **Small**, **Medium**, or **Large**.

10. To close the pane, click the Close icon \(![Close icon](../image/CloseLog.png) \).


**Parent Topic:**[Debugging Service Catalog](../concept/debugging-service-catalog.md)

