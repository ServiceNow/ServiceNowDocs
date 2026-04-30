---
title: Create a UI action to enable creating knowledge articles from HR cases
description: Create a UI action to add the Knowledge check box to the HR case form.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enable actionable knowledge feedback, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a UI action to enable creating knowledge articles from HR cases

Create a UI action to add the Knowledge check box to the HR case form.

## Before you begin

Role required: admin

Ensure that the Developer Application is set to **Human Resources: Core**.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **UI Actions**.

2.  Click **New**.

3.  Fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |Name|Create Knowledge|
    |Table|HR Case|
    |Action name|create\_knowledge|

4.  Select the **Client** check box.

5.  Select the **List v3 Compatible** check box.

6.  Select the **Form button** check box.

7.  In the **Onclick** field, enter `createKnowledgeClient()`.

8.  In the **Condition** field, enter `gs.getProperty("sn_hr_core.enable_kcs_hr") == 'true' && new global.CSMTableMapUtil (current).findMapByName("sn_hr_core.hr_case_kcs_article") && new global.KBKnowledge().canCreate()`.

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
        map.findMapByName("sn_hr_core.hr_case_kcs_article");
        var targetURL = map.getTargetURL();
        var referenceLink = 
    "&sysparm_collection=sn_hr_core_case&sysparm_collectionID="+current.sys_id+"&sysparm_collection_key=task&sysparm_link_collection=m2m_kb_task&sysparm_collection_related_field=kb_knowledge&sysparm_referring_url=sn_hr_core_case.do%3fsys_id%3d"+current.sys_id;
        if(targetURL)
            action.setRedirectURL(targetURL[0]+referenceLink);
    }
    ```

10. Click **Submit**.


