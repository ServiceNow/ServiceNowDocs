---
title: View a password expiration table
description: You can view a password expiration table and validate whether a record is created in it.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure password expiration reminder, Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# View a password expiration table

You can view a password expiration table and validate whether a record is created in it.

## Before you begin

Role required: password\_reset\_admin

## About this task

This table contains the password expiration information of an individual user in each process that the user is entitled to. The expiration framework uses this table information to send the expiration notification reminders across the credential stores. You can also view details of the record, such as if there are any errors, error logs, or password expiration dates.

## Procedure

1.  Select **All** and then enter **pwd\_expiration.list** in the navigation filter.

    The Password Expirations page shows the table with the generated records.

2.  View the various columns that you want to use in the table and validate the information.

    |Column Name|Description|
    |-----------|-----------|
    |Users|Shows the reference to the sys\_user table.|
    |Password Reset Process|Shows the reference to the password reset process table. The process that a user belongs to and for which you have configured password expiration.|
    |Last Password Reset Date|Shows the last date when the user reset the password.|
    |Password Expiration Date|Shows the date that indicates when the password is going to expire.|
    |Send Notification|Shows whether password expiration notifications are to be sent or not.|
    |Active|Shows the status of the password expiration record. For example, suppose that a user is no longer associated with the process. In that case, the record shows the value as **false**. It means that the record is inactive and the scheduled process does not fetch the data for that user. The **true** value indicates that the record is active.|
    |Error Count|Shows whether there is any error while getting information about the user password expiration. For example, when getting information about a user’s password expiration while calling an external credential store, an error might occur.|
    |Last Refresh Date|Shows the last date when the record was refreshed from an external system.|
    |Last Error Log|Shows the last error log if there is any error while getting information about the user’s password expiration.|

    **Note:** The password expiration table stores the password expiration information of different users for different password reset processes because both the tables are data domain separated. The password expiration table is also data domain separated. For more information about domain separation, see [Domain separation and the Password Reset application](../concept/domain-separation-pwd-reset.md).


**Parent Topic:**[Configure password expiration reminder](password-reset-expiration-setup.md)

