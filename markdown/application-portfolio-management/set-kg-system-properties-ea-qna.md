---
title: Enable Knowledge Graph system properties for the Enterprise Architecture query agent
description: Enable the Knowledge Graph system properties to allow the Enterprise Architecture query agent to generate accurate answers based on your Configuration Management Database \(CMDB\) data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/set-kg-system-properties-ea-qna.html
release: australia
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for Enterprise Architecture \(EA\), Enterprise Architecture]
---

# Enable Knowledge Graph system properties for the Enterprise Architecture query agent

Enable the Knowledge Graph system properties to allow the Enterprise Architecture query agent to generate accurate answers based on your Configuration Management Database \(CMDB\) data.

## Before you begin

Role required: admin

## About this task

The Enterprise Architecture query agent uses the ServiceNow Knowledge Graph to answer questions about CMDB relationships and infrastructure data. To enable this capability, you must set the required Knowledge Graph system properties to `true`. Enable the following system properties:

-   **sn\_kg.description\_generation.enable.cmdb\_rel\_ci**
-   **sn\_kg.query.enable\_cmdb\_rel\_ci**
-   **sn\_kg.description\_generation.enable.non\_production\_envs** — Required only on non-production instances such as development or test environments.

After enabling the properties, the Knowledge Graph runs scheduled jobs that read your CMDB data and generate descriptions and relationships across your instance. Initial data processing time varies based on the volume of data in your instance.

**Important:**

Until Knowledge Graph completes its initial data processing, responses from the Enterprise Architecture query agent that rely on CMDB relationship data may be incomplete or limited. Query results improve progressively as processing continues.

If the Knowledge Graph data processing is in progress, the Knowledge Graph Designer displays a notification. This means that the scheduled jobs required to set up the enterprise graph are still running. The Enterprise Architecture query agent is not available until this process is complete and the notification is no longer displayed. To speed up the process, you can import enterprise graph descriptions from a non-production instance where setup has already completed. For more information, see [Initial setup for Enterprise Graph schema in production instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/initial-setup-for-enterprise-graph-schema.md).

\[Omitted image "ea-qna-kg-setup-banner.png"\] Alt text: Knowledge Graph Designer page showing a setup-in-progress notification banner indicating the Enterprise Graph is not yet available for queries.

For more information on Knowledge Graph configuration, see [Configuration item relationships and Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ci-relationships-knowledge-graph.md) and [Setting up Enterprise graph in sub-production instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/setting-up-global-graph-in-production-instance.md).

## Procedure

1.  Select **All** and in the navigation filter enter **sys\_properties.list**.

2.  Search for and open the **sn\_kg.description\_generation.enable.cmdb\_rel\_ci** system property.

    **Note:** You can similarly search and open the **sn\_kg.query.enable\_cmdb\_rel\_ci** and **sn\_kg.description\_generation.enable.non\_production\_envs** system properties.

3.  Select **here** in the banner, to update the property details.

    \[Omitted image "sys-prop-kg-ea-qna.png"\] Alt text: System property form for sn\_kg.description\_generation.enable.cmdb\_rel\_ci, with a banner alert containing the here link to switch the editing application to Knowledge Graph.

4.  In the **Value** field, set the value to `true`.

5.  Select **Update**.


## Result

Knowledge Graph begins processing your CMDB data using scheduled jobs. After initial processing is complete, the Enterprise Architecture query agent uses the relationships and descriptions in your instance to answer questions about your CMDB data.

**Parent Topic:**[Configure Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/configure-now-assist-ea.md)

**Related topics**  


[Enterprise Architecture query agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/ea-qna-overview.md)

[Use Enterprise Architecture query agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/ea-qna-use.md)

[Configure Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/configure-now-assist-ea.md)

[Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md)

