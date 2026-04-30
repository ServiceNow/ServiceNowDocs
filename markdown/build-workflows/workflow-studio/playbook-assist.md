---
title: Exploring Playbook Assist
description: Use Playbook Assist to generate a playbook from text, an image or both. For example, you can upload an image of a business process you've outlined on a whiteboard or in diagramming software, describe more details of the process, and generate a playbook from those combined inputs. Playbook Assist is part of the Now Assist for Creator application.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Playbook Assist, Exploring playbooks, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Exploring Playbook Assist

Use Playbook Assist to generate a playbook from text, an image or both. For example, you can upload an image of a business process you've outlined on a whiteboard or in diagramming software, describe more details of the process, and generate a playbook from those combined inputs. Playbook Assist is part of the Now Assist for Creator application.

Activate the playbook skills in the Now Assist for Creator app. Playbook skills include:

-   Playbook generation
-   Playbook generation with images
-   Playbook recommendations

**Note:** Playbook authors must be assigned the **now.assist.creator** role to use playbook generation. See [Playbook Assist roles](../reference/playbook-assist-roles.md) for more information about this skill.

Playbook authors can provide an image of a business process from a whiteboard or diagramming software and add details with a text description to create multi-stage playbooks. As of version 26.2 for Now Assist for Creator, Now Assist inserts the activities that align most closely with your inputs. For activities that Now Assist isn't able to guess, placeholder activities are inserted.

**Note:** For placeholder activities, you can use the recommendations skill to find activities that might best replace placeholder activities, or manually find and configure activities before activating your playbook.

![Choose an activity definition for the placeholder activity.](../images/configure-placeholder-activity.png)

To learn more about recommendations, see [Playbook recommendations](playbook-recommendations.md#).

## Activation

**Playbook generation**, **playbook recommendations**, and **playbook generation with images** are skills that are installed with the Now Assist for Creator \(sn\_now\_creator\) application. You can install this application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Supported Now Assist skills

Playbook Assist currently supports the playbook generation, playbook recommendations, and playbook generation with images skills in English. The playbook generation with images skill is not available for ServiceNow instances hosted in the APAC region.

## Supported user interfaces

Access the playbook generation skill when you’re:

-   Creating a playbook in Workflow Studio from image, text, or both.

    ![Build a new playbook with Now Assist.](../images/example-img2playbook.png)

-   Replacing placeholder activities.

    ![Use the Playbook Recommendations skill to find common activities you can use instead of placeholders](../images/playbook-recommendations.png)


## Providing inputs and reviewing playbooks

Follow these guidelines when creating playbooks with playbook generation skills.

Provide inputs:

-   **Provide a meaningful name for the playbook**

    The more descriptive the playbook name is, the better the playbook that Now Assist can create.

-   **Make sure your image is the right format and size.**
    -   The image should be in JPG, JPEG, PNG, or WEBP format.
    -   The image should be 10MB or less.
-   **Make sure your image is clear and visible.**
    -   Upload an image that is clear and visible to the human eye. Make sure that any writing is legible. If you can't what's in an image, neither can Now Assist.
    -   When uploading an image, it is the primary input. You can use the text description to add more context about the business process in your uploaded image.
-   **Be precise and descriptive in text inputs**
    -   Describe each stage and activity in as much detail as you can.

    -   Specify the order that stages and activities run in.

    -   Specify if any stages or activities run at the same time.

    -   Add additional context for an image input.
-   **Experiment with inputs**

    Save your inputs somewhere, including any modified versions. Saving your inputs enables easy comparison of results.

    **Note:** Inputs used only to generate a preview are not saved, but inputs used for a saved playbook are in the playbook's **Properties** setting.


**Tip:** To learn more about playbook generation inputs, see [General Guidelines for Building Playbooks with Now Assist](../reference/general-guidelines-playbook-assist.md).

Review playbooks:

-   **Check for accuracy**

    Review each stage and activity in a generated playbook to determine accuracy, efficiency, and how well it outlines your business process.

-   **Configure placeholder activities**

    Configure placeholder activities before you activate your playbook. Use playbook recommendations to help choose activity definitions.

    ![Choose an activity definition for the placeholder activity.](../images/configure-placeholder-activity.png "Configure the activity definition in the activity side panel")


**Parent Topic:**[Playbook Assist](playbook-assist-landing.md)

