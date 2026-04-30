---
title: Playbooks in Service Portal
description: Use playbooks to guide Service Portal users through your business processes.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Designing playbooks, Use, Workflow Studio, Build workflows]
---

# Playbooks in Service Portal

Use playbooks to guide Service Portal users through your business processes.

## Using the widget

The Portal Playbook widget adds playbooks that your Service Portal users can run.

Provide a playbook experience to your Service Portal users for a consumer grade user experience. Requests on portals are surfaced as catalog items, including any playbooks you make available in Service Portal. Embedding a playbook in Service Portal enables:

-   A rich user interface for activities during a business process​
-   Guidance for long business processes
-   Going back and editing any previous steps of a business process
-   Saving long running playbooks for a business process and resuming at a later point
-   Seamless transition for agents and teams to enter a business process
-   Visibility into where you are in a business process
-   Visibility on a specific user's tasks
-   Single admin experience for a whole business process.

Service Portal playbooks are also supported in a mobile interface.

![A running playbook in a Service Portal instance](../images/running-playbook-portal.png)

## Use cases

-   **Business account onboarding**

    Onboarding a new or existing business customer with one or more contacts along with onboarding the services requested such as wire transfers, treasury services. Promote compliance and deliver​ a faster time to value​.

-   **Loan or mortgage application**

    Intake of a new credit card application or loan application for both consumers and corporate programs​. Customer needs the ability to save the application and come back at a loter time to resume application.

-   **Insurance claims**

    Policy holder submitting a new personal auto or home claim for an auto accident or home damage via portal.

-   **Request quote for a new policy​**

    Business customer requesting a quote for small business insurance policy that includes liability and commercial property insurance The customer can start filling in the request and the agent needs the abilith to fill in the remaining on behalf of the customer.

-   **License request**

    Constituents requesting a new license such as a business license, or personal license \(fishing, driving or hunting\) from a government agency via a government portal. These applications typically vary by service and state and constituents need to be guided through request.

-   **Customer cases**

    Cases logged by users who need guidance to select the correct issue and enter all the necessary details, such as instances, steps to reproduce, best time to contact, etc. Enable faster case resolution.


## Life cycle

The general life cycle of a Service Portal playbook can be summarized as:

-   A business process administrator builds the playbook in Workflow Studio. To learn more about building a playbook in Workflow Studio, see [Building playbooks](building-a-process.md).
-   An administrator adds the playbook to a Service Portal page and customizes the playbook runtime experience at the same time through the ServiceNow AI Platform®. To learn more about embedding a playbook in Service Portal and further customizations in the ServiceNow AI Platform®, see [Embed the playbook in Service Portal](../task/embed-playbook-service-portal.md).
-   Service Portal administrators and developers customize the playbook portal page. To learn more about using the Service Portal Designer to customize the playbook portal page, see [Customize the playbook in Service Portal](../task/customize-playbook-service-portal.md).
-   Service Portal end users, also called requesters, launch and run through the playbook. To learn more about launching and running a playbook in Service Portal, see [Run a playbook in Service Portal](../task/run-a-playbook-in-service-portal.md).

-   **[Set up mappings between themes](../task/set-up-mappings-between-themes.md)**  
Make sure that playbooks run as expected in your Service Portal by setting up mappings between your Service Portal theme and the UXF theme used in UI Builder.
-   **[Embed the playbook in Service Portal](../task/embed-playbook-service-portal.md)**  
Add a playbook that Service Portal users can launch and run by creating a Playbook Content Item.
-   **[Customize the playbook in Service Portal](../task/customize-playbook-service-portal.md)**  
Use the Service Portal Designer to customize the playbook runtime experience for Service Portal users.
-   **[Run a playbook in Service Portal](../task/run-a-playbook-in-service-portal.md)**  
Launch a playbook as a Service Portal requestor.

**Parent Topic:**[Designing playbooks](../../workspace/concept/playbook-experience-admins.md)

