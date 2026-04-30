---
title: Installed with Enterprise Architecture \(formerly Application Portfolio Management\)
description: Several types of components are installed with Enterprise Architecture.Tables are added with activation of Enterprise Architecture.Roles are added with activation of Enterprise Architecture.UI policies are added with activation of Enterprise Architecture.Scheduled jobs are added with activation of Enterprise Architecture.Client scripts are added with activation of Enterprise Architecture.Business rules are added with activation of Enterprise Architecture.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Explore, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Installed with Enterprise Architecture \(formerly Application Portfolio Management\)

Several types of components are installed with Enterprise Architecture.

## Tables installed with Enterprise Architecture \(formerly Application Portfolio Management\)

Tables are added with activation of Enterprise Architecture.

<table id="table_khk_y54_rx"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application Bubble Chart \[apm\_bubble\_chart\]

</td><td>

Bubble chart configuration.

</td></tr><tr><td>

Application Service Risk \[sn\_apm\_tpm\_business\_service\_risk\]

</td><td>

Stores risks on an application service for TPM.

</td></tr><tr><td>

Application Category \[apm\_application\_category\]

</td><td>

Application category to which the business application belongs to.

</td></tr><tr><td>

Application Category Group \[apm\_application\_category\_group\]

</td><td>

Group of application categories.

</td></tr><tr><td>

Application Family \[apm\_application\_family\]

</td><td>

All application families.

</td></tr><tr><td>

Indicator \[apm\_metric\]

</td><td>

Indicator definition to capture the indicator scores.

</td></tr><tr><td>

Indicator Score \[apm\_app\_indicator\_score\]

</td><td>

Indicator scores calculated by the engine based on the profile.

</td></tr><tr><td>

Scoring Profile \[apm\_application\_profile\]

</td><td>

Scoring profile definition.

</td></tr><tr><td>

Profile Indicator \[apm\_application\_profile\_indicator\]

</td><td>

Application profile indicator with a weightage numbers to calculate the overall score of a business application.

</td></tr><tr><td>

CI Score \[apm\_app\_score\]

</td><td>

Overall application score calculated by the engine based on the application profile.

</td></tr><tr><td>

Business Application \[cmdb\_ci\_business\_app\]

</td><td>

All business applications.

</td></tr><tr><td>

Application Service Software Model \[sn\_apm\_tpm\_service\_software\_model\]

</td><td>

Stores the software models \(technologies\) underlying each application service.

</td></tr><tr><td>

Goal Contribution Target \[goal\_contribution\_target\]

</td><td>

Goal contribution of a program for the target fiscal year.

</td></tr><tr><td>

Demand Action \[apm\_idea\_action\]

</td><td>

Actions available for submitting a demand.

</td></tr><tr><td>

Risk Parameter \[sn\_apm\_tpm\_risk\_parameter\]

</td><td>

Stores the risk parameters in TPM.

</td></tr><tr><td>

Risk Parameter Score \[sn\_apm\_tpm\_risk\_param\_score\]

</td><td>

Stores the risk parameter scores for each software model in TPM.For example, if there are four parameters, then for each software model there are four records stored in the table.

</td></tr><tr><td>

Software Model Risk \[sn\_apm\_tpm\_software\_model\_risk\]

</td><td>

Stores risks on the software models in TPM.

</td></tr><tr><td>

Hardware Model Risk \[sn\_apm\_tpm\_hardware\_model\_risk\]

</td><td>

Stores risks on the hardware models in TPM.

</td></tr><tr><td>

TRM Product Lifecycle Request \[sn\_apm\_trm\_product\_lifecycle\_request\]

</td><td>

Request for a TRM product lifecycle.

</td></tr><tr><td>

TRM Product Request \[sn\_apm\_trm\_product\_request\]

</td><td>

Request for a TRM product.

</td></tr><tr><td>

TRM Category \[sn\_apm\_trm\_standards\_category\]

</td><td>

TRM category.

</td></tr><tr><td>

TRM Phase \[sn\_apm\_trm\_standards\_phase\]

</td><td>

TRM phase.

</td></tr><tr><td>

TRM Product \[sn\_apm\_trm\_standards\_product\]

</td><td>

TRM Product.

</td></tr><tr><td>

TRM Product Lifecycle \[sn\_apm\_trm\_standards\_product\_lifecycle\]

</td><td>

TRM Product Lifecycle.

</td></tr><tr><td>

TRM Technical debt \[sn\_apm\_trm\_standards\_technical\_debt\]

