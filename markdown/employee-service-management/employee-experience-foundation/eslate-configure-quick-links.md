---
title: Configure Quick Links widgets
description: Select and display Quick Links on the Employee Slate home page and Canvas by capturing sys\_ids and updating each widget.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/eslate-configure-quick-links.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 2
keywords: [quick links, homepage widget, canvas widget, sys\_id, background script, Employee Slate]
breadcrumb: [Quick Links widgets, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Configure Quick Links widgets

Select and display Quick Links on the Employee Slate home page and Canvas by capturing sys\_ids and updating each widget.

## Before you begin

Role required: admin.

Create and configure the Quick Links to display in Employee Center before starting.

## About this task

Both widgets use sys\_ids from the Employee Center Quick Links table \(`sn_ex_sp_quick_link`\). Complete Section 1 first, then configure the home page widget, the Canvas widget, or both.

## Procedure

1.  Section 1: Capture Quick Link sys\_ids
2.  Go to **Employee Center** &gt; **Quick Links**, or open the `sn_ex_sp_quick_link` table directly.

3.  Open the Quick Link record to include in the widget.

4.  Right-click the record header or any field label, then select **Copy sys\_id**.

5.  Repeat for each Quick Link to display.

    Save the sys\_ids in a text file as a comma-separated list. You use this list in the sections below. For example: `sys_id1,sys_id2,sys_id3`.

6.  Section 2: Configure the home page Quick Links widget
7.  Go to **System Definition** &gt; **Scripts – Background**.

    The home page Quick Links widget configuration field is read-only in the standard UI. Use a background script to update it programmatically.

8.  Copy the following script and paste it into the script editor.

    ```javascript
    /* -------------------------------------------------------
     * Updates the Quick Links widget on the Employee Home Page.
     * Add your Quick Link sys_ids as comma-separated values
     * in the "value" field below.
     * ------------------------------------------------------- */
    
    var WIDGET_ID = 'quick-links';
    
    var NEW_OPTIONS = {
        "quick_links": {
            "value": "sys_id1,sys_id2,sys_id3"  // Replace with your sys_ids
        }
    };
    
    // ---- Do not edit below this line ----
    
    var gr = new GlideRecord('sys_aix_widget_instance');
    if (!gr.get('5ebb39e1ffda72106d14ffffffffffff2a')) {
        gs.info('Record not found');
    }
    
    var props = JSON.parse(gr.getValue('properties'));
    var widget = null;
    
    for (var i = 0; i < props.widgets.length; i++) {
        if (props.widgets[i].id === WIDGET_ID) {
            widget = props.widgets[i];
            break;
        }
    }
    
    if (!widget) {
        gs.info('Widget "' + WIDGET_ID + '" not found in properties');
    }
    
    widget.options = NEW_OPTIONS;
    gr.setValue('properties', JSON.stringify(props, null, 4));
    gr.update();
    gs.info('Updated options for widget "' + WIDGET_ID + '"');
    ```

9.  In the **value** field of the script, replace `sys_id1,sys_id2,sys_id3` with your comma-separated list of Quick Link sys\_ids.

10. Select **Run Script**.

    The home page Quick Links widget shows the Quick Links with the sys\_ids you provided, based on the access permissions of each user.

11. Section 3: Configure the Canvas Quick Links widget
12. Go to **AIUX** &gt; **Dashboards** and open the Canvas record.

13. In the AIX Dashboard Items related list at the bottom of the record, locate and open the Quick Links widget instance.

14. In the Widget Properties field, locate the **value** property.

15. Enter your comma-separated list of Quick Link sys\_ids in the **value** field.

    For example: `sys_id1,sys_id2,sys_id3`

16. Select **Save**.

    The Canvas Quick Links widget displays the Quick Links with the sys\_ids you provided.


**Related topics**  


[Quick links](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/eslate-quick-links.md)

