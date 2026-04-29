---
title: Set up Now Assist in the portal case form
description: Configure the Now Assist in portal case form to minimize case creation when a resolution already exists in the current knowledge base or external sources.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Generative AI, Generative AI for Customer Service Management, record producer, portal case form, AI Search Assist]
breadcrumb: [Configure, Now Assist for CSM, Customer Service Management]
---

# Set up Now Assist in the portal case form

Configure the Now Assist in portal case form to minimize case creation when a resolution already exists in the current knowledge base or external sources.

Configure Now Assist in portal case form 

## Before you begin

Role required: admin

## About this task

This configuration involves setting up the record producer, configuring related lists and variables, testing the configuration, and relating the catalog to the portal.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Record Producers**.

2.  Search and open the record producer **Create case for a product \(Now Assist\)**.

    The base system configuration details display.

3.  Select **Copy** to duplicate the record producer.

    This creates a new version you can customize for your use case.

4.  Enter a **Name**.

    This is the title the customers see in the portal.

5.  Set the **Table name** to a specific case type.

6.  Modify the **Short description** and **Description** to match your use case.

7.  Scroll to review the variables list and update as required.

    For example, update the client scripts, change variables, add user criteria UI policies, and virtual agent topics and catalogs. You will find variables called **AI Search Assist** and **AI Genius Results** options in your configuration. Do not delete **Start**, **AI Search Assist**, **AI Genius Results Options**, and **Continue with Record Creation** to maintain the experience. These variables leverage the AI Search genius result widget found under AI Search Assist record producer configurations.

8.  Select **Save** after completing all changes in the record producer configuration.

9.  Select **Try It** to preview the record producer.

10. Navigate to **All** &gt; **AI Search** &gt; **AI Search Assist** &gt; **Record Producer Configuration** to edit the record producer configuration that we previously duplicated.

11. Select **New**.

12. On the **Record Producer Configuration** form, fill in the following fields.

    |Field|Value|
    |-----|-----|
    |**__Search application information__**| |
    |**Search Application**|Select the configuration for a portal that includes Now Assist Q&amp;A Genius Results. As an example, you might select the Service Portal Default Search Application configuration.|
    |**__Record producer information__**| |
    |**Record producer**|Select a record producer. As an example, you might select the Create case for a product record producer.|
    |**Search variable**|Select the name of the field that you want to search and generate Genius Results from. As an example, you might select the Description field as your search variable.|

13. Select **Submit**.

14. Navigate to **Service Portal** &gt; **Portal** to connect the record producer to a catalog and Portal.

15. Search for the portal configuration and select it.

16. Scroll down to note the **Catalog** and **Taxonomy** topics.

17. Select the **Taxonomy** value.

18. Select a topic under **Child Topics**.

19. Select the **Enable AI Search** check box.

20. Select a pre-configured **Search Application** – CSM Portal Default Search Application.

21. Select **Update**.

22. Return to the record producer.

23. Edit the **Catalog** field to include the catalog we noted from the Portal settings.

24. Select **Assigned Topics** and add the relevant topic to ensure the record producer appears in the correct location of the portal.

25. Select **Save**.

26. Navigate to the Portal and under **Catalogs** verify that the record producer appears under the specified topic.

    **Note:** Ensure the catalog you related to the record producer is also related to the portal and fully published.

27. Navigate to the **Service Portals**.

28. Open the catalog and go to the record producer you created.


## Result

The Now Assist Case in form portal is now configured and available for use.

**Related topics**  


[Using Now Assist in portal case form](../concept/using-ai-search-with-q-a-within-the-portal-form.md)

