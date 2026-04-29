---
title: Product life cycles
description: In the absence of vendor-provided life cycles, there are various capabilities that the Software Asset Management application provides to improve life cycle coverage.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Product life cycles

In the absence of vendor-provided life cycles, there are various capabilities that the Software Asset Management application provides to improve life cycle coverage.

## Overview of product life cycles

The Content Library provides approximated life cycle dates and life cycle codes which you can use to drive your life cycle reporting.

You can also use calculated life cycles to create end-of-support \(EOS\), end- of-extended-support \(EOES\), and end-of-life \(EOL\) life cycles for your software products. Additionally, you can create custom life cycles to supplement missing life cycles or overwrite any existing ones from the Content Library.

## Software Product Lifecycles table

The Software Product Lifecycles \[sam\_sw\_product\_lifecycle\] table holds the information of the software product, its lifecycle type \(internal or external\), full version, lifecycle phases, start date of the phase, and the risk.

The Content active column in the Software Product Lifecycles \[sam\_sw\_product\_lifecycle\] table is set to the value true by the Software Asset Management content service if the lifecycle records are valid. If you do not want a lifecycle phase to be rendered on the Technology Portfolio Management \(TPM\) timeline, then set the **Active** column to false. For example, you can have **General Availability**, **End of Extended Support**, and **End of Support** lifecycle phases as three records for Oracle DB Server software model in the Software Product Lifecycles list. However, if you do not want **General Availability** phase to be shown on the timeline, you can clear the **Active** check box in the Software Product Lifecycle form for that lifecycle phase record. As a result, the timeline starts with the **End of Support** phase. Although the lifecycle phase record exists for the software product lifecycle, the lifecycle data will not be rendered on the timeline. Because only active lifecycle records are considered and plotted in the TPM timeline.

View the Software Product Lifecycle report to be informed about the products nearing end-of-life, end-of-support, and end-of-extended support. View the report by navigating to **Reports** &gt; **View/Run**. The report is based on the scheduled job, **SAM - Generate Data For Software Lifecycle Report**.

## Software Lifecycle Report table

The Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\] table calculates the current and upcoming lifecycle phases from the lifecycle phases mentioned in the Software Product Lifecycle \[sam\_sw\_product\_lifecyle\] table.

For records with the same publisher, product, version, full version, and edition, there's a single record for different lifecycle phases. This helps in avoiding duplicate software installation count for each lifecycle phase. You can export lifecycles from the Software Installation \[cmdb-sam-sw-install\] table. The software installation records are linked to lifecycles via the **Installs associated to lifecycle** column in the Software Installation \[cmdb-sam-sw-install\] table.

For better visibility into all life-cycle phases, the following columns have been added to the Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\] table:

-   Current phase \[current\_lifecycle\_phase\]
-   Current phase start date \[current\_lifecycle\_phase\_start\_date\]
-   Upcoming lifecycle phase \[upcoming\_lifecycle\_phase\]
-   Upcoming lifecycle phase start date \[upcoming\_lifecycle\_phase\_start\_date\]
-   General availability start date \[ga\_start\_date\]
-   End of support start date \[eos\_start\_date\]
-   End of extended support start date \[eoes\_start\_date\]
-   End of life start date \[eol\_start\_date\]

## Approximated life cycles and life-cycle codes

Approximated life cycles are provided by the Content Library when life cycle dates are not explicitly published by the publisher. The life cycle record may contain an actual date \(through various methods of approximation\) or an explanation as to why the date could not be provided. This explanation is captured in the Lifecycle codes.

The Software Lifecycle Code \[software\_lifecycle\_code\] table, contains all the approximation codes along with a description of each code. For a detailed explanation of life-cycle codes, see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB1642485](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1642485).

A new column, Lifecycle code, is added to the Software Product Lifecycles \[sam\_sw\_product\_lifecycle\] table. This column refers to the Software Lifecycle Code \[software\_lifecycle\_code\] table. If the column is populated, it indicates the record is an approximated lifecycle. If the column is empty, it indicates that the life cycle record has confirmed or explicit dates as published by the publisher.

Approximated life cycles are enabled by default as part of generating the Software Lifecycle Report. This is managed in the system property **com.snc.samp.use\_lifecycle\_approximation**. For details on this property, see [Software Asset Management properties](../reference/sam-properties.md).

Life cycle code columns can also be added to the Software Lifecycle Report for each life cycle phase \(GA, EOS, EOES, and EOL\). This may require dot-walking the columns from the Software Lifecycle Code table. You should be able to identify which life cycle phase is approximated based on the existence of the codes.

## Calculated life cycles

To further improve life cycle coverages, even after approximated life cycles have been considered, EOS, EOES, and EOL life-cycle dates can be calculated based on software life cycle averages, measured in months, from the GA dates.

Software life cycle averages can be defined at the product level, publisher level, or industry level. For details on specifying software life cycle averages in the Software Asset Workspace, see [Create averages for product life cycles in workspace](../task/create-lifecycle-averages-workspace.md) and for specifying software life cycle averages in the Software Asset Management classic application, see [Create averages for product life cycles in Software Asset Management classic](../task/create-lifecycle-averages-classic.md)