</td><td>

Technical debts information for TRM products.

</td></tr><tr><td>

Architectural Artifact \[sn\_apm\_architectural\_artifact\]

</td><td>

Name of an Architectural Artifact.

</td></tr><tr><td>

Architectural Artifact Version \[sn\_apm\_architectural\_version\]

</td><td>

Version of an Architectural Artifact.

</td></tr><tr><td>

Architectural Category \[sn\_apm\_architectural\_category\]

</td><td>

Category of an Architectural Artifact.

</td></tr><tr><td>

Related Entities \[sn\_apm\_related\_entities\]

</td><td>

Related entities for Architectural Artifacts.

</td></tr><tr><td>

New Table \[sn\_apm\_ppt\_status\_report\]

</td><td>

APM PowerPoint Status Report Table.

</td></tr><tr><td>

Data Classifications \[cmdb\_data\_classification\]

</td><td>

List of data classifications for information objects.

</td></tr><tr><td>

Data Classification Groups \[cmdb\_data\_classification\_group\]

</td><td>

List of data classification groups for information objects.

</td></tr><tr><td>

Data Classification Mapping \[cmdb\_data\_classification\_mapping\]

</td><td>

Mapping details of the data classification with an information object.

</td></tr></tbody>
</table>## Roles installed with Enterprise Architecture \(formerly Application Portfolio Management\)

Roles are added with activation of Enterprise Architecture.

<table id="table_jgf_j34_px"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_apm.apm\_read

</td><td>

Access to view Enterprise Architecture dashboards provided by the base system and the underlying tables from where the data for the dashboards are retrieved.

</td><td>

Includes pa\_viewer and cmdb\_read roles.

**Note:** Activate the Notify \(com.snc.notify\) plugin to include the notify\_view role.

 View Application 360 dashboard, Application Landscape dashboard, Application Assessments dashboard.

</td></tr><tr><td>

sn\_apm.apm\_user

</td><td>

Access to update applications, view landscape, and roadmap.

</td><td>

Includes pa\_viewer, and certification roles.

**Note:**

