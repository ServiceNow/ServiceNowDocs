---
title: Product lifecycle data on the timeline
description: The lifecycle data of software models \(of each full version\) and hardware models depend on its type, phase, source, dates, and the associated risk. Understand the conditions and considerations applied to denote the software model risks on the timeline. This knowledge enables you to decode the characters on the timeline.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Product lifecycle data on the timeline

The lifecycle data of software models \(of each full version\) and hardware models depend on its type, phase, source, dates, and the associated risk. Understand the conditions and considerations applied to denote the software model risks on the timeline. This knowledge enables you to decode the characters on the timeline.

## Lifecycle phases on the timeline

The timeline depicts two types of lifecycles, which are publisher and internal. The Publisher Lifecycle information that is shown on the pop-up of the timeline are retrieved from the Software Product Lifecycles \[sam\_sw\_product\_lifecycle\] table for the software and Hardware Model Lifecycle \[cmdb\_hardware\_model\_lifecycle\] table for the hardware. This information is denoted as characters such as S and I on the timeline. S, for example, denotes ServiceNow and I for Internal Lifecycle.

**Note:** Both the hardware and software models are together referred to as product model.

As a SAM user or software model manager, you can [add the software product lifecycle](https://www.servicenow.com/docs/access?context=record-terms-software-licenses&version=australia&pubname=australia-it-asset-management&ft:locale=en-US) to the software product lifecycle table. This table holds the information of the software product, its lifecycle type \(internal or external\), full version, lifecycle phases, start date of the phase, and the risk.

As a hardware model manager, you can add lifecycle data to a hardware model.

**Note:** The start date of a subsequent lifecycle phase marks the end of the previous lifecycle phase. Hence there is no phase end date specified in the lifecycle information pop-up.

If you do not want a lifecycle phase to be rendered on the TPM timeline, then set the **Active** flag of that software product lifecycle record to false. For example, you can have **General Availability**, **End of Extended Support**, and **End of Support** lifecycle phases as three records for **Oracle DB Server** software model in the Software Product Lifecycles list. However, if you do not want **General Availability** phase to be shown on the timeline, you can clear the **Active** check box in the Software Product Lifecycle form for that lifecycle phase record. As a result, the timeline starts with the End of Support phase. Although the lifecycle phase record exists for the software product lifecycle, the lifecycle data will not be rendered on the timeline. Because only active lifecycle records are considered and plotted in the TPM timeline.

## Lifecycle sources on the timeline

The sources of the publisher and internal lifecycle types are generated externally and internally, respectively. The records that are created internally are marked as **I** on the timeline and you cannot edit such product lifecycle source. But, if the publisher is external and if there are more than one publisher source for the same product model, then you can configure your preferred publisher source using the [field mapping functionality](https://www.servicenow.com/docs/access?context=example-field-mapping&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) to the **Sequence** field in the Choices \[sys\_choice\_list\] table.

The timeline shows the publisher sources that fulfill the following conditions:

-   The publisher source with the least sequence number is prioritized and plotted on the timeline.
-   If a product model has multiple publisher sources for its lifecycle phases, then the source with the least Sequence number alone is plotted on the timeline and the rest of the phases are not considered.
-   The first alphabet in the name of the publisher source is plotted on the timeline. However, if there is more than one source beginning with the same letter, then the character is appended with a positive integer. For example, C1 for Central, C2 for Corporate.

## Date range configuration for the lifecycle phases

If you are an admin user, then you can configure the date ranges.

1.  To configure the date ranges, navigate to **System Properties** &gt; **All Properties**.
2.  Click **startRangeOfTPMLifecycle** property name to open the record.
3.  Enter a positive value of your choice for the start range of TPM lifecycle in the timeline.
4.  Click **Update**.
5.  Click **endRangeOfTPMLifecycle** property name to open the record.
6.  Enter a positive value of your choice for the end range of TPM lifecycle.
7.  Click **Update**.

To know more about the Date conditions and the lifecycle phases of the record, see [Date conditions](../reference/date-conditions.md).

## Color-coded timeline to identify product model risks

-   If there are internal as well as publisher records for a phase, then internal overrides the publisher for that phase.
-   The last phase in the timeline takes the risk color and source of the previous phase that is not overridden.

