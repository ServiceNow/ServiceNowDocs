---
title: Computer Telephony Integration
description: Computer Telephony Integration \(CTI\) is accomplished by the CTI client on the user machine sending a URL to the instance.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Supported integration interfaces, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer]
---

# Computer Telephony Integration

Computer Telephony Integration \(CTI\) is accomplished by the CTI client on the user machine sending a URL to the instance.

The URL must have the following components:

1.  The base URL. For example: `https://<instance name>.service-now.com/cti.do?` would get to the instance and ask for CTI processing. The URL is accessible to authenticated users only.
2.  Parameters identify what parts of the incident form to display.
    -   **sysparm\_caller\_name**=name where 'name' is the name for a user.
    -   **sysparm\_caller\_phone**=phone where 'phone' is the user's phone number. Either a name or phone should be provided if you want to identify the user on the call. Other parameters may be supplied to identify the user as discussed later.
    -   **sysparm\_task\_id**=taskID where 'taskID' identifies an existing issue that the caller is calling about.
    -   **sysparm\_view**=view where 'view' is the name of the view to be used to display the data.
    -   **sysparm\_xxxx**=value where 'xxxx' is the name of a field within the 'incident' record that should be populated with the specified 'value'. For example sysparm\_priority=1 would result in the priority field set to value of 1 when the new incident screen is shown.
    -   **sysparm\_cti\_rule**=name where 'name' is the name of a function to be invoked for CTI processing rather than using the default script. The function must be defined in a sys\_script entry marked client callable. If the function needs to insert, update, or delete any GlideRecord\(s\), it must call a separate non-client callable function to perform the update\(s\).

        **Note:** While the CTI Processing script has been changed to be client callable, the code implementing the task view has been commented out. You must implement a new non-client-callable function for the code that performs the task.update\(\).

        To make a script client-callable you must check the client-callable checkbox on the form that displays when the sys\_script entry is displayed. The client-callable checkbox might not show by default. To show the client-callable checkbox, you may need to modify the fields that show on the form using the gear icon and slushbucket mechanism.

        Parameters on the URL are available to the business rule as global values. For example:

        ```
        var name = sysparm_caller_name;
        ```

        The business rule you specify must return the URL for the pop-up screen, and set the 'answer' global variable.


An example URL to bring up a screen shot for user Don Goodliffe would look like the following. `https://<instance name>.service-now.com/cti.do?sysparm_caller_name=Don%20Goodliffe` Multiple sysparm parameters can be used, separated by ampersands \(&amp;\).

## CTI Processing script

When the **sysparm\_cti\_rule** parameter is not specified, the system uses the CTI Processing script to provide the following functionality.

The CTI Processing script does the following:

1.  Tries to identify the user by the **sysparm\_caller\_name** value if it was supplied.
2.  If no user has been found, the script tries to identify the user by the **sysparm\_caller\_phone** value if it was supplied.
3.  If a user has been identified then one of the following is done
    1.  If the user has open incidents, the popup screen shows information about the current caller and all the user's open incidents.
    2.  If the user does not have any open incidents, the popup screen shows a new incident with information provided in the URL shown.
4.  If a user was not identified and a taskID is given and the taskID exists, then nothing happens. The code to handle this case is commented out. If you want the popup screen to show the details for the task, you must modify the CTI Processing script to put the functionality in a separate non-client-callable function.

**Parent Topic:**[Supported integration interfaces](../../vendor-specific-integrations/reference/r_SupportedIntegrationInterfaces.md)