You can override the GA date provided by ServiceNow by creating a custom GA date. The custom GA date always takes priority over the GA date provided by ServiceNow. The life cycles are calculated based on the product or publisher values that you specified. Life cycle dates are defined only at the generic version and not the full version. For details on specifying custom values in the Software Asset Workspace, see [Create averages for product life cycles in workspace](../task/create-lifecycle-averages-workspace.md), and for specifying values in the Software Asset Management classic application, see [Create averages for product life cycles in Software Asset Management classic](../task/create-lifecycle-averages-classic.md).

Software life cycle averages are stored in the Software Lifecycle Averages \[samp\_sw\_lifecycle\_averages\] table. Lifecycle records created using these averages have their source column defined as calculated.

**Note:** Life cycle averages can be created by the sam\_user or the sam\_admin role.

Calculated life cycles come with the following prerequisites:

-   The Software Asset Management Professional \(com.sn\_samp\_master\) plugin must be activated.
-   GA dates available for the product either provided by the Content Service or custom GA dates that you created.
-   EOS, EOES, and EOL life cycles are not provided by the Content Service.
-   Product is shipped by the Content Service.
-   Life cycle dates are defined only at the generic version and not the full version.

## Custom life cycles

Besides approximated life cycles and calculated life cycles, to further improve your life cycle coverage you can also create custom life cycles. Custom life cycles are records that you define at each life cycle phase for the product and version that you selected. You can type in the dates directly in the date fields, and these dates will take priority in the Software Lifecycle Report generation. You can also use this capability to overwrite an existing life cycle record that was provided by the Content Library.

Custom life cycles can be created from either of the two locations on selecting **New**:

-   Software Product Lifecycles \[sam\_sw\_product\_lifecycle\] table.
-   Custom Software Product Lifecycle \[sam\_custom\_sw\_product\_lifecycle\] table.

## Publisher add-on life cycles

Software publishers offer various add-ons and optional support that can extend the life cycles of their existing products. The Software Asset Management Content Service maintains life-cycle information for both the standard version of each software product and any available add-ons or optional support in the Software Product Lifecycle \[sam\_sw\_product\_lifecycle\] table. To track life cycles more accurately, you can indicate if you have purchased any add-ons or optional support for your software products. The Software Asset Management application then uses the corresponding life-cycle information in the Software Product Lifecycle \[sam\_sw\_product\_lifecycle\] table to automatically update the life-cycle dates of those products with the extended life-cycle dates of the add-ons or optional support. These updated life-cycle dates are populated in the Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\] table. For more information, see [Use publisher add-on lifecycles in the Software Lifecycle Report](../task/specify-publisher-add-on-lifecyles.md).

## Software life-cycle process

The scheduled job **SAM - Generate Software Lifecycle Report** aggregates life cycle data for all normalized software products which have non- zero installation counts. Each record on the Software Lifecycle Report table displays all life cycle phase columns along with their corresponding phase start dates, if the date is available. Life cycle codes can also be displayed to indicate whether the record is an approximated life cycle or not.

The Software Lifecycle Report table also displays the Current Phase and Upcoming Phase columns along with their corresponding dates. For further details about these columns, see [Software models and Software entitlements](software-models-and-entitlements.md).

Another scheduled job, **SAM - Create Calculated Software Lifecycles**, checks for all records on the Software Lifecycle Report table which have GA dates but are missing EOS, EOES, or EOL dates and creates calculated life cycles for them based on the definitions that you have created on Software Lifecycle Averages table.

Keep the following in mind for the scheduled job **SAM - Create Calculated Software Lifecycles** to generate life cycles:

-   If domain separation is disabled, enable the **com.snc.samp.generate.calculated.lifecycles** system property in the System Property \[sys\_properties\] table.
-   If domain separation is enabled, use the Application Properties \[sys\_application\_properties\] table to enable the **com.snc.samp.generate.calculated.lifecycles** property. In the Application Properties \[sys\_application\_properties\] table, select the **com.snc.samp.generate.calculated.lifecycles** property to open the Application Properties page. Scroll down to **Application Property Values** and select **New** to create a record. The **Application Property** and **Domain** fields are pre-filled with values. In the **Value** field, enter **true** and select **Submit**. You also need to enable reconciliation by specifying the value of the column **Run asset process \[run\_asset\_process\]** to be true in the Domain Asset Process Setting \[alm\_domain\_asset\_process\_setting\] table.

    **Note:** Reconciliation can be enabled either for the parent domain or for the child domain; it cannot be enabled for both the parent and the child domains.


The calculated life cycles and the life cycles created by you are stored in the Custom Software Product Lifecycle \[sam\_custom\_sw\_product\_lifecycle\] table. Life cycles created by the Content Service are stored in the Software Product Lifecycles \[sam\_sw\_product\_lifecycle\] table.

If you create custom life cycles, calculated life cycles crated by the scheduled job gets deleted in the next Content Service update, as priority is given to the custom life cycles that you created.

Once created, the EOS, EOES, and EOL life cycles are visible in the software model page.

**Note:** If a sam\_user or sam\_admin deletes an EOS, EOES, or EOL life cycle on a software model, the life cycles aren’t reinstated back to the software model.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

