---
title: Create a UI action to close multiple incidents
description: Create a UI action to close multiple incidents at once from the Actions list in the list view.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Incident resolution and closure, Manage, Incident Management, IT Service Management]
---

# Create a UI action to close multiple incidents

Create a UI action to close multiple incidents at once from the **Actions** list in the list view.

## Before you begin

Role required: business\_rule\_admin \(for business rule\), ui\_action\_admin \(for UI action\), or admin

## About this task

Closing an incident from **Actions** list adds the same close note to all the incidents that are closed and does not require the list\_updater role. Implementing this process requires a script include that is referred from a UI action and a custom UI page.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes** and click **New**.

2.  Create the script includes with the following information.

    -   **Name**: IncidentClosure
    -   **Client callable**: Select the check box
    -   **Active**: Select the check box
    -   **Script**: Paste the following information:

        ```
        var IncidentClosure = Class.create();
        IncidentClosure.prototype = Object.extendsObject(AbstractAjaxProcessor, {
            closeIncidents: function() {
                var selectedIncidents = this.getParameter("sysparm_incidents");
                var notes = this.getParameter("sysparm_closeNote");
                var code = this.getParameter("sysparm_closeCode");
                var incidentGr = new GlideRecord('incident');
                incidentGr.addQuery('sys_id', 'IN', selectedIncidents);
                incidentGr.query();
                while (incidentGr.next()) {
                    incidentGr.setValue('state', 7);
                    incidentGr.setValue('close_notes', notes);
                    incidentGr.setValue('close_code', code);    
                    incidentGr.update();
                }
                return true;
            },
            
           type: 'IncidentClosure'
        });
        ```

3.  Save the record.

4.  Create the following steps to create a UI page.

    -   **Name**: mandatory\_fields\_to\_close\_incident\_ui
    -   **HTML**: Paste the following information:

        ```
        <?xml version="1.0" encoding="utf-8" ?>
        <j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
            <style>
                #content_row .reference-label {
                    padding-right: 15px;
                }
        
                #page_timing_div {
                    display: none;
                }
            </style>
            <form class="form-horizontal">
                <div class="form-group">
                    <label class="col-xs-4 control-label">
                        <span style="padding-right: 5px;"></span>
                        <span class="label-text">${gs.getMessage('Resolution code')}</span>
                    </label>
                    <div class="col-xs-5 form-field input_controls" style="line-height: 32px;">
                        <select name="closeCode" id="closeCode">
                            <option value="" selected="SELECTED" role="option">-- None --</option>
                            <option value="Solved (Work Around)" role="option">Solved (Work Around)</option>
                            <option value="Solved (Permanently)" role="option">Solved (Permanently)</option>
                            <option value="Solved Remotely (Work Around)" role="option">Solved Remotely (Work Around)</option>
                            <option value="Solved Remotely (Permanently)" role="option">Solved Remotely (Permanently)</option>
                            <option value="Not Solved (Not Reproducible)" role="option">Not Solved (Not Reproducible)</option>
                            <option value="Not Solved (Too Costly)" role="option">Not Solved (Too Costly)</option>
                            <option value="Closed/Resolved by Caller" role="option">Closed/Resolved by Caller</option>
                        </select>
                    </div>
                </div>
                <div class="form-group">
                    <label class="col-xs-4 control-label">
                        <span class="label-text" style="">${gs.getMessage('Resolution Notes')}</span>
                    </label>
                    <div class="col-xs-7 form-field input_controls">
                        <textarea required="true" class="form-control" value="closeNotes" id="closeNotes" type="text"></textarea>
                    </div>
                </div>
                <div class="form-group" style="padding-right:20px;margin-bottom:0;padding-left: 75%; line-height: 45px;">
                    <g:dialog_button id="cancel_button" type="button" style_class="$btn btn-default" onclick="actionCancel()" style="min-width: 5em;">${gs.getMessage('Cancel')}</g:dialog_button>
        
                    <g:dialog_button id="ok_button" type="button" onclick="actionOK()" style_class="btn btn-primary" style="min-width: 5em;">${gs.getMessage('OK')}</g:dialog_button>
                    <div class="clearfix"></div>
                </div>
            </form>
        </j:jelly>
        ```

    -   **Client script**: Paste the following information:

        ```
        function actionOK() {
            var modal = GlideModal.prototype.get("mandatory_fields_to_close_incident_ui");
            var incidents = modal.getPreference("selected_incidents");
            if (incidents) {
                //close the incidents
                var glideAjax = new GlideAjax("IncidentClosure");
                glideAjax.addParam("sysparm_name", "closeIncidents");
                glideAjax.addParam("sysparm_incidents", incidents);
                glideAjax.addParam("sysparm_closeCode", $("closeCode").value);
                glideAjax.addParam("sysparm_closeNote", $("closeNotes").value);
                glideAjax.getXMLAnswer(function(answer) {
                    GlideModal.prototype.get("mandatory_fields_to_close_incident_ui").destroy();
                    GlideList2.get('incident').refresh();
                });
            }
        }
        
        function actionCancel() {
            GlideModal.prototype.get("mandatory_fields_to_close_incident_ui").destroy();
        }
        
        (function() {
            var okButton = gel('ok_button');
            var closeCodeEl = gel('closeCode');
            var closeNotesEl = gel('closeNotes');
            okButton.disabled = true;
            closeNotesEl.value = "";
            closeCodeEl.on('change', function() {
                if (closeCodeEl.value !=="" && closeNotesEl.value !=="")
                    okButton.disabled = false;
                else
                    okButton.disabled = true;
            });
            closeNotesEl.on('input', function() {
                if (closeCodeEl.value !=="" && closeNotesEl.value !=="")
                    okButton.disabled = false;
                else
                    okButton.disabled = true;
            });
        })();
        ```

5.  Save the record.

6.  Complete the following steps to create the UI action for closing multiple incidents.

    1.  Navigate to **System Definition** &gt; **UI Actions** and click **New**.

    2.  Create the UI actions with the following information:

        -   **Name**: Close incidents
        -   **Table**: Incident \[incident\]
        -   **Show update**: Select the check box
        -   **List choice**: Select the check box
        -   **List v2 Compatible**: Select the check box
        -   **Client**: Select the check box
        -   **Onclick**: closeIncidents\(\)
        -   **Condition**: current.getValue\('state'\) !== '7'
        -   **Script**: paste the following information
        ```
        function closeIncidents() {
            var list = GlideList2.get('incident');
            var title = list.getTitle();
            var incidents = list.getChecked();
            if (incidents) {
                var o = new GlideModal('mandatory_fields_to_close_incident_ui');
                    getMessage("Close Incidents", function(msg) {
                        o.setTitle(msg);
                        o.setPreference('selected_incidents', incidents);
                        o.render();
                    });
                }
            }
                   
        ```

7.  Save the record.


## Result

Service desk agents can close multiple incidents using **Close incidents** in the **Actions** list below the Incident list.

**Parent Topic:**[Incident resolution and closure](../concept/c_IncidentResolutionAndRecovery.md)

