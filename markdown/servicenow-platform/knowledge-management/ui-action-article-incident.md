---
title: Create a UI action to enable creating knowledge articles from incidents
description: Create a UI action to add the Knowledge check box to the Incident form.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Knowledge article creation from an incident, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a UI action to enable creating knowledge articles from incidents

Create a UI action to add the Knowledge check box to the Incident form.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System UI** &gt; **UI Actions**.

2.  Click **New**.

3.  Fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |Name|Create Knowledge|
    |Table|Incident|
    |Action name|create\_knowledge|

4.  Select the **Client** check box.

5.  Select the **List v3 Compatible** check box.

6.  Select the **Form button** check box.

7.  In the **Onclick** field, enter `createKnowledgeClient()`.

8.  In the **Condition** field, enter `gs.getProperty("enable_kcs_incident") == 'true' && new global.CSMTableMapUtil (current).findMapByName("incident_kcs_article") && new global.KBKnowledge().canCreate()`.

9.  In the **Script** field, enter the following code.

    ```
    function createKnowledgeClient() {
        if (g_form.modified) {
            alert(new GwtMessage().getMessage('You have unsaved changes. Please save them to continue.'));    
        }else{
            //Call the UI Action again but skip the 'onclick' function
            gsftSubmit(null, g_form.getFormElement(), 'create_knowledge');
    //MUST call the 'Action name' set in this UI Action
        }
    }
    
    //Code that runs without 'onclick'
    //Ensure call to server-side function with no browser errors
    if (typeof window == 'undefined')
        CreateKnowledgeServer();
    
    function CreateKnowledgeServer(){
        current.update();
    
        var map = new global.CSMTableMapUtil (current);
        map.findMapByName("incident_kcs_article");
        var targetURL = map.getTargetURL();
            if(targetURL)
            action.setRedirectURL(targetURL[0]);
    }
    ```


**Parent Topic:**[Knowledge article creation from an incident](../concept/article-from-incident.md)

