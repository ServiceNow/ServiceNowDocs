---
title: Recipients lists
description: Create the recipients list for a targeted communications that can include internal users, customers, accounts, contacts, and consumers. You can create the recipient list using the methods of user import, dynamic lists, or scripting.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Targeted communications, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Recipients lists

Create the recipients list for a targeted communications that can include internal users, customers, accounts, contacts, and consumers. You can create the recipient list using the methods of user import, dynamic lists, or scripting.

When an article is published, the recipients on this list can view the article on the Customer or Consumer Service Portal. Recipients can also receive optional email notifications.

Recipients lists are also used by the Major Issue Management application to create child cases for a major case.

Recipients lists are created in the following ways:

-   By creating a list of imported users.
-   By creating a dynamic list based on selected conditions.
-   By creating a script.

Recipients lists can have both dynamically generated and manually added records of the same type.

The system administrator can manage a scheduled job to refresh recipient lists. This scheduled job, **Targeted Communications Refresh recipient list**, adds new recipients to each of the active published articles. The new recipients receive email notification of the article and are granted access to view the article on the portal.

## Create a recipient list by importing contact information

Create a recipient list by importing contact information. For contacts, supported file types include xls and csv.

Multiple files can be imported into the same recipient list, with new recipients appended to the recipient list file. The system checks and imports only those accounts and contacts that exist in the system. Duplicate entries are not created. At the end of the import process, the system displays a status with the number of records imported and rejected.

The system uses the sys\_id and the email address attributes to match contacts. It first looks for a matching sys\_id match. If not found, it then looks for a matching email address. If neither are found, the record is rejected.

## Create a recipient list by importing account, consumer, or internal user information

Create a recipient list by importing account, consumer, or internal user information. The supported file type is xls.

The system uses the following attributes to match the imported records:

-   Account: Uses the sys\_id and the account number. Attempts to match the sys\_id. If not found, then attempts to match using the account number. If neither are found, the record is rejected.
-   Consumer and User: Uses the sys\_id or the email address. Attempts to match the sys\_id. If not found, then attempts to match the email address. If neither are found, the record is rejected.

**Note:** Column names are case sensitive. For example, use **sys\_id** and **number** for accounts and **email** for consumers and users.

## Create a recipient list using a script

Create a recipient list using a script with these supported entities: contact, company/account, consumer, and internal user. The output of the script is an array of sys\_ids of the corresponding entity. After creating the recipient list, the system shows the total number of records identified, added to the list, and rejected.

To create a recipient list using a script, select Dynamic Condition in the **Method** field on the Recipients List form and enable the **Show Script** check box. Then create your script in the **Script** field.

