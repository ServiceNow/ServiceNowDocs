---
title: GlideAgentWorkspace \(g\_aw\) - Client
description: The g\_aw API provides methods that enable a UI action or client script to open a specified record in an Agent Workspace tab.Closes the currently open record, such as a form, in a subtab within Agent Workspace.Opens a specified record, such as a form, in a subtab within Agent Workspace.Sets a form section to expanded or collapsed state.Gets the domain scope details.
locale: en-US
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideAgentWorkspace \(g\_aw\)- Client

The g\_aw API provides methods that enable a UI action or client script to open a specified record in an Agent Workspace tab.

There is no constructor for this class. Access GlideAgentWorkspace methods using the `g_aw` global object.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideAgentWorkspace - closeRecord\(\)

Closes the currently open record, such as a form, in a subtab within Agent Workspace.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example saves the content of the tab and then closes it.

```
function onClick(g_form) {
```

```
function onClick(g_form) {
  g_form.save().then(function(){
    g_aw.closeRecord();
  });
}
```

The following example script uses the `g_aw.closeRecord()` method to close a record when a button is clicked in Agent Workspace. You can use this script as follows:

1.  Add this script to a UI Action \(button\) configured for Agent Workspace.
2.  When the button is clicked, it will attempt to close the current record.
3.  Basic logging indicates success or failure.

```
functioncloseCurrentRecord() {
    if (typeof g_aw !== 'undefined' && g_aw.closeRecord) {
        g_aw.closeRecord().then(function(response) {
            console.log(response.success ? 'Record closed successfully.' : 'Failed to close the record.');
        }).catch(function(error) {
            console.error('Error closing the record:', error);
        });
    }
}
```

In a more complex example, the closeRecord\(\) method is applied in a client script where a support agent wants to automatically close an incident record in Agent Workspace after performing a specific action, such as resolving the incident. The key actions of this script are as follows:

-   Trigger Condition: The script checks if the incident's state is set to "Resolved" \(`state = 6`\).
-   Workspace Validation: Ensures the code runs only within Agent Workspace using `typeof g_aw !== 'undefined'`.
-   Promise Handling: Uses .then\(\) and .catch\(\) for handling the asynchronous nature of closeRecord\(\).
-   Error Handling: Provides detailed logging for both successful and failed attempts.

```
(function executeRule(current, gForm, gUser, gSNC) {
    // Check if the incident state is 'Resolved' (state = 6 in default ServiceNow setup)
    if (current.state == 6) {
        // Ensure we're in Agent Workspace
        if (typeof g_aw !== 'undefined' && g_aw.closeRecord) {
            g_aw.closeRecord().then(function(response) {
                if (response.success) {
                    console.log('Incident record closed successfully in Agent Workspace.');
                } else {
                    console.error('Failed to close the record:', response.errorMessage);
                }
            }).catch(function(error) {
                console.error('An error occurred while closing the record:', error);
            });
        }
    }
})(current, gForm, gUser, gSNC);
```

## GlideAgentWorkspace - openRecord\(String table, String sysId, Object params\)

Opens a specified record, such as a form, in a subtab within Agent Workspace.

**Note:** This method is only available in the Agent Workspace client scripting environment or in a UI action on the workspace client script field.

<table id="table_lhq_mph_bhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

table

</td><td>

String

</td><td>

Name of the table that contains the record to open.

</td></tr><tr><td>

sysId

</td><td>

String

</td><td>

Sys ID of the record to open.

</td></tr><tr><td>

params

</td><td>

Object

</td><td>

Optional. Name/value pairs of the parameters to pass to the record.```
"params": {
  "readOnlyForm": Boolean;
  "defaultTab": "String";
  "hideDetails": Boolean
}
```

</td></tr><tr><td>

params.readOnlyForm

</td><td>

Boolean

</td><td>

Flag that indicates whether all fields on the opened record are read-only; regardless of the UI policy and ACLs.-   true: All fields are read only.
-   false: Fields adhere to the associated UI policy and ACLs.

 Default: false

</td></tr><tr><td>

params.defaultTab

</td><td>

String

</td><td>

