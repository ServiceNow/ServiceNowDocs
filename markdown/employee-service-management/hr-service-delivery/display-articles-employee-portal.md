---
title: Displaying related knowledge articles for completing tasks
description: Display knowledge articles that help in completing HR and Content tasks in the Employee Service Center To-dos page and the HR Ticket page.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Machine learning solutions for HR Service Delivery, Integrate with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Displaying related knowledge articles for completing tasks

Display knowledge articles that help in completing HR and Content tasks in the Employee Service Center To-dos page and the HR Ticket page.

## Related knowledge articles

When the following solution definitions are configured and predictive models are trained, the related knowledge articles are displayed to an employee in Employee Service Center and the HR Ticket page.

-   The related knowledge articles are displayed for an HR task in Employee Service Center and the HR Ticket page, when you train the Similar Knowledge Articles for HR Task \(ml\_x\_sn\_hr\_core\_global\_similar\_knowledge\_articles\_for\_hr\_task\) solution definition.
-   The related knowledge articles are displayed for a Content task in Employee Service Center and HR Ticket page, when you train the Similar Knowledge Articles for Content task \(ml\_sn\_sn\_cd\_global\_similar\_knowledge\_articles\_for\_content\_task\) solution definition.

![Illustration depicting how related knowledge articles are displayed to an employee while performing a task.](../image/related-articles-todo.png)

## Auto training the predictive models

The Similar Knowledge Articles for HR Task and Similar Knowledge Articles for Content Task solution definitions are configured and predictive models are auto trained when the following conditions are met:

-   The Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is installed.
-   The Predictive Intelligence \(com.glide.platform\_ml\) plugin is installed.
-   The Employee Center \(com.sn\_hr\_service\_portal\) plugin is required to display related articles for HR tasks.
-   The Content Delivery \(com.sn\_content\_delivery\) plugin is required to display related articles for Content tasks.
-   The**glide.platform\_ml.auto\_training.enabled** system property is set to true.

You can [manually train the predictive models](hr-predictive-intelligence-train.md) if they are not auto trained by default. After you manually train the predictive models, navigate to the **Service Portal Configuration** module and select the Widget editor. Search for **Recommended articles for to dos**, click **Edit Option Schema**, and add the configured solution definitions in the following widget options:

-   Solution name for Content Task
-   Solution name for HR Task

**Parent Topic:**[Machine learning solutions for HR Service Delivery](../concept/predictive-intelligence-for-hr-service-delivery-1.md)

