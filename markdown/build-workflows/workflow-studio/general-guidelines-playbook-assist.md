---
title: General Guidelines for Building Playbooks with Now Assist
description: See guidelines and examples for using the Now Assist Playbooks capabilities.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-09-17"
reading_time_minutes: 4
breadcrumb: [Playbook Assist reference, Playbook Assist, Exploring playbooks, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# General Guidelines for Building Playbooks with Now Assist

See guidelines and examples for using the Now Assist Playbooks capabilities.

## Image inputs

The following examples can help you to generate playbooks using an image input:

-   **Make sure your image is the right format and size.**
    -   The image should be in JPG, JPEG, PNG, or WEBP format.
    -   By default, the image should be 5MB or less.

        **Note:** To change the max image size, change the **com.glide.attachment.max\_get\_size** system property. To earn more about changing the max image size, see [Change the maximum image size](../task/change-max-img-size.md).

-   **Make sure your image is clear and visible.**
    -   Upload an image that is clear and visible to the human eye. Make sure that any writing is legible. If you can't what's in an image, neither can Now Assist.

        If the image is unclear in any way, Now Assist returns an error and cannot generate a preview. This error is also displayed if an image is not a business process.

    -   When uploading an image, it is the primary input by default. You can use the text description to add more context about the business process in your uploaded image.

        **Note:** Since an image is the primary input, you will receive an error for a unusable or unclear image even if you include a valid text input.

-   **Don't use a nested process.**

    Nested processes are not currently supported for image to playbook generation.

-   **Make sure activities don't reference previous stages.**

    Processes with activities that reference previous stages are not currently supported for image to playbook generation.

-   **Don't use decision activities.**

    Decision activities are not currently supported for image to playbook generation.

-   **Don't use triggers.**

    Triggers cannot currently be created for playbook generation.

-   **Don't use variants.**

    Playbook variants are not currently supported for image to playbook generation.

-   **Don't use pictures that contain pictures.**

    Pictures that contains pictures are not supported.

-   **Make sure your image is unencrypted.**

    Encrypted images are not currently supported for image to playbook generation.

-   **Don't use loops in the process.**

    Processes that contain loops or have arrows that go back are not currently supported.

-   **Don't use multiple starting points.**

    Processes with multiple start nodes are not currently supported in Workflow Studio.

-   **Make sure your activities and stages are connected properly.**

    Lines should clearly connect activities and stages.


## Example text inputs

The following examples can help you to generate playbooks using only a text input:

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


**Note:** Generating or regenerating a playbook preview counts as 10 assists. To track your Now Assist usage, see .

**Parent Topic:**[Playbook Assist reference](playbook-assist-reference.md)

