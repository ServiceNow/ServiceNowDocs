---
title: ServiceNow Studio instance strategy
description: Install ServiceNow Studio on every ServiceNow instance where you develop applications, then define your company's access and deployment strategy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/servicenow-studio-instance-strategy.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Installing ServiceNow Studio, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# ServiceNow Studio instance strategy

Install ServiceNow Studio on every ServiceNow instance where you develop applications, then define your company's access and deployment strategy.

Define your company's instance strategy for ServiceNow Studio by deciding how to manage access. Options include:

-   Grant access to all users in your company.
-   Grant access to a specific group of users.
-   Grant access on a case-by-case basis using a form where users describe the app they want to build. An admin then decides whether to approve access for each request.

Use a non-production instance that is configured similarly to your production instance as your test environment. This configuration enables you to identify issues that may appear when the application is deployed to production.

**Note:** If you plan to clone your production instance to one or more non-production instances, install ServiceNow Studio on your production instance before cloning. For more information, see .

After you establish your instance strategy, complete the following tasks.

1.  Establish and automate your approval or review process.
2.  Select the non-production environment where ServiceNow Studio will run.
3.  Determine how to promote apps from your non-production instance to your test instance, and then to production. Deploy apps using update sets, pipelines, or the Application Repository in ServiceNow Studio.

**Parent Topic:**[Installing ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/installing-servicenow-studio.md)

