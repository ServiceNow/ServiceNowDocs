---
title: Application assessment
description: Set up indicators to measure the usability, cost, quality, performance, and risk of applications. Evaluate and score your business applications based on qualitative inputs. You can translate abstract information of applications based on surveys and assessments into more tangible concrete metrics. These assessments help you make strategic decisions on whether to replace or upgrade applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-portfolio-management/application-assessment.html
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Explore, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Application assessment

Set up indicators to measure the usability, cost, quality, performance, and risk of applications. Evaluate and score your business applications based on qualitative inputs. You can translate abstract information of applications based on surveys and assessments into more tangible concrete metrics. These assessments help you make strategic decisions on whether to replace or upgrade applications.

You can use existing assessment metric types or configure them per your requirements.

Application assessment in Enterprise Architecture evaluates business applications using measurable criteria to produce application scores. These scores help portfolio managers and architects compare applications, identify risks, and prioritize investment or retirement decisions.

The application assessment framework consists of three key components that work together:

-   Assessment indicators define individual evaluation criteria, such as cost, risk, quality, or usability.
-   Scoring profiles group multiple indicators and define how they are weighted for a specific assessment context.
-   Application scores are calculated results that reflect how well an application performs against the selected scoring profile.

-   **[Framework setup for application assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/applications-assessment-overview.md)**  
You can create indicators and score profiles based on which you can assess your applications. Application indicators are business metrics that help derive application scores.
-   **[Job schedule to compute application scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/job-run-compute-application-scores.md)**  
After you set up assessment indicators and scoring profiles, application scores are calculated by a scheduled job. Enterprise Architecture provides a predefined scheduled job that periodically recalculates application scores based on the assigned scoring profiles. An administrator can review or adjust the schedule from the Scheduled Jobs list if needed.
-   **[Visualization of application performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/visualization-application-performance.md)**  
Visualization of the performance of applications in different dimensions on a bubble chart, in a dashboard, and in an application 360 view helps you to take decisions on the applications.

**Parent Topic:**[Exploring Enterprise Architecture \(formerly Application Portfolio Management\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/explore-apm.md)

**Related topics**  


[View all application scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/view-application-scores.md)

[View application indicator scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/view-application-indicator-scores.md)

[Add or edit a scoring profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-create-scoring-profile.md)

[Add or edit an application indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-create-indicator.md)

[Activate or turn off an application or capability indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-enable-or-disable-an-application-indicator.md)

[Add a business capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/add-a-capability.md)

[Update the hierarchy of a business capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/update-hierarchy.md)

