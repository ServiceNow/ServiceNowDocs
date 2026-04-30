---
title: Setup checklist for the ESG Management application
description: This checklist includes the set up tasks that you are required to complete in your ServiceNow AI Platform instance. When you have completed these tasks, the base system is ready for operation.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [ESG Management implementation, Configuring ESG Management, Environmental, Social, and Governance Management]
---

# Setup checklist for the ESG Management application

This checklist includes the set up tasks that you are required to complete in your ServiceNow AI Platform® instance. When you have completed these tasks, the base system is ready for operation.

## Before you begin

Role required: none

Consider creating and printing a PDF of this checklist topic. You can then check off tasks as you complete them. To generate a PDF, click the **Save As PDF** ![Save as PDF icon](../images/save-as-pdf.png)icon and at the top of the topic and click **Selected topic**.

<table id="table_rzz_z21_xmb"><thead><tr><th>

Item

</th><th>

Checklist

</th></tr></thead><tbody><tr><td>

![checkbox](../images/checkbox.png)

</td><td>

A user with the sn\_esg.program\_manager role, can download and install the ESG Management application. For details, see [Install ESG Management](install-esg.md).

</td></tr><tr><td>

![checkbox](../images/checkbox.png)

</td><td>

A user with the sn\_esg.program\_manager role performs the following tasks:-   [Creates material topics](create-material-topics.md)
-   [Creates goals](create-esg-goal.md)
-   [Creates targets](create-esg-target.md)
-   [Creates an emission activity](create-an-emission-activity.md)
-   [Creates an emission factor](create-an-emission-factor.md)

</td></tr><tr><td>

![checkbox](../images/checkbox.png)

</td><td>

A user with the sn\_esg.program\_manager role also manages entities and performs the following tasks:-   [Creates an entity](create-entity.md)
-   [Creates an entity type](create-entity-type.md)
-   [Creates an entity class](create-entity-class.md)

</td></tr><tr><td>

![checkbox](../images/checkbox.png)

</td><td>

A user with the sn\_esg.metrics\_manager role defines the various types of metric definitions and metrics. This user performs the following tasks:-   [Creates an automated metric definition](../../metrics/task/update-automated-metric-definition.md)
-   [Creates a manual metric](../../metrics/task/create-manual-metric-definition.md)
-   [Creates a composite metric definition](../../metrics/task/create-composite-metric-definition.md)
-   [Create a metric](../../metrics/task/create-a-metric.md)

</td></tr><tr><td>

![checkbox](../images/checkbox.png)

</td><td>

A user with the sn\_esg.data\_owner role can provide data for the manual metrics data tasks and a user with the sn\_esg.program\_manager can override the data that is provided. For more information, see [Provide data for a metric data task](../../metrics/task/provide-data-for-metric-data-task.md)

</td></tr><tr><td>

![checkbox](../images/checkbox.png)

</td><td>

A user with the sn\_esg.reporting\_disclosure\_manager, sn\_esg.program\_manager roles can create disclosure. Disclosures enable the investors to make informed decisions about the companies, their risk posture, sustainability standards, and ESG Management compliance.

</td></tr><tr><td>

![checkbox](../images/checkbox.png)

</td><td>

Optionally, users of the [Install ESG Management](install-esg.md) application can integrate with other applications such as Project Portfolio Management and Integrated Risk Management. These integrations provide more features and capabilities. For more information, see [Integrating ESG Management with other applications](../concept/integrate-esg.md)

</td></tr></tbody>
</table>**Parent Topic:**[ESG Management implementation](../concept/esg-implementation.md)

