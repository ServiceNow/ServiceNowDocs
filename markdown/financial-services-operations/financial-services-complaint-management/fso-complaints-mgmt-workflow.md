---
title: Financial Services Complaint Management workflow example
description: The Financial Services Complaint Management application installs an automated workflow for complaint servicing. This workflow enables intake of complaints and routing of cases and tasks to different departments, including the complaint, quality control, and business unit specific agents. The workflow applies to both business and personal complaint service requests.
locale: en-US
release: australia
product: Financial Services Complaint Management
classification: financial-services-complaint-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Complaint Management, Common applications, Financial Services Operations \(FSO\)]
---

# Financial Services Complaint Management workflow example

The Financial Services Complaint Management application installs an automated workflow for complaint servicing. This workflow enables intake of complaints and routing of cases and tasks to different departments, including the complaint, quality control, and business unit specific agents. The workflow applies to both business and personal complaint service requests.

The following diagram shows how the application helps bank agents resolve a complaint request.

![Workflow that shows how a complaint request is resolved using the Complaint management application. For the text description, refer to the workflow steps that follow.](../image/fso-complaints-workflow-example.png "Complaint management workflow")

**Note:** This workflow is built using Process Automation Designer and Flow Designer. The complaint admin can review and customize this predefined flow based on the business needs of your organization.

The following workflow routes the case and tasks for a complaint request to agents in different departments. The agents log in to CSM Configurable Workspace to work on the case and tasks in their queue. The case playbook guides agents through the steps that are needed to resolve customer complaints.

-   **As a customer or branch worker**

    A customer \(consumer or contact\) or a branch worker submits a complaint service request on behalf of a customer.

    **Note:** Consumers can submit a request through the Consumer Service Portal. You must have the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\) activated before your consumers can submit a request.

    A case is initiated based on the request.

-   **As back-office agents**

    After the case is initiated and a complaint agent starts updating the case details using the case playbook, a workflow is triggered automatically. The assignment rules route the associated tasks to the appropriate back-office teams.

    1.  In the case playbook, a complaint agent reviews the case details and adds additional details.
    2.  If the complaint agent requires information from a business unit \(BU\) to resolve the case, the agent can request it from the BU complaint agent.

        The workflow generates a BU complaint task and a BU complaint agent works on it to provide a response.

    3.  If the complaint agent identifies the case as having a legal impact, the workflow generates a legal complaint task.

        A legal complaint agent works on this task to provide a response for the case.

    4.  If the case has a potential regulatory impact, a quality control approval is required.

        The workflow generates a quality control task and a quality control agent works on it to review the complaint details and agent's response for the case and approve it.

    5.  The complaint agent sends out the response to the customer. If the customer accepts the response, the workflow advances to step 6 otherwise it goes back to the complaint agent.

        **Note:** If there's a Customer or Consumer Service Portal for customers, they get a notification for the response on the portal from where they can choose to accept or reject the response.

    6.  The complaint agent records the findings and learnings from the case and closes the complaint case.

The state of the case is set to Closed Complete. The customer can also view the status of the case from the Customer or Consumer Service Portal or another self-service portal.