Name of the initial tab to display in the workspace. You can only specify related items or related lists.If not specified, the details tab appears unless **hideDetails** is set to true.

 For more information on the method to use to obtain a related list name, see [getRelatedListNames\(\)](../../GlideForm/concept/c_GlideFormAPI.md#).

</td></tr><tr><td>

params.hideDetails

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the details tab and the UI actions.-   true: Only the form header, all other tabs, and the first available tab appear on the form.
-   false: Details tab and UI actions appear on the form.

 Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

Open a sys\_user record in a subtab.

```
g_aw.openRecord('sys_user', '62826bf03710200044e0bfc8bcbe5df1'); 
```

Open a record in a subtab where all fields are read-only.

```
g_aw.openRecord('sys_user', '62826bf03710200044e0bfc8bcbe5df1', {readOnlyForm: true}); 
```

Open a record in a subtab and go directly to the "Groups" related list.

```
g_aw.openRecord('sys_user', '62826bf03710200044e0bfc8bcbe5df1', {defaultTab: "sys_user_grmember.user"});  
```

Open a record in a subtab but only show the form header and other tabs.

```
g_aw.openRecord('sys_user', '62826bf03710200044e0bfc8bcbe5df1', {hideDetails: true}); 
```

The following example script demonstrates how an agent can add a button to an incident which opens a related change request in a new tab within Agent Workspace. The key actions of this script are as follows:

-   Dynamic Record Opening: The script retrieves the sys\_id of the related change request from the current incident.
-   Agent Workspace Context: It checks if `g_aw` is available to confirm the script is running in Agent Workspace.
-   Custom Parameters:
    -   `view: 'agent'` opens the record in a specific view \(optional\).
    -   `readOnly: true` opens the record in read-only mode \(optional\).
-   Error Handling: Uses .then\(\) and .catch\(\) for handling responses and errors.

```
function openRelatedChangeRequest() {
    // Get the sys_id of the related Change Request from the current incident
    var changeRequestSysId = g_form.getValue('change_request'); // Assuming 'change_request' is the field name

    if (changeRequestSysId && typeof g_aw !== 'undefined' && g_aw.openRecord) {
        g_aw.openRecord('change_request', changeRequestSysId, {
            view: 'agent', // Optional: Specify a custom view
            readOnly: true // Optional: Open the record in read-only mode
        }).then(function(response) {
            if (response.success) {
                console.log('Change Request opened successfully.');
            } else {
                console.error('Failed to open Change Request:', response.errorMessage);
            }
        }).catch(function(error) {
            console.error('Error opening Change Request:', error);
        });
    } else {
        console.warn('No related Change Request found or Agent Workspace is not available.');
    }
}
```

**Note:** You can use this script in your own instance by attaching this script to a UI Action \(button\) on the Incident form in Agent Workspace. Clicking the button opens the related change request in a new tab, improving the agent's workflow.

## GlideAgentWorkspace - setSectionExpanded\(String section\_name, Boolean expanded\)

Sets a form section to expanded or collapsed state.

<table id="table_lhq_mph_bhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

section\_name

</td><td>

String

</td><td>

Name of a form section in Agent Workspace.

</td></tr><tr><td>

expanded

</td><td>

Boolean

</td><td>

Flag that indicates whether a section is to be expanded or collapsed by default.-   true: The section is expanded by default.
-   false: The section is collapsed by default.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a form section named `related_records` to collapse by default.

```
function onLoad() {
   g_aw.setSectionExpanded('related_records', false);
}
```

The following example script demonstrates how an agent can use the setSectionExpanded method to open an incident where the "Work Notes" section should automatically expand if the incident has a high priority \(e.g., Priority 1 or 2\). For lower priorities, the section remains collapsed to reduce visual clutter.

The key actions of this script are as follows:

-   Priority-Based Logic: The script checks the incident's priority using `g_form.getValue('priority')`.
-   Dynamic Section Control: Expands the "Work Notes" section if the priority is 1 \(Critical\) or 2 \(High\). Collapses it for lower priorities to maintain a cleaner UI.
-   Agent Workspace Check: Ensures the script only runs in Agent Workspace.

```
javascriptCopyEdit(functiontoggleWorkNotesSection() {
    // Check if we're in Agent Workspace and the method is availableif (typeof g_aw !== 'undefined' && g_aw.setSectionExpanded) {
        // Get the incident priority from the formvar priority = g_form.getValue('priority');

        // Automatically expand the "Work Notes" section for high-priority incidents (1 or 2)var shouldExpand = (priority == '1' || priority == '2');

        // Expand or collapse the section based on priority
        g_aw.setSectionExpanded('Work Notes', shouldExpand);
    }
})();
```

You can add this example as a client script with the type set to "onLoad" for incidents in Agent Workspace. Make sure the section name matches exactly as it appears in the form layout \(for example, "Work Notes"\).

## GlideAgentWorkspace - domainScopeProvider\(\)

Gets the domain scope details.

The domainScopeProvider\(\) method accesses four functions to return information about the domain scope. For information, see Domain scope.

Required role – domain\_expand\_scope.

<table id="table_lhq_mph_bhb" class="parameters"><thead><tr><th>

Function Name

</th><th>

Return Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

getDomainScope\(\)

</td><td>

String

</td><td>

Gets the domain scope.Possible values:

-   false: Returns basic domain info and doesn't include information about parent domains, inherited properties, or domain hierarchy.
-   true: Return detailed domain scope information about the current record or workspace context.

Default: false

</td></tr><tr><td>

hasDomainChanged\(\)

</td><td>

Boolean

</td><td>

Flag that indicates if the domain has changed for the current record compared to its original domain.Valid values:

-   true: Domain has changed.
-   false: Domain hasn't changed. Returns basic domain information without evaluating whether the domain has changed.

Default: false

</td></tr><tr><td>

isDomainEnabledRecord\(\)

</td><td>

Boolean

</td><td>

Flag that indicates whether the method should check if the current record is domain-separated \(domain-enabled\).Valid values:

-   true: Record is domain-enabled \(for example, domain separation applies to it\).
-   false: Record isn't domain-enabled \(for example, it exists globally without domain-specific restrictions\).

Default: false

</td></tr><tr><td>

toggleDomainScope\(\)

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable or disable the domain scope context for a record.Valid values:

-   true: Display all data available based to the user's domain and child domains.
-   false: Display only data that matches the current record's domain.

Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

### Example

The following example shows how to toggle the domain scope between the user session and the record as expanded \(session scope\) or collapsed \(record scope\) in a UI action workplace client script.

```
function onClick(g_form) {
    var provider = g_aw.domainScopeProvider();
    
    provider.toggleDomainScope();

    var domainScopeNow = provider.getDomainScope();

    if (domainScopeNow === 'SESSION')
        g_form.addInfoMessage(getMessage("Domain Scope Expanded"));
    else if (domainScopeNow === 'RECORD')
        g_form.addInfoMessage(getMessage("Domain Scope Collapsed"));
}
```

```
function onSubmit() {
      if (typeof g_aw === 'undefined' || !g_aw.domainScopeProvider || typeof g_scratchpad === 'undefined') return true;
      if (g_scratchpad._domainConfirmationPassed ||
          g_scratchpad._domainCheckErrorBypass || g_scratchpad._domainCheckPassed) return true;
      var provider = g_aw.domainScopeProvider();
      if (!provider || !provider.isDomainEnabledRecord || !provider.isDomainEnabledRecord()) return true;
  // if you change these messages, please change them in the above messages field var title = getMessage("Change Domain"); var message = getMessage("You are about to change the domain of this record which may result in data
      loss.We will copy the information we can but you may need to replace the lost data.Do you want to proceed ? ");
      var gFormRef = g_form;
      var popModalConfirm = function() {  g_modal.confirm(title, message , function(response) {
      if (response) {
          g_scratchpad._domainConfirmationPassed = true;
          gFormRef.submit(gFormRef.getActionName());
      }
  });
  return false;
  };

  var proceedWithSubmit = function() {
      gFormRef.submit(gFormRef.getActionName());
  };

  var hasDomainChanged = provider.hasDomainChanged();
  if (hasDomainChanged === false) return true;
  if (hasDomainChanged === true) return popModalConfirm();
  else {
      hasDomainChanged.then(function(isChanged) {
          if (isChanged)
              return popModalConfirm();
          else {
              g_scratchpad._domainCheckPassed = true;
              proceedWithSubmit();
          }
      }, function(error) {
          g_scratchpad._domainCheckErrorBypass = true;
          proceedWithSubmit();
      });
      return false;
  }
}
```

The following example script demonstrates how an agent can verify which domain they are working in when handling records in Agent Workspace. The key actions of this script are as follows:

-   Basic Checks: `typeof g_aw !=='undefined'` ensures the script only runs in Agent Workspace. `g_aw.domainScopeProvider` checks if the method exists.
-   Simple Asynchronous Handling: Uses `.then()` to process the result when the domain info is available. Uses `.catch()` to handle any errors \(for example, if something goes wrong when fetching the domain\).
-   User-Friendly Alert: Displays an alert with the domain name \(`alert('You are working in the domain: ...')`\), which is simple and easy to understand. If no domain info is found, it alerts the user with "`Domain information is not available.`"
-   Error Handling: Errors are logged to the console using `console.error()` for basic troubleshooting.

```
(function showDomainAlert() {
    // Check if we're in Agent Workspace and the domainScopeProvider is available
    if (typeof g_aw !== 'undefined' && g_aw.domainScopeProvider) {
        // Get the current domain information
        g_aw.domainScopeProvider().then(function(domainInfo) {
            if (domainInfo && domainInfo.name) {
                // Show an alert with the current domain name
                alert('You are working in the domain: ' + domainInfo.name);
            } else {
                alert('Domain information is not available.');
            }
        }).catch(function(error) {
            console.error('Error getting domain scope:', error);
        });
    }
})();
```

You can add this script as an "onLoad" Client Script in Agent Workspace. When an agent opens a record, an alert will pop up showing the current domain name.