-   Activate the Notify \(com.snc.notify\) plugin to include the notify\_view role.
-   Activate PPM Standard \(com.snc.financial\_planning\_pmo\) plugin to create project/program in CBP and TPM. For information on PPM roles, see [Plugins installed with PPM Standard \(Project Portfolio Management\)](https://www.servicenow.com/docs/access?context=plugins-installed-with-PPS-finance&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)

.

 -   View/update applications.
-   [Request to create business applications](../task/balm-request-retire-bus-application.md).
-   View application landscape reports and dashboards.
-   View applications roadmap.
-   View Application 360 dashboard.

</td></tr><tr><td>

sn\_apm.apm\_admin

</td><td>

Create or update application records and access administration activities.

</td><td>

Includes sn\_apm.apm\_user, assessment\_admin, certification\_admin roles.

 -   Create/update/delete application categories.
-   Create/update/delete application families.
-   Create/update/delete business processes.
-   Create/update/delete application indicators.
-   Create/update/delete application score profile.
-   Create/update/delete bubble charts.
-   View application indicator scores and application scores.
-   View application assessment dashboard.
-   View Application 360 dashboard.

</td></tr><tr><td>

sn\_apm.apm\_analyst

</td><td>

Create applications and access landscape and dashboards.

</td><td>

Includes sn\_apm.apm\_admin and treemap\_user roles.

**Note:** Activate PPM Standard \(com.snc.financial\_planning\_pmo\) plugin to create project/program in Capability-Based Planning \(CBP\) and Technology Portfolio Management \(TPM\). For information on PPM roles, see [Plugins installed with PPM Standard \(Project Portfolio Management\)](https://www.servicenow.com/docs/access?context=plugins-installed-with-PPS-finance&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US).

 -   Create/update/delete applications.
-   Create/update/delete application indicator scores.
-   Create/update/delete application scores.
-   Create/update/delete Enterprise Architecture programs and targets.
-   Create/update/delete goals.
-   Access the Enterprise Architecture Service Portal pages for program navigation, category analysis, bubble chart view, application comparisons.
-   Create demand with application strategy related attributes.
-   View Application 360 dashboard.

</td></tr></tbody>
</table>## UI policies installed with Enterprise Architecture \(formerly Application Portfolio Management\)

UI policies are added with activation of Enterprise Architecture.

|UI policy|Table|Description|
|---------|-----|-----------|
|When data source is not PA|Application Indicator \[apm\_metric\]|Shows the **Result precision** field when the data source is not PA.|
|When query condition is data source|Application Indicator \[apm\_metric\]|Shows the **Query table**, **Consolidate**, **Aggregate type**, **Aggregate**, **Conditions and Group By** fields when the data source is custom script.|
|When Assessments and Surveys are data source|Application Indicator \[apm\_metric\]|Shows the **Normalization script****Metric Type** and **Metric Category** fields when the data source is Assessments and Surveys.|
|When PA is data source|Application Indicator \[apm\_metric\]|Shows the **Source PA indicator** and **Frequency and Default breakdown** fields when the data source is PA.|
|When data source is custom script|Application Indicator \[apm\_metric\]|Shows the **Custom Script** field when the data source is custom script.|

## Scheduled jobs installed with Enterprise Architecture \(formerly Application Portfolio Management\)

Scheduled jobs are added with activation of Enterprise Architecture.

<table id="table_nyh_hjs_rx"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business Application Certification On Demand

</td><td>

Schedules a certification task and the certification schedule is run on demand.

</td></tr><tr><td>

Business Application Certification Quarterly

</td><td>

Schedules a certification task and the certification schedule is run periodically every quarter.

</td></tr><tr><td>

Business Applications not related to any Business Capability audit

</td><td>

Checks the CI relationship \[cmdb\_rel\_ci\] table for business applications that are not related to any business capability.

</td></tr><tr><td>

Business Applications not related to any Software Model

</td><td>

Checks the CI relationship \[cmdb\_rel\_ci\] table for business applications that are not related to any software model.

</td></tr><tr><td>

Business Applications related to multiple Business Capabilities in the same hierarchy

</td><td>

Checks the CI relationship \[cmdb\_rel\_ci\] table for a possibility where the same business application is tied to multiple business capabilities at the same level of the hierarchy.

</td></tr><tr><td>

Load Application Indicators and compute Application Scores

</td><td>

Populates application indicator score and calculates application scores based on the scoring profile attached to the business application.

</td></tr><tr><td>

Load TPM Risk Parameters and compute Application Service Risks

</td><td>

Calculates the software model risk and the business application risk.

</td></tr><tr><td>

Orphaned Business Capabilities

</td><td>

Checks for capabilities that have neither parent capability nor child capabilities, and do not have any business applications related to it.

</td></tr><tr><td>

Software Products with no lifecycle data\(for product models that are used by the business applications\)

</td><td>

Retrieves software model records used by the business applications and then checks if life-cycle data is present for the products related to these software models.

</td></tr><tr><td>

Update Business Capability Levels and Hierarchy IDs

</td><td>

Updates the order and hierarchy of the business capabilities in the Capability map.

</td></tr><tr><td>

Populate TRM Technical debt for production applications

</td><td>

Populates data in the TRM technical debts table.

</td></tr></tbody>
</table>## Client scripts installed with Enterprise Architecture \(formerly Application Portfolio Management\)

Client scripts are added with activation of Enterprise Architecture.

|Client script|Table|Description|
|-------------|-----|-----------|
|Mark **Goal** mandatory with respect to Enterprise Architecture view|Program \[pm\_program\]|Marks **Goal** mandatory with respect to Enterprise Architecture view.|
|Defaulting comments for scripted indicator|Application Indicator \[apm\_metric\]|If the **Data Source** field is Custom script, then the **Custom script** field is populated with the sample custom script.|
|Populate CI manufacturer for applications|Business Application \[cmdb\_ci\_business\_app\]|Populates manufacturer for business application.|
|Set view in Enterprise Architecture to true|Program \[pm\_program\]|Sets the **Used by Enterprise Architecture** check box to true.|
|Set mandatory attributes for Enterprise Architecture goals|Goal \[goal\]|Sets mandatory attributes for Enterprise Architecture goals.|
|Restrict Sustain|Demand Action \[apm\_idea\_action\]|Restricts sustain from the list of strategies.|

## Business rules installed with Enterprise Architecture \(formerly Application Portfolio Management\)

Business rules are added with activation of Enterprise Architecture.

|Business rule|Table|Description|
|-------------|-----|-----------|
|Populate **Short Description**|Goal \[goal\]|Populates **Short Description** of the goal based on the attributes provided.|
|PA Indicator frequency check|Indicator \[apm\_metric\]|Checks the frequency of the performance analytic indicators.|
|Only one Enterprise rollout is allowed|Business Entity \[apm\_rollout\_entity\]|Allows only one enterprise rollout for a business application.|

