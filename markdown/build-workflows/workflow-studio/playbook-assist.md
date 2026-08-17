---
title: Playbook generation from text prompt or image
description: Generate a playbook using AI from text prompt or image inputs. For example, you can enter a text description to generate a playbook for managing customer support cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/playbook-assist.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Creating and managing Playbooks, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Playbook generation from text prompt or image

Generate a playbook using AI from text prompt or image inputs. For example, you can enter a text description to generate a playbook for managing customer support cases.

ServiceNow Otto for Creator activates the playbook generation skill. Playbook generation gives generative AI capabilities to playbook authors.

## Activation

Playbook generation is a skill that is installed with the ServiceNow Otto for Creator \(sn\_now\_creator\) application. You can install this application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website. You must enable the Playbook generation skill to generate playbooks using AI.

## Supported user interfaces

Access the Playbook generation skill when you’re creating a playbook in Workflow Studio.

\[Omitted image "new-playbook-otto.png"\] Alt text: Build a new playbook using AI.

## Writing prompts

Follow these guidelines when writing prompts to generate playbooks.

-   **Provide a meaningful name for the playbook**

    The more descriptive the playbook name is, the better the playbook that AI can create.

-   **Be precise and descriptive in the directions**
    -   Describe each stage and activity in as much detail as you can.

    -   Specify the order that stages and activities run in.

    -   Specify if any stages or activities run at the same time.

-   **Use clear images**

    Use high resolution images with clear shapes, text, and arrows. Avoid using blurred screenshots and images of unclear whiteboard diagrams.

    You can use one image of up to 10 MB, in JPG, JPEG, PNG, or WEBP format.

-   **Experiment with prompts**

    Save your prompts somewhere, including any modified versions. Saving your prompts enables easy comparison of results.

    **Note:** Prompts used only to generate a preview aren't saved, but prompts used for a saved playbook outline are in the playbook's Properties setting.


## Reviewing playbooks

Follow these guidelines to review the generated playbooks.

-   **Check for accuracy**

    Review each stage and activity in a generated playbook to determine accuracy, efficiency, and how well it outlines your business process.

-   **Configure placeholder activities**

    Configure placeholder activities before you activate your playbook. Use playbook recommendations to help choose activity definitions.

    \[Omitted image "configure-placeholder-activity.png"\] Alt text: Choose an activity definition for the placeholder activity.


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


-   **[Generate a playbook from text or image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/generate-a-playbook-outline.md)**  
Generate a playbook using AI by providing text directions or an image.

**Parent Topic:**[Creating and managing Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/creating-managing-playbooks.md)

**Related topics**  


[Generate a playbook from text or image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/generate-a-playbook-outline.md)

