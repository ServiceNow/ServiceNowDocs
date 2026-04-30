---
title: End of Life \(EOL\) and End of Support \(EOS\) life cycles
description: In the absence of vendor-provided life cycles, use calculated life cycles to assess and manage your risks by creating EOL and EOS life cycles for your software products. You can also use approximated dates to improve life cycle coverage.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# End of Life \(EOL\) and End of Support \(EOS\) life cycles

In the absence of vendor-provided life cycles, use calculated life cycles to assess and manage your risks by creating EOL and EOS life cycles for your software products. You can also use approximated dates to improve life cycle coverage.

## Calculated life cycles

You can create EOL and EOS life cycles based on industry averages, measured in months, from the General Availability \(GA\) dates.

**Note:** The life cycles can be created by the sam\_user or the sam\_admin role.

You can override the global industry averages by specifying custom values pertaining to a product or a publisher. The life cycles are calculated based on the product or publisher values that you specified. For details on specifying custom values in the Software Asset Workspace, see [Create averages for product life cycles in workspace](../task/create-lifecycle-averages-workspace.md), and for specifying values in the Software Asset Management classic application, see [Create averages for product life cycles in Software Asset Management classic](../task/create-lifecycle-averages-classic.md).

When creating EOL or EOS life cycles, keep the following pre-requisites in mind:

-   The Software Asset Management Professional \(com.sn\_samp\_master\) plugin must be activated.
-   GA dates available for the product.
-   EOL and EOS life cycles not provided by the Content Service.
-   Product is shipped by the Content Service.

## Software life cycle process

The scheduled job **SAM - Generate Software Lifecycle Report** collects data for life cycles for products whose GA dates are available and published by the Content Service. This scheduled job checks if all these GA records have an EOL or EOS life cycle record associated with them. If no EOL or EOS life cycle record is created by you or the Content Service, then calculated EOL or EOS life cycle records are created by another scheduled job, **SAM - Create Calculated Software Lifecycles**.

For the scheduled job **SAM - Create Calculated Software Lifecycles** to generate life cycles, keep the following in mind:

-   If domain separation is disabled, enable the **com.snc.samp.generate.calculated.lifecycles** system property in the System Property \[sys\_properties\] table.
-   If domain separation is enabled, use the Application Properties \[sys\_application\_properties\] table to enable the **com.snc.samp.generate.calculated.lifecycles**\) property. In the Application Properties \[sys\_application\_properties\] table, click the **com.snc.samp.generate.calculated.lifecycles** property to open the Application Properties page. Scroll down to **Application Property Values** and click **New** to create a record. The **Application Property** and **Domain** fields are pre-filled with values. In the **Value** field, enter **true** and click **Submit**. You also need to enable reconciliation by specifying the value of the column **Run asset process \[run\_asset\_process\]** to be true in the Domain Asset Process Setting \[alm\_domain\_asset\_process\_setting\] table.

    **Note:** Reconciliation can be enabled either for the parent domain or for the child domain; it cannot be enabled for both the parent and the child domains.


The calculated life cycles and the life cycles created by you are stored in the Custom Software Product Lifecycle \[sam\_custom\_sw\_product\_lifecycle\] table. Life cycles created by the Content Service are stored in the Software Product Lifecycle \[sam\_sw\_product\_lifecycle\] table.

The industry averages are stored in the Software Lifecycle Averages \[samp\_sw\_lifecycle\_averages\] table. The life cycles created using these averages have their source column defined as **calculated**.

**Note:** If you create an EOS or EOL record, then an EOL or EOS created by the scheduled job gets deleted in the next Content Service update, as priority is given to the custom records that you create. Similarly, if the scheduled job creates EOL and EOS records and then you create custom records, the records created by the scheduled job are deleted in the next Content Service update, as the custom records take precedence.

Once created, the EOL and EOS life cycles are visible in the software model page.

**Note:** If a sam\_user or sam\_admin deletes an EOL or EOS life cycle on a software model, the life cycles are not reinstated back to the software model.

## Approximate dates for life cycles and life cycle codes

To improve life cycle report coverage, approximate life cycles dates are assigned to life cycles without a date.

Select the system property \(com.snc.samp.use\_lifecycle\_approximation\), to include the approximate life cycle dates when generating the life cycle report. For details on this property, see [Software Asset Management properties](../reference/sam-properties.md).

The new table, Software Lifecycle Code \[software\_lifecycle\_code\], contains all the approximation codes along with a description of each code. For a detailed explanation of life cycle codes, see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB1642485](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1642485).

A new column, Lifecycle code, is added to the Software Product Lifecycle \[sam\_sw\_product\_lifecycle\] table. The Lifecycle code column refers to the Software Lifecycle Code \[software\_lifecycle\_code\] table if approximate dates are assigned to a life cycle. The lifecycle code column is empty if the lifecycle has confirmed dates.

For better visibility of all the life cycle phases, the following columns have been added to the Software Lifecycle Reports \[sam\_sw\_product\_lifecycle\_report'\] table

-   General Availability start date
-   General Availability
-   End of Support start date
-   End of Support lifecycle
-   End of Extended Support start date
-   End of Extended Support lifecycle
-   End of Life start date
-   End of Life lifecycle
-   Software model
-   Owners

EOL, EOS, and End of Extended Support dates for all build versions are not shipped by the Content Service. The life cycle report inherits such dates from the generic version.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

