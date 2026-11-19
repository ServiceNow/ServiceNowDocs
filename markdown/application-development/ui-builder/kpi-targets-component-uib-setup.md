---
title: KPI Targets component setup
description: The KPI Targets component enables users to set and review targets on Performance Analytics indicators from Next Experience. Configure the indicators you want to show and indicator targets you want to create. Then configure the information and controls to display.Define the indicator targets that your KPI Targets component should display. Set whether the component can be used to create targets and on which indicator. Configure what the component shows.Several configuration options affect whether a user can create or edit targets. These settings also affect which indicator targets they can create.Specify either the UUID of a single indicator in the Target UUID field or a JSON list of indicator id and label pairs in the KPI List field.You can specify a breakdown and element for KPI Targets. Users create targets on that breakdown and element. The breakdown can be first or second-level.No events are exposed for the KPI Targets component in the Brazil release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/kpi-targets-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# KPI Targets component setup

The KPI Targets component enables users to set and review targets on Performance Analytics indicators from Next Experience. Configure the indicators you want to show and indicator targets you want to create. Then configure the information and controls to display.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your KPI Targets component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "pa-targets-component-tree.png"\] Alt text: KPI Targets list connected component renamed KPI Targets for MyWorkspace

2.  Select the KPI Targets component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the KPI Targets label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## KPI Targets component properties

Define the indicator targets that your KPI Targets component should display. Set whether the component can be used to create targets and on which indicator. Configure what the component shows.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_u4p_xyv_nnb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Query \(Edit Query\)

</td><td>

queryString

</td><td>

A query made to the Target values \[pa\_target\_values\] table about which indicators to show the target cards for. Uses the ServiceNow AI Platform® condition builder, including Related Tables. Default: \[Target\]\[is not\]\[empty\]

</td></tr><tr><td colspan="3">

Grid properties

</td></tr><tr><td>

Show tabs

</td><td>

showTabs

</td><td>

Select whether to show separate tabs for Global \("For everyone"\) and Personal \("For me"\) targets.

</td></tr><tr><td>

Default tab

</td><td>

type

</td><td>

If **Show tabs** is turned on, sets whether to show Global \("For everyone"\) or Personal \("For me"\) targets by default.

</td></tr><tr><td>

Show filters button

</td><td>

showFilters

</td><td>

If turned on, shows the List Settings button. When enabled, a user can decide whether to show current, past, and/or future targets. Default settings are set by the individual Show current, Show past, and Show future properties.Default: true \(on\)

</td></tr><tr><td>

Show current

</td><td>

showCurrentTarget

</td><td>

Setting this on turns **Show current** on by default. Turning off this setting hides the current target whether the Show filters button is on. However, even if the Show filters button is off, users have a **Show all targets in the list** link that overrides the Show current, Show past, and Show future settings for the current session.Default: true \(on\)

</td></tr><tr><td>

Show past

</td><td>

showPastTargets

</td><td>

As Show current, but for expired, past targets.

</td></tr><tr><td>

Show future

</td><td>

showFutureTargets

</td><td>

As Show current, but for targets that don’t become active until a date in the future.

</td></tr><tr><td colspan="3">

Card properties

</td></tr><tr><td>

Show indicator name

</td><td>

showIndicatorName

</td><td>

Shows indicator name for target if 'true.'Default: true

</td></tr><tr><td>

Show target status

</td><td>

showTargetStatus

</td><td>

If true and an indicator has a review date, the status of the target is shown. The target status reflects whether the target trend shows that the target will be met on the review date. If there are not enough scores to make this prediction, the target status indicates this situation.

</td></tr><tr><td colspan="3">

Create new target

</td></tr><tr><td>

Target UUID

</td><td>

uuid

</td><td>

The UUID of a fully specified indicator which a user can apply a target to. For a runtime user to create a target for an indicator, also set **Enable editing** to true.Specify a target UUID or a KPI list, not both.

</td></tr><tr><td>

KPI List

</td><td>

indicatorsList

</td><td>

A JSON list of `{"id":"Indicator id","label":"Indicator name"}` pairs. The user can set a target for any or all of these indicators. Also set **Enable editing** to true.If you specify a **KPI List**, this list overrides the **Target UUID**.

</td></tr><tr><td>

Breakdowns : elements

</td><td>

breakdownElementInfo

</td><td>

A breakdown and an element SysIDs linked by a colon, such as `baec:d625d`. You can also specify a second-level breakdown and element, following another colon. The target is created on this breakdown and element combination.

</td></tr><tr><td>

Average Score

</td><td>

averageScore

</td><td>

Average Score to be used as a baseline for improvement targets. You must specify this value to enable the "averageScore" baseline config option.

</td></tr><tr><td>

Additional baseline filter

</td><td>

additionalBaselineFilter

</td><td>

A function you provide yourself to filter baseline values, such as which values are used to calculate the average score.

</td></tr><tr><td>

Baseline config options

</td><td>

baselineConfigOptions

</td><td>

Allow user to base a new target on a change to the old target or a change to the average score. If neither option is available or selected, the new target is an entered value. Pass an empty array or one or both of \["averageScore", "previousTarget"\], case-sensitive. The previousTarget option only takes effect if a target value is already defined.

</td></tr><tr><td colspan="3">

Additional settings

</td></tr><tr><td>

Enable editing

</td><td>

enableEdit

</td><td>

Enables or disables the ability of a user to change a target value. Security restrictions on setting global targets apply. This property also enables the creation of new targets when the **Target UUID** or **KPI List** property is also set.Default: true

</td></tr></tbody>
</table>## Creating and editing targets

