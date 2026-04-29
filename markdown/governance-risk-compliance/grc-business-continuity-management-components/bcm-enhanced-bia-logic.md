---
title: Configuring dictionary, UI policy, and element variables
description: Starting with Release 6.1.x, administrators have the capability to configure different aspects of a dependency. This includes the Dictionary, UI policy, element variables, and UI view. These configurations play a crucial role in determining specific columns, required fields, and overall display in the list view and form view of a dependency within the dependency assessment of a BIA.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Structured workflows for BIAs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configuring dictionary, UI policy, and element variables

Starting with Release 6.1.x, administrators have the capability to configure different aspects of a dependency. This includes the Dictionary, UI policy, element variables, and UI view. These configurations play a crucial role in determining specific columns, required fields, and overall display in the list view and form view of a dependency within the dependency assessment of a BIA.

Dictionary entries \[sys\_dictionary\] serve the purpose of providing additional details for each table and defining the columns on those tables. For more information on Dictionary entries, see [Data dictionary tables](https://www.servicenow.com/docs/access?context=c_DataDictionaryTables&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

UI policies are used to dynamically alter the behavior of information on a form. Administrators can configure the UI policies to show or hide fields, make fields required or read-only based on specific conditions. For more information on UI policies, see [Using UI policies](https://www.servicenow.com/docs/access?context=t_CreateAUIPolicy&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Element variables are employed to define additional data for a record, allowing for more granular control over the behavior and attributes of that record. For more information on Element variables, see [Configure element variables for element definitions](../task/configure-element-variable-uib-ws.md).

View rules are utilized to define the filter condition and execution order for a table, providing a way to customize the view and presentation of data within that table. For more information on View rules, see [Create a view rule](https://www.servicenow.com/docs/access?context=t_CreateAViewRule&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Administrators play a crucial role in configuring the Dictionary, UI policy, element variables, and UI view for a dependency by performing these tasks:

1.  Configuring the Dictionary record in the instance to add required or optional fields, or marking existing fields as required or optional for a dependency.
2.  Configuring the element variables record in the instance to add required or optional element variables.
3.  Configuring the element definitions and UX view rules for the dependency assessment.
4.  Configuring the UI policies to mark the fields in the dependency as required or optional. Starting with release 6.1.x, UI policies are used to designate fields as required or optional for a dependency. A UI policy can be created for a specific element definition or multiple element definitions within the dependency assessment.
5.  Configuring the UI view for both lists and forms to specify the columns displayed in the table's list layout for the list view and form view.
6.  Defining a view rule in the BIA scope. The system determines the UI view displayed for the dependency based on the defined filter condition and execution order in the view rule.

**Note:** Define UI policies and element variables within the BCM core application scope to maintain proper functionality.

The BCM application relies on the configurations of the dictionary, UI policies, glide variables \(element variables\), and view rules to retrieve the required fields for each dependency. Once these configurations are properly set up, the setup process is considered complete.

**Note:** Marking fields as required through client scripts is not supported. Additionally, the **Run Script** option in the UI Policy for marking fields as required or optional is also not supported.

The BCM application automatically completes the dependency assessment when all required fields for a dependency are filled, or if the dependency does not have any required fields.

For detailed instructions on configuring the UI view \[sys\_ui\_view\] table, table list layout, and view rules for both the list view and form view, refer to [KB1645940](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1645940).

## Upgrading from the previous version to Release 6.1.x

During the upgrade process from the previous version to Release 6.1.x, the required fields for the Required Recovery Timeframe are removed from the dictionary. However, it's important to note that the **Required Recovery Timeframe** field is only required for the Applications element variable and is added as part of the UI policy. No other element variables have required fields as part of the dependency assessment.

As administrators, you have the flexibility to configure your own settings to make fields required or optional. Additionally, you can customize the view for the element variables and display different columns based on the element definitions.

When the software is upgraded to Release 6.1.x, the state of each dependency is reevaluated for Business Impact Analyses \(BIAs\) in the **Returned**, **In review**, and **Draft** states. The system performs checks to determine if each dependency has any required fields and if all required fields are filled in. Based on these checks, the state of each dependency is then updated accordingly.

## Executing the fix script

A fix script refers to server-side JavaScript code that administrators execute after installing or upgrading an application. Its purpose is to confirm that any metadata changes made by administrators in the Dictionary, UI policy, or element variables configurations for the BIA dependency are accurately reflected.

To properly update the state of the dependency, administrators must fill in the required fields and then execute the fix script. The execution of the fix script updates the state of the dependency based on the table:

|All required fields are filled|State of the dependency|
|------------------------------|-----------------------|
|No|**Pending**|
|Yes|**Complete**|

If a dependency is in the **Pending** state, the BIA user must fill in the required fields associated with that dependency. Once the required fields are completed, the system automatically marks the overall dependency assessment as complete. Running the fix script after filling in the required fields updates the state of the dependency to **Complete**.

For more information on the fix scripts, see [Fix scripts](https://www.servicenow.com/docs/access?context=c_FixScripts&version=australia&pubname=australia-application-development&ft:locale=en-US).

**Parent Topic:**[Structured workflows for BIAs](bia-tasks-performed-by-bia-owner.md)

