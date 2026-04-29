---
title: Document tasks generation
description: Document tasks can be generated either automatically or manually. The tasks get generated in the order defined for the participants.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Document Templates: HR Service Delivery, Using Document Templates, Document Templates, HR Documents, HR Service Delivery, Employee Service Management]
---

# Document tasks generation

Document tasks can be generated either automatically or manually. The tasks get generated in the order defined for the participants.

**Note:** Cancelling an HR case leads to the cancellation of document tasks associated with it. If you do not want the document tasks to be cancelled automatically, navigate to **All** &gt; **System Definition** &gt; **Business Rules** and inactivate the following business rules:

-   Initiate Cancel Document Tasks
-   Cancel Document Tasks

## Automatically

Document tasks are automatically initiated for the participants when you:

-   Select the **Automatically Initiate Document tasks** option on the HR service of a case.

    **Note:** Make sure that the HR template configured in the HR Service has document template associated to it.

-   Change the state of the HR case to **Ready**.

![Enabling case option and selecting document template on HR service.](../image/hr-service-config.png)

## Manually

Document tasks are manually initiated when you click the **Initiate document tasks** button on the **Preview Document** option on the case.

**Note:** The **Initiate document tasks** option does not appear when the **Automatically Initiate Document tasks** option is already enabled on the HR service of a case.

![Initiating document tasks](../image/initiate-tasks.png)

**Note:** Initiating document tasks from a Preview model is not available for a word document template.

**Parent Topic:**[Using Document Templates: HR Service Delivery](../concept/understanding-doc-templates.md)

