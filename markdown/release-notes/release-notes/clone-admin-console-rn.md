---
title: Clone Admin Console release notes
description: The ServiceNow Clone Admin Console application relies on the existing clone engine. It provides a unified admin experience and enhanced visibility for cloning data between instances. Clone Admin Console was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
---

# Clone Admin Console release notes

The ServiceNow® Clone Admin Console application relies on the existing clone engine. It provides a unified admin experience and enhanced visibility for cloning data between instances. Clone Admin Console was enhanced and updated in the Xanadu release.

## Clone Admin Console highlights for the Xanadu release

-   Use a new backup when you’re backing up the Clone Admin Console to make the backup go more quickly.
-   View the Clone preserver guidance added to the Create a clone form to understand how to use Clone preservers.
-   Clone related queries now go through ACLs. Custom clone flows should be tested.

See [Clone Admin Console](https://www.servicenow.com/docs/access?context=Clone-UI&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more information.

**Important:** Clone Admin Console is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Target instance modal](https://www.servicenow.com/docs/access?context=clone-ui-request-clone&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Request a clone to copy the data from a production instance to a non-production instance or to copy the data between non-production instances. You can request a clone without leaving the form by using the **add an instance** option in the **clone request target instance** field.

-   **[Using the same backup from another clone](https://www.servicenow.com/docs/access?context=Clone-UI&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Use the backup from another clone when you're selecting a backup option for a faster backup process. If the backup no longer exists, it triggers an on-demand backup instead.

-   **[Clone storage](https://www.servicenow.com/docs/access?context=Clone-UI&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Legacy clones and new clones are stored separately. Clones that you request via the Clone Admin Console are stored on a new table and displayed within the new console.  Legacy clones aren't shown in the Clone Admin Console. Clones that you initiate via the legacy Request Clone page are stored on the legacy Clone History table.


## UI changes

-   **[Creating a new clone preserver](https://www.servicenow.com/docs/access?context=clone-ui-request-clone&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    On the Create New Clone Data Preserver page, a message now notifies you of the Clone Duration Impact when you are using preservers. The message also instructs you to consider using conditions to preserve only the data that you need.

-   **[Scheduling calendar time slots](https://www.servicenow.com/docs/access?context=clone-ui-request-clone&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    On the Clone Request page, available time slots were added to the Scheduling Calendar.

-   **[Clone Duration time](https://www.servicenow.com/docs/access?context=clone-ui-request-clone&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    The clone duration timestamps now display properly.

-   **[Date and Timestamps](https://www.servicenow.com/docs/access?context=Clone-UI&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    The date and timestamps for clones are now in the system date and time format.

-   **[Clone completion progress bar](https://www.servicenow.com/docs/access?context=Clone-UI&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    The clone completion progress bar on the clone status page has been updated with accuracy improvements.

-   **[Clone restore progress](https://www.servicenow.com/docs/access?context=Clone-UI&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    The clone restore progress bar on the clone status page has been updated to include granular percentages.


## Related ServiceNow applications and features

-   **[System Clone](https://www.servicenow.com/docs/access?context=c_SystemClone&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Use the ServiceNow® System Clone application to copy everything in a database from one instance to another.


**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

