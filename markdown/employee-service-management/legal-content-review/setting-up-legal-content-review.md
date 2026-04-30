---
title: Configure Legal Content Review
description: Configure the foundation data to provide Legal Content Review request services to employees who can use these services to submit requests to the legal department.
locale: en-US
release: zurich
product: Legal Content Review
classification: legal-content-review
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Legal Content Review, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure Legal Content Review

Configure the foundation data to provide Legal Content Review request services to employees who can use these services to submit requests to the legal department.

As an administrator, review the installed components and modify them or add new ones as applicable.

-   **[Create or modify a practice area](../../legal-request-management/task/manage-practice-areas.md)**

    Set up the practice areas specific to law practices such as Intellectual Property, Privacy, or Compliance. Associate categories to the practice area and assign a legal department user as the practice area lead.

-   **[Create or modify a legal catalog category](../../legal-request-management/task/add-catalog-categories.md)**

    Create catalog categories to group legal services that employees can use to find a specific legal service request on the Legal Service Portal.

    If you are an existing user and upgrading the application, run the `Fix Content Review Intake Form` fix script to map the new Legal Content Review record producer to the content review category.

-   **[Create or modify a record producer for legal services through Classic environment](../../legal-request-management/task/create-record-producer-legal-request.md)**

    Create record producers to define the intake forms for Legal Content Review request services. These record producers are available in the Legal Operations service catalog on the Legal Service Portal. Employees can use them to submit legal service requests.

-   **[Configure an external storage system for legal requests and legal matters](../../legal-request-management/task/integrate-legal-ext-storage.md)**

    Configure an external storage system to store documents attached to the Legal Content Review requests by the requester or the fulfiller to enable your organization to have a centralized documentation management and retention policy.

-   **[Create or modify a response template for legal services](../../legal-request-management/task/create-lsd-response-template.md)**

    Configure a response template with a reusable message that legal fulfillers can use to send users quick and consistent messages through work notes, comments, emails, or chat conversations.

    Each response template is associated with a table and can be configured to include field variables from that table. You can use a condition builder to specify the conditions that a Legal Content Review request must meet for the template to be usable through the configured channels. For example, you can define a condition to enable response templates only for Legal Content Review requests of type marketing presentation.

    For chat response templates, you can specify a short name that can be used as a shortcut to present the response message to a user quickly.

-   **[Create an email notification](https://www.servicenow.com/docs/access?context=t_CreateANotification&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Create or modify email notifications that are sent when specific events occur for example, when a request is assigned, closed, or canceled, or a message has been posted to request additional information.

-   **[Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    To track dispositions from Legal Content Review requests, add the Legal Disposition \[sn\_lg\_ops\_legal\_disposition\] table as a related list to any Legal Content Review Request form. For more information on adding a related list on a form, see [Add a related list to a form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).


-   **[Install Legal Content Review](../task/install-legal-content-review.md)**  
You can install the Legal Content Review application \(sn\_lg\_cont\_review\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.
-   **[Reconfigure forms to use new components](../task/reconfigure-forms-to-use-new-components.md)**  
As an administrator, after installing Legal Content Review reconfigure forms to use the new content review record producer, catalog category, and content taxonomy.

**Parent Topic:**[Legal Content Review](../reference/legal-content-review.md)

