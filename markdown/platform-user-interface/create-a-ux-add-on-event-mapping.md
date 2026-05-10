---
title: Create a UX add-on event mapping
description: Connect a button to a modal using UX add-on event mapping in order for an action button to open a custom modal.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure a custom form modal, Configure action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Create a UX add-on event mapping

Connect a button to a modal using UX add-on event mapping in order for an action button to open a custom modal.

## Before you begin

Complete the following actions:

-   [Create a form action](create-a-new-form-action.md)
-   Open your record page in UIB or [create a page variant in UIB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-variant.md)
-   [Design your page variant in UIB](design-a-page-variant-in-uib.md#)
-   [Configure your page variant as a modal in UIB](configure-a-page-variant-as-a-modal-in-uib.md#)

Role required: admin

## Procedure

1.  Open the add-on event mapping **&lt;instance-name&gt;.service-now.com/sys\_ux\_addon\_event\_mapping\_list.do** into your browser.

2.  Create a new record by selecting **New**.

3.  Enter a name for your map.

4.  Select **ui\_action\_bar** for the Source element ID field.

5.  Select the action name for your declarative action for the Source Declarative Action field.

6.  Set the macroponent to the workspace record macroponent using the sysID copied from the record's page definition.

    For more information, see [Configure a page variant as a modal in UIB](configure-a-page-variant-as-a-modal-in-uib.md#).

7.  Trigger the event to open a modal by selecting **\[Record Page\] Open modal** in the Target Event field.

8.  Define the fields to send to the modal by pasting the JSON object into the Target Payload Mapping field.

    ```
    {
    	"type": "MAP_CONTAINER",
    	"container": {
    		"route": {
    			"type": "EVENT_PAYLOAD_BINDING",
    			"binding": {
    				"address": ["route"]
    			}
    		},
    		"size": {
    			"type": "EVENT_PAYLOAD_BINDING",
    			"binding": {
    				"address": ["size"]
    			}
    		},
    		"fields": {
    			"type": "EVENT_PAYLOAD_BINDING",
    			"binding": {
    				"address": ["fields"]
    			}
    		},
    		"params": {
    			"type": "EVENT_PAYLOAD_BINDING",
    			"binding": {
    				"address": ["params"]
    			}
    		}
    	}
    }
    ```

9.  Select **Submit**.


