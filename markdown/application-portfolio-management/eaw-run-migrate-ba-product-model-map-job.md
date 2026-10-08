---
title: Run the Migrate BA Product Model Map job
description: Run this job to migrate existing AI system-to-business application associations to the new Enterprise Architecture for AICT data model after activating the AI Control Tower and Enterprise Architecture integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-portfolio-management/eaw-run-migrate-ba-product-model-map-job.html
release: australia
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 1
breadcrumb: [Working with an application portfolio, Working with Portfolio list view, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Run the Migrate BA Product Model Map job

Run this job to migrate existing AI system-to-business application associations to the new Enterprise Architecture for AICT data model after activating the AI Control Tower and Enterprise Architecture integration.

## Before you begin

Role required: admin

## About this task

This job does not run automatically. This scheduled job is installed with the Enterprise Architecture for AICT plugin. In Enterprise Architecture Workspace versions earlier than 10.1.3, associations between AI systems and business applications were stored in the Enterprise Architecture Workspace map \[sn\_apm\_ws\_ba\_product\_model\_map\]. In version 10.1.3 and later, they're stored in the Enterprise Architecture for AICT plugin's map \[sn\_ea\_aict\_ba\_product\_model\_map\]. If you had this integration active before upgrading, the old table retains your existing associations until you run this job.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open the **Migrate BA Product Model Map from EA Workspace** job.

3.  Select **Execute Now**.


## Result

Your existing AI system-to-business application associations are migrated into the sn\_ea\_aict\_ba\_product\_model\_map table. You can confirm the migration by checking that associations still appear correctly in both Enterprise Architecture Workspace and AI Control Tower.

**Parent Topic:**[Working with an application portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/eaw-work-with-application-portfolio.md)

**Related topics**  


[AI Control Tower integration with Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/eaw-aict.md)

[Components installed with AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-installed-with.md)

[Enterprise Architecture for AICT plugin installation and upgrade considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-ea-common-upgrade-considerations.md)

