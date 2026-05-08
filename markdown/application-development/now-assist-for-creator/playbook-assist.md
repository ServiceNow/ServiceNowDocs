---
title: Exploring Now Assist for Playbooks
description: Use Now Assist to generate playbook outlines from text or image inputs. For example, you can enter a text description to generate a playbook outline for managing customer support cases. Playbook Assist is part of the Now Assist for Creator application.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Playbook generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Exploring Now Assist for Playbooks

Use Now Assist to generate playbook outlines from text or image inputs. For example, you can enter a text description to generate a playbook outline for managing customer support cases. Playbook Assist is part of the Now Assist for Creator application.

Now Assist for Creator activates the playbook generation skill. Playbook generation gives generative AI capabilities to playbook authors.

Playbook authors can provide text directions to create multi-stage playbooks with placeholder activities \(![placeholder activity icon.](../images/placeholder-activity-icon.png)\).

**Note:** Playbook generation uses placeholder activities in your playbook. [Configure each activity](../task/generate-a-playbook-outline.md) before activating your playbook.

![Choose an activity definition for the placeholder activity.](../images/configure-placeholder-activity.png)

## Activation

Playbook generation is a skill that is installed with the Now Assist for Creator \(sn\_now\_creator\) application. You can install this application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Supported Now Assist skills

Playbook Assist currently only supports the playbook generation skill in English.

Playbook Assist currently supports the playbook generation, playbook recommendations, and playbook generation with images skills in English. The playbook generation with images skill is not available for ServiceNow instances hosted in the APAC region.

## Supported user interfaces

Access the playbook generation skill when you’re creating a playbook in Workflow Studio.

![Build a new playbook with Now Assist.](../images/new-playbook-now-assist.png)

## Writing prompts and reviewing playbook outlines

Follow these guidelines when creating playbooks with playbook generation skills.

Write prompts:

-   **Provide a meaningful name for the playbook**

    The more descriptive the playbook name is, the better the playbook that Now Assist can create.

-   **Be precise and descriptive in the directions**
    -   Describe each stage and activity in as much detail as you can.

    -   Specify the order that stages and activities run in.

    -   Specify if any stages or activities run at the same time.

-   **Experiment with prompts**

    Save your prompts somewhere, including any modified versions. Saving your prompts enables easy comparison of results.

    **Note:** Prompts used only to generate a preview are not saved, but prompts used for a saved playbook outline are in the playbook's Properties setting.


Review playbook outlines:

-   **Check for accuracy**

    Review each stage and activity in a generated playbook to determine accuracy, efficiency, and how well it outlines your business process.

-   **Configure placeholder activities**

    Configure placeholder activities before you activate your playbook. Use playbook recommendations to help choose activity definitions.

    ![Choose an activity definition for the placeholder activity.](../images/configure-placeholder-activity.png "Configure the activity definition in the activity side panel")


## Retrieval Augmented Generation \(RAG\) support

Playbook generation uses Retrieval Augmented Generation \(RAG\) to include the names of active actions, subflows, flows, and activity definitions available on your instance. Workflow Studio updates the list of active actions, subflows, flows, and activity definitions every hour to make them available to playbook generation. You can refer to active actions, subflows, flows, and activity definitions by name in your playbook generation inputs.

## Example prompts

The following examples can help you to generate playbook outlines:

-   **Example playbook prompt 1: Employee onboarding**

    You can use this prompt to create a playbook for the onboarding process of new hires.

    ```
    Create an employee onboarding playbook that integrates new hires into the organization. 
    HR initiates it upon job offer acceptance, gathering documents, assigning mentors, providing orientation, 
    setting up IT access, ensuring compliance, and job-specific training. The playbook ends with feedback from the employee and HR, 
    resulting in an onboarding checklist.
    ```

-   **Example playbook prompt 2: Customer support**

    You can use this prompt to create a playbook with the steps that an agent takes for customer support cases.

    ```
    Create a customer support playbook which is the primary point of contact for handling customer inquiries, 
    problems, and requests. It starts by receiving and categorizing customer inquiries based on urgency and complexity. 
    Support tickets are then assigned to agents who troubleshoot and resolve them, with the option to escalate to higher 
    support tiers if needed. After resolution, follow-up with the customer is crucial. A satisfaction survey gathers feedback for 
    improvement, and all interactions are documented, updating the knowledge base for future reference.
    ```

-   **Example playbook prompt 3: Travel reimbursement**

    You can use this prompt to create a playbook to manage employee travel expenses.

    ```
    Create a travel expense reimbursement playbook for managing employee travel expenses efficiently. 
    Employees submit expense reports with valid receipts. Finance verifies expenses against policies, ensuring budget compliance. 
    Managers approve expenses, initiating payment processing.
    ```

-   **Example playbook prompt 4: Control document**

    You can use this prompt to create a playbook to manage a control document.

    ```
    Create a playbook for generating, reviewing, and approving a control document. Suppliers and Quality managers collaborate 
    to upload documents and conduct appropriate refinement before a final document is approved.
    ```

-   **Example playbook prompt 5: Supplier evaluation**

    You can use this prompt to create a playbook to evaluate whether potential suppliers meet qualification standards.

    ```
    Create a playbook for qualifying a new supplier. Suppliers request qualification. Quality managers review and approve 
    qualification requests, plan qualification deliverables, execute qualification activities, and summarize qualification findings in a report. 
    The playbook concludes by determining if the supplier has achieved the requested qualification.
    ```

-   **Example playbook prompt 6: Hardware inventory**

    You can use this prompt to create a playbook to manage hardware inventory.

    ```
    Create a playbook that manages hardware inventory. This playbook should efficiently track stock levels, update in real-time, 
    and generate alerts for low inventory. It must support categorization, bar codes, and seamless integration with sales and procurement systems.
    ```


**Note:** Generating or regenerating a playbook preview counts as 10 assists. To track your Now Assist usage, see Monitoring Now Assist usage in Subscription Management.

**Parent Topic:**[Playbook generation](playbook-assist-landing.md)

