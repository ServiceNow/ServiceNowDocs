---
title: Configuring Legal Request Management
description: Configure the foundation data to provide legal request services to employees who can use these services to submit requests to the legal department.
locale: en-US
release: zurich
product: Legal Request Management
classification: legal-request-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configuring Legal Request Management

Configure the foundation data to provide legal request services to employees who can use these services to submit requests to the legal department.

## Configuration overview

1.  [Practice areas](../task/manage-practice-areas.md)

    Set up the practice areas specific to law practices such as Intellectual Property, Privacy, or Compliance. Associate categories to the practice area and assign a legal department user as the practice area lead.

2.  [Catalog categories](../task/add-catalog-categories.md)

    Create catalog categories to group legal services that employees can use to find a specific legal service request on the Legal Service Portal.

3.  [Record producers](../task/create-record-producer-legal-request.md)

    Create record producers to define the intake forms for legal request services. These record producers are available in the Legal Operations Catalog on the Legal Service Portal. Employees can use them to submit legal service requests.

4.  [External storage system](../task/integrate-legal-ext-storage.md)

    Configure an external storage system to store documents attached to legal requests and legal matters . The integration with an external storage system enables organizations to have a centralized documentation management and retention policy.

5.  [Response templates](../task/create-lsd-response-template.md)

    Configure a response template with a reusable message that legal fulfillers can use to send users quick and consistent messages through work notes, comments, emails, or chat conversations.

    Each response template is associated with a table and can be configured to include field variables from that table. You can use a condition builder to specify the conditions that a legal request or legal matter must meet for the template to be usable through the configured channels. For example, you can define a condition to enable response templates only for legal requests of type digital forensics.

    Also, for chat response templates, you can specify a short name that can be used as a shortcut with the slash command to present the response message to a user quickly.

6.  [Email notifications](https://www.servicenow.com/docs/access?context=t_CreateANotification&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) Create or modify email notifications that are sent when specific events occur. Some possible event triggers might be: When a request is assigned to a legal department member to work on, a request is closed or canceled, or a message is posted to get additional information.

    New email notification templates are available for Legal Service Delivery applications from Legal Request Management 4.2.2 version onwards when you also have the Employee Center installed. You can differentiate them from the existing ones by the **EC:** prefix in their names.

    -   These email notifications are active by default for new installations of Legal Request Management 5.0 version and later versions.
    -   These email notifications are inactive by default when you upgrade from Legal Request Management version earlier than 5.0. You must manually activate them while deactivating the existing notifications.

        To activate the email notifications based on the applications installed, the admin can run the following scripts:

        -   `Activate EC email template for legal req`: Activates email notifications for Legal Request Management.
        -   `Activate EC email template for lg matter`: Activates email notifications for Legal Matter Management.
        -   `Activate EC email template lg contracts`: Activates email notifications for Legal Simple Contracts.
        -   `Activate EC email template for Legal COI`: Activates email notifications for Legal Conflict of Interest.
        -   `Activate EC email template for lg stock`: Activates email notifications for Legal Stock Preclearance.
        **Note:** Links in the new email notifications navigate to either Employee Center or Legal Counsel Center based on the user's role:

        -   For requesters, the link in the email opens the Standard Ticket page in the Employee Center portal.
        -   For legal fulfillers, the link in the email opens the record form in the Legal Counsel Center.
7.  [Legal dispositions of legal request or legal matter](../reference/installed-with-legal-request-management.md)

    Add the Legal Disposition \[sn\_lg\_ops\_legal\_disposition\] table, which stores dispositions from legal requests and legal matters, as a related list to any Legal Request or Legal Matter form. For more information on adding a related list on a form, see [Add a related list to a form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).


-   **[Install Legal Request Management](../task/install-legal-request-management.md)**  
You can install the Legal Request Management application \(sn\_lg\_ops\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.
-   **[Configure a practice area table](../task/configure-pa-tables-for-reporting.md)**  
Configure a practice area table so you can use fields from legal request and legal matter tables to include in the Lists section of Legal Counsel Center.
-   **[Create or modify a legal catalog category](../task/add-catalog-categories.md)**  
Create or modify a catalog category to organize your legal catalog items into logical groups in the Legal Operations Catalog.
-   **[Create or modify a practice area](../task/manage-practice-areas.md)**  
Create or modify practice areas for specific areas of law practice, such as Intellectual Property, Privacy, or Compliance.
-   **[Assigning legal request](../task/lsd-lr-assignment-landing.md)**  
Legal requests can be automatically assigned via an assignment rules or Advanced Work Assignment. You can also use Predictive Intelligence to predict the assignment group.
-   **[Activate a system property to close a long-running legal request](../task/activate-sys-prop-close-long-run-leg-req.md)**  
As an admin, activate the `sn_lg_ops.allow_request_closure_with_open_matters` system property to close legal requests even when they’re linked to long-running requests.
-   **[Configure number of records to display in search suggestions](../task/confg-no-of-rec-in-search-suggestions.md)**  
As an administrator, configure the sn\_lg\_cf\_workspace.workspace\_typeahead\_list\_count system property to specify the number of records that appears in the suggestion list of a typeahead search in legal requests.
-   **[Managing record producers for legal services](record-producers-legal-services.md)**  
A record producer helps you set up a legal intake form containing fields that a requester has to fill in and initiate a legal request.
-   **[Configure an external storage system for legal requests and legal matters](../task/integrate-legal-ext-storage.md)**  
Configure an external storage system to store documents attached to legal requests and legal matters.
-   **[Create or modify a response template for legal services](../task/create-lsd-response-template.md)**  
Create or modify a response template with a reusable message that legal fulfillers can use to send users quick and consistent messages. They can use these reusable messages in their assigned legal requests or legal matter forms, as well as in chat sessions or emails.
-   **[Configure an Action for legal services on the Standard ticket page](../task/configure-action-legal-request-lsp.md)**  
Add or modify an Action and its functionality on the Standard ticket page for a legal request.
-   **[Enable and configure AI Search in Legal Service Portal](../task/configure-ai-search-lsd.md)**  
The ServiceNow® AI Search application provides a modern consumer-grade search engine for the Legal Service Portal.
-   **[Delegation of legal duties and approvals](legal-services-delegation.md)**  
Legal fulfillers can delegate their legal duties to other users while they are unavailable. The delegate gets the same level of access as the legal fulfillers to work on their legal requests, legal matters, legal matter tasks, and approvals.

**Parent Topic:**[Legal Request Management](../reference/legal-request-management-landing-page.md)