Several configuration options affect whether a user can create or edit targets. These settings also affect which indicator targets they can create.

There are two ways to let a user create and edit targets. First, is to let them change existing targets that the query returns. To do so, activate the **Enable editing** property. At runtime, the user can click a target card to open a dialog for setting a new target value. For a global \("For everyone"\) target, the user must be either an admin or a responsible user for that target. Clicking the following target card opens a dialog for changing the score:

\[Omitted image "kpi-targets-tile-to-click.png"\] Alt text: Target tile in KPI Details component in runtime.

The second way is to let users add a new target value to specific indicators. For example, a user might want to add a personal target to an indicator that has no targets. Users add such targets by selecting Create Target.

\[Omitted image "kpi-details-create-target.png"\] Alt text: Create target button..

Enable the Create Target button by activating the **Enable editing** button. However, users can only add a target this way to indicators that you specify. Specify the UUID of at least one indicator. You can also specify a breakdown and element on that indicator.

### Get and pass indicator UUIDs

Specify either the UUID of a single indicator in the **Target UUID** field or a JSON list of indicator id and label pairs in the **KPI List** field.

#### Before you begin

Role required: ui\_builder\_admin

#### Procedure

1.  Navigate to **Platform Analytics** &gt; **Library** &gt; **Indicators**.

2.  Locate the indicator you are interested in.

    If you cannot find the indicator, it might not be published in the library. To publish it, change a setting on the indicator record. Contact a Performance Analytics admin for assistance.

3.  Select the indicator to open it in KPI Details.

4.  Copy the value of the **var\_uuid** parameter from the KPI Details URL.

    For example, if the KPI Details URL is `https://instance.servicenow.com/now/platform-analytics-workspace/ac_kpi_details/0077c1f3c3353110458f1fec5440ddb7`, the indicator UUID is `0077c1f3c3353110458f1fec5440ddb7`.

5.  Navigate back to the KPI Targets component you are configuring in the UI Builder.

6.  Either:

    -   Enter the indicator UUID in the **Target UUID** field. Users can add targets only to that indicator.
    -   Enter the indicator UUID as part of a UUID/Label pair in the **KPI List** field. Users can choose between the indicators that you specify.
    For example, to give users a choice of adding targets to either the **Number of open incidents** or the **Average age open incidents** indicator, enter the following array:

    `[{"id":"fb007202d7130100b96d45a3ce6103b4","label":"Number of open incidents"},{"id":"88a0b602d7130100b96d45a3ce61030c","label":"Average age open incidents"}]`

    The user then sees an indicator selector in runtime.

    \[Omitted image "kpi-targets-indicator-picker.png"\] Alt text: Selection of indicators for the user to create a target for in runtime.


#### What to do next

You can select a first-level or a second-level breakdown for the indicator or the array of indicators.

### Get and pass breakdown and element UUIDs

You can specify a breakdown and element for KPI Targets. Users create targets on that breakdown and element. The breakdown can be first or second-level.

#### Before you begin

Role required: ui\_builder\_admin

Get the UUID of the indicator or indicators for which you want users to create targets. Indicator UUIDs are described in "Get and pass indicator UUIDs."

#### About this task

Use the PAScorecards API to get the UUIDs of breakdowns and elements. For more information, see [Scorecards API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/c_PerformanceAnalyticsAPI.md). You can also look up this API in the API Reference here on the Developer Site.

For more information about breakdowns and elements, see [Automated breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/automated-breakdowns.md).

**Note:** If a user tries to create a target for an indicator that doesn’t support the breakdown, they get an error message, and no target is created. This situation can occur when you specify an array of indicators to choose from. It can also occur when you specify a second-level breakdown on an indicator that doesn’t support breakdown matrix collection.

#### Procedure

1.  To get a list of the breakdowns for an indicator, pass the indicator UUID and the parameter **sysparm\_include\_available\_breakdowns=true** to the PAScorecards API.

    For example, for the indicator **Number of open incidents**, whose UUID is `fb007202d7130100b96d45a3ce6103b4`, pass the following query to your instance:

    `curl -v -u "user:password" -H "Accept:application/json" "https://instance.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4&sysparm_include_available_breakdowns=true"`

2.  Locate the UUID of the breakdown you want in the JSON output.

3.  To get a list of the elements of a breakdown, pass the indicator UUID and the **sysparm\_breakdown** parameter with the breakdown UUID.

    For example, to get the elements of the Assignment Group breakdown for the Number of open incidents indicator, pass the following query:

    `curl -v -u "user:password" -H "Accept:application/json" "https://<instance>.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4&sysparm_breakdown=baec0752bf130100b96dac808c0739ed"`

4.  Locate the UUID of the element you want in the JSON output.

5.  If you want to specify a second-level breakdown, repeat these steps.

6.  Navigate to the KPI Targets component you’re configuring in UI Builder.

7.  Enter either a first-level or a second-level breakdown and element in the **Breakdowns : elements** field.

    -   For a first-level breakdown, enter `[breakdown UUID]:[element UUID]`.
    -   For a second-level breakdown, enter `[breakdown UUID]:[element UUID]:[level 2 breakdown UUID]:[level 2 element UUID]`.
    For example, for the Assignment Group breakdown and the Service Desk element, enter `baec0752bf130100b96dac808c0739ed:d625dccec0a8016700a222a0f7900d06`. The UUID of the Assignment Group breakdown is `baec0752bf130100b96dac808c0739ed`. The UUID of the Service Desk element is `d625dccec0a8016700a222a0f7900d06`.


## KPI Targets component events

No events are exposed for the KPI Targets component in the Brazil release.

