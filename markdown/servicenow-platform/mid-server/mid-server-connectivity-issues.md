---
title: MID Server user connectivity issues
description: The instance writes issues involving MID Server user logins and network connectivity to the MID Server Issue \[ecc\_agent\_issue\] table and creates events you can use in custom scripts or to send email notifications.After attempting to resolve a user connectivity issue that appears in the MID Server Issue \[ecc\_agent\_issue\] table, you can test your remediation efforts without having to wait until the next scheduled reporting period by shortening the sampling interval.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [Resolving MID Server issues, MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server user connectivity issues

The instance writes issues involving MID Server user logins and network connectivity to the MID Server Issue \[ecc\_agent\_issue\] table and creates events you can use in custom scripts or to send email notifications.

Records in the MID Server Issue \[ecc\_agent\_issue\] table can provide insight into why your MID Server user cannot log in or why a MID Server cannot connect to the instance. The system displays records for connectivity problems in this table that include informative error messages suggesting possible causes. By default, a scheduled job called MIDUserConnectivity runs every four hours and launches the MIDUserConnectivity script include to evaluate MID Server connection activity. Records in the MID Server Issue \[ecc\_agent\_issue\] table reflect the status of MID Server login attempts and connectivity at the time the scheduled job runs.

From the perspective of the instance, the MID Server is **Down** when:

-   User authentication fails
-   User authorization fails.
-   Network issues prevent MID Server from establishing a TCP/IP connection.

**Note:** To associate a user with a MID Server, navigate to the `servicenow/<mid server name>/agent/config.xml` file and enter the user credentials in the **mid.instance.username** and **mid.instance.password** parameters. Make sure to restart the MID Server to activate your changes.

## How issues are logged

User authentication failures and authorization issues are logged automatically to the MID Server [agent log file](../concept/ecc-queue-mid-server.md#). The message for both is the same: **User cannot be authenticated or is missing the proper roles.** If the issue is related to authorization, the `agent.log` file shows the list of missing roles.

When debugging is enabled, MID Server issues are logged to the system log \(syslog\) and are available for display in either a [summary or a detailed](mid-user-connectivity-debug-output.md) format. You can also change the sampling interval from the default 4 hours to something shorter for tracking your remediation efforts. For instructions on enabling and configuring debugging for MID Server user issues, see [Test remediation efforts for MID Server user connectivity issues](mid-server-connectivity-issues.md#).

## Data provided

When the instance encounters user connectivity issues, it opens a record in the MID Server Issue \[ecc\_agent\_issue\] table.

![Example user authentication error message](../image/MIDIssueAuthenticationFailNoAssoc.png "Example user authentication error message")

The MID Server Issue table contains these fields:

<table id="table_ytb_ccy_1z"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Last detected

</td><td>

Date and time the issue was last detected.

</td></tr><tr><td>

Short description

</td><td>

Contents of the generated message that specifies a possible issue with the named user or the MID Server.

</td></tr><tr><td>

MID Server

</td><td>

Empty in the Jakarta release.

</td></tr><tr><td>

Issue source

</td><td>

The process that identified the issue. For all issues with MID Server user connectivity, the source is MIDUserConnectivity.

</td></tr><tr><td>

State

</td><td>

The current state of the issue. Possible states are:-   **New**: Starting state when the instance creates the issue.
-   **Acknowledged**: State set when the administrator first examines the issue.
-   **Resolved**: Ending state, set by the instance, indicating that the issue has been resolved. If the scheduled job does not encounter the issue when it runs again, the instance automatically sets this value.

</td></tr><tr><td>

Domain

</td><td>

Domain associated with the MID Server user account.

</td></tr><tr><td>

Count

</td><td>

Number of times an issue has been detected. Each time the scheduled job runs and encounters the same issue, it increments this field.

</td></tr></tbody>
</table>## User authentication failure

The credentials that the instance uses to authenticate a MID Server user are configured in the MID Server Configuration Parameters \[ecc\_agent\_config\] table. If the MID Server user attempts to log into the instance with invalid credentials, the instance rejects the connection, and writes the **login.failed** event to the Events \[sysevents\] table for the user. Administrators can use this event in a custom script or in email notifications for authentication failure.

**Note:** If user authentication fails, user authorization is not attempted.

**User accounts associated with a MID Server**

Either of the following messages in the MID Server Issue \[ecc\_agent\_issue\] table indicate authentication failure for user accounts that are associated with a MID Server:

-   **Login authentication failure for User &lt;user name&gt; associated with 1 down MID Server. Check password on MID server.**
-   **Login authentication failure for User &lt;user name&gt; associated with &lt;n&gt; down MID Servers. Check password on MID servers.**

The necessary conditions for these messages to appear are:

-   The **Status** field in the MID Servers \[ecc\_agent\] table that is associated with the MID Server indicates that the MID Server is **Down**.
-   The user identified in the MID Server Configuration Parameters \[ecc\_agent\_config\] table is the user that one or more MID Servers is configured to use for authentication and authorization when connecting to the instance. The record in the \[ecc\_agent\_config\] table must have these values:
    -   Parameter name \[param\_name\] field set to **mid.instance.username**.
    -   Value \[value\] field set to the user’s name, corresponding to the User ID \[user\_name\] field in Users \[sys\_user\] table.
-   The Events \[sysevent\] table contains posts showing that the last login attempt associated with the user failed during the scheduled time period. The record created in the \[sysevent\] table contains these field values:
    -   Event Name \[name\] field is set to **login.failed**.
    -   Parm1 \[parm1\] field is set to the user’s name.

**Note:** The MID Server \[mid\_server\] field in the MID Server Issues \[ecc\_agent\_issue\] table is empty \(=NULL\).

**User accounts with the mid-server role not associated with a MID Server**

The following message appears when a user with the mid\_server role who is not associated with a MID Server fails to authenticate: **Login authentication failure for User &lt;user name&gt; with mid\_server role not associated with a MID Server.**

The necessary conditions for this message to appear are:

-   The User Roles \[sys\_user\_has\_role\] table contains a record linking the sys\_id associated with the user record stored in the \[sys\_user\] table, with the sys\_id associated with the mid\_server role record stored in the \[sys\_user\_role\] table.
-   The user is not identified in the MID Server Configuration Parameters \[ecc\_agent\_config\] table as the user whom one or more MID Servers are configured to use for authentication and authorization when connecting to the instance.
-   The Events \[sysevent\] table contains posts showing that the last login attempt associated with the user failed during the scheduled time period.
    -   The \[sysevent\] table contains a record with the Event Name \[name\] field set to **login.failed**.
    -   The Parm1 \[parm1\] field is set to the user’s name, corresponding to the User ID \[user\_name\] field in Users \[sys\_user\] table.

**Note:** The MID Server \[mid\_server\] field in the MID Server Issues \[ecc\_agent\_issue\] table is empty \(=NULL\).

## User authorization failure

The user authorization check occurs after the MID Server has successfully authenticated on the instance. In this step, the system ensures that the user account associated with a MID Server is granted the minimum roles required. A SOAP web service called MIDServerCheck performs the role checking on the instance. If the MID Server user has the proper roles, the connection is allowed and a **login** event is written to the Events \[sysevents\] table. If the user does not have the proper roles, the instance writes a **login.authorization.failed** event to the Events \[sysevents\] table. This event provides a comma separated list of the user's missing roles. Administrators can use this event in custom scripts or in email notifications for authorization failure.

Authorization can fail if a user is missing the mid\_server role or any of the important SOAP roles, as in these cases:

-   If the user has the soap\_script role, the MIDServerCheck SOAP web service runs to check for the appropriate MID Server roles. If the user lacks the mid\_server role or any of the other SOAP roles, authorization fails, and the **login.authorization.failed** event is created.
-   If the user is missing the soap\_script role, that user is not authorized to launch the MIDServerCheck SOAP web service, which checks for all required MID Server roles. Authorization fails, but the **login.authorization.failed** event is not created. When this occurs, the instance displays this message: **Connectivity of MID Server user &lt;user name&gt; cannot be detected by the instance**.

**Users associated with one or more down MID Servers**

Either of the following messages in the MID Server Issue \[ecc\_agent\_issue\] table indicate authorization failure for user accounts that are associated with a MID Server that is **Down**:

-   **Login authorization failure for User &lt;user name&gt; associated with 1 down MID Server. Re-assign mid\_server role to grant all required roles.**
-   **Login authorization failure for User &lt;user name&gt; associated with &lt;n&gt; down MID Servers. Re-assign mid\_server role to grant all required roles.**

The **MIDUserConnectivity** script include identifies active users associated with one or more down MID Servers whose last login attempt within the reporting period failed user authorization. This message is generated when user authorization failures are detected and reported by the MIDServerCheck scripted web service. However, user authorization failures are not reported for users who are not assigned the soap\_script role. Should this occur, problems with the user are reported by the network connectivity message.

This message appears in the MID Server Issue \[ecc\_agent\_issue\] table when:

-   The user may or may not have the mid\_server role.
-   The user is identified in the MID Server Configuration Parameters \[ecc\_agent\_config\] table as the user whom one or more MID Servers are configured to use for authentication and authorization when connecting to the instance.
-   The Events \[sysevent\] table contains posts showing that the last login attempt associated with the user failed during the scheduled time period. The \[sysevent\] table contains a record with these settings:
    -   Event Name \[name\] field set to **login.authorization.failed**.
    -   Parm1 \[parm1\] field set to the user’s name, corresponding to the User ID \[user\_name\] field in Users \[sys\_user\] table.

**Note:** The MID Server \[mid\_server\] field in the MID Server Issues \[ecc\_agent\_issue\] table is empty \(=NULL\).

**Users with the proper role not associated with a MID Server**

The following message appears when a user with the mid\_server role who is not associated with a MID Server fails authorization: **Login authorization failure for User &lt;user name&gt; with mid\_server role not associated with a MID Server.**

This message is generated when user authorization failures are detected in which the user account, with the mid\_server role, is not identified as a configured MID Server user in the \[ecc\_agent\_config\] table. It is possible that the user account was associated with a MID Server at the time of the failure.

This message appears in the MID Server Issue \[ecc\_agent\_issue\] table when:

-   The user has the mid\_server role. The User Roles \[sys\_user\_has\_role\] table has a record linking the sys\_id associated with the user record stored in the \[sys\_user\] table, with the sys\_id associated with the mid\_server role record stored in the \[sys\_user\_role\] table.
-   The user is not identified in the MID Server Configuration Parameters \[ecc\_agent\_config\] table as the user whom one or more MID Servers are configured to use for authentication and authorization when connecting to the instance.
-   The Events \[sysevent\] table contains posts showing that the last login attempt associated with the user failed during the scheduled time period. The \[sysevent\] table contains a record with these settings:
    -   Event Name \[name\] field set to **login.authorization.failed**.
    -   Parm1 \[parm1\] field set to the user’s name, corresponding to the User ID \[user\_name\] field in Users \[sys\_user\] table.

**Note:** The MID Server \[mid\_server\] field in the MID Server Issues \[ecc\_agent\_issue\] table is empty \(=NULL\).

## Network issues

A network issue can prevent the MID Server from connecting to the instance's TCP/IP server to begin a session. In this case, the instance marks the MID Server as **Down**, because the instance failed to receive the MID Server heartbeat within the prescribed 5 minute interval.

**Users associated with down MID Servers who have not attempted to log in**

Either of the following messages in the MID Server Issue \[ecc\_agent\_issue\] table name users associated with MID Servers who have not attempted to log in during the reporting period:

-   **User &lt;user name&gt; is associated with 1 down MID Server. No login attempts within reporting period.**
-   **User &lt;user name&gt; is associated with &lt;n&gt; down MID Servers. No login attempts within reporting period.**

The MIDUserConnectivity script include reports active users associated with down MID Servers where network connectivity cannot be detected by the instance.

This message appears in the MID Server Issue \[ecc\_agent\_issue\] table when:

-   The user may or may not have the mid\_server role.
-   The user is identified in the MID Server Configuration Parameters \[ecc\_agent\_config\] table as the user which one or more MID Servers are configured to use for authentication and authorization when connecting to the instance.
-   There are no login attempts, either failed or successful, recorded in the Events \[sysevent\] table for the user during the scheduled reporting period.

**Note:** The MID Server \[mid\_server\] field in the MID Server Issues \[ecc\_agent\_issue\] table is empty \(=NULL\).

**Users not associated with MID Servers who have not attempted to log in**

The following message appears when a user with the mid\_server role who is not associated with a MID Server has not attempted to login during the configured reporting interval: **User &lt;user name&gt; with mid\_server role is not associated with a MID Server. No login attempts within reporting period.**

The MIDUserConnectivity script include reports active users with the mid\_server role not associated with a MID Server, where connectivity cannot be detected by the instance.

This message appears in the MID Server Issue \[ecc\_agent\_issue\] table when:

-   The user has the mid\_server role. The User Roles \[sys\_user\_has\_role\] table has a record linking the sys\_id associated with the user record stored in the \[sys\_user\] table, with the sys\_id associated with the mid\_server role record stored in the \[sys\_user\_role\] table.
-   The user is not identified in the MID Server Configuration Parameters \[ecc\_agent\_config\] table as the user whom one or more MID Servers are configured to use for authentication and authorization when connecting to the instance.
-   There are no login attempts, either failed or successful, recorded in the Events \[sysevent\] table for the user during the scheduled reporting period.

**Note:** The MID Server \[mid\_server\] field in the MID Server Issues \[ecc\_agent\_issue\] table is empty \(=NULL\).

## Configuration issues

Any of the following messages, discussed above, can indicate a configuration issue:

-   **Login authentication failure for User &lt;user name&gt; with mid\_server role not associated with a MID Server.**
-   **Login authorization failure for User &lt;user name&gt; with mid\_server role not associated with a MID Server.**
-   **User &lt;user name&gt; with mid\_server role is not associated with a MID Server. No login attempts within reporting period.**

These are some common configuration errors:

-   An administrator neglected to associate the user record with the MID Server record as shown in the MID Server Configuration Parameters \[ecc\_agent\_config\] table. This table is read-only and cannot be updated directly. To associate a user with a MID Server, configure the user name and password in the MID Server's `config.xml` file and restart the MID Server.
-   During the process of reconfiguring a MID Server to use a different account for TCP/IP connection, the administrator has not yet removed the mid\_server role from the account or deleted the account.
-   A multipurpose user account was created and granted a large number of roles, including the mid\_server role, although this account was never intended to be used as a MID Server account.

**User who successfully authenticates and authorizes but might not need mid\_server role**

The following message appears when a user with the mid\_server role who is not associated with a MID Server successfully logs in: **User &lt;user name&gt; with mid\_server role successfully connected but not associated with a MID Server. The mid\_server role should be reserved for MID Server use only.**

The MIDUserConnectivity script include reports active users with the mid\_server role who are not identified as a configured MID Server user, and whose last login attempt was successful during the scheduled time period. This message suggests that the user’s credentials are being used by a system administrator or a process that is not running on a MID Server. The assumption here is that the mid\_server role should only be used for applications deployed to a MID Server. The presence of this message reminds the system administrator to remove extraneous mid\_server roles from user accounts that do not require them.

This message appears in the MID Server Issue \[ecc\_agent\_issue\] table when:

-   The user has the mid\_server role.
-   The user is not identified in the MID Server Configuration Parameters \[ecc\_agent\_config\] table as the user whom one or more MID Servers are configured to use for authentication and authorization when connecting to the instance.
-   The Events \[sysevent\] table contains posts showing that the last login attempt associated with the user succeeded during the scheduled time period. The \[sysevent\] table contains a record with these settings:
    -   Event Name \[name\] field set to **login**.
    -   Parm1 \[parm1\] field set to the user’s name, corresponding to the User ID \[user\_name\] field in Users \[sys\_user\] table.

**Note:** The MID Server \[mid\_server\] field in the MID Server Issues \[ecc\_agent\_issue\] table is empty \(=NULL\).

**Parent Topic:**[Resolving MID Server issues](r_MIDServerTroubleshooting.md)

## Test remediation efforts for MID Server user connectivity issues

After attempting to resolve a user connectivity issue that appears in the MID Server Issue \[ecc\_agent\_issue\] table, you can test your remediation efforts without having to wait until the next scheduled reporting period by shortening the sampling interval.

### Before you begin

Role required: admin

### About this task

Reconfigure the sampling interval using this procedure and then examine the results in the MID Server Issue \[ecc\_agent\_issue\] table. You can set any time span for the sample, but you should define a window of not less than 5 minutes, since this is the default interval of the MID Server heartbeat that reports its status. The recommended method for configuring a shorter sampling interval is to copy and modify the code from the MIDUserConnectivity scheduled job, and then run it manually in the background script utility.

**Warning:** Avoid editing the script in the MIDUserConnectivity schedule record. If you make any change to this record, it will not be updated when you upgrade the instance.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open the MIDUserConnectivity scheduled job.

3.  Copy this line from the **Run this script** field:

    `MIDUserConnectivity(0).checkConnectivity(4 * (60 * 60 * 1000));`

    This code sets the 4 hour sampling interval in milliseconds and turns debugging off with the **MIDUserConnectivity\(0\)** value.

4.  Navigate to **System Definition** &gt; **Scripts - Background**.

5.  Paste the code from the scheduled job into the **Run script** field.

6.  Set the sampling interval to 5 minutes by changing the time calculation to **\(5 \* 60 \*1000\)**.

    The modified command looks like this: `MIDUserConnectivity(0).checkConnectivity (5 * 60 *1000);`

7.  Click **Run script**.

8.  Open the record of the MID Server that had the issue and select the **MID Server Issues** related list.

    The issue is updated as follows:

    -   If the issue persists, the **Count** column is incremented, and the **Last detected** column shows the current date and time.
    -   If the issue no longer exists, the system changes the **State** to **Resolved**.
9.  You can enable debugging by selecting a level, and then run the script again to see the breakdown for each condition evaluated.

    Use these settings to select a debugging level:

    -   For a summary view, enter **MIDUserConnectivity\(1\)**.
    -   For a detailed view, enter **MIDUserConnectivity\(2\)**.
    For details about the type of debugging information provided, see [Interpreting MID Server user debugging output](mid-user-connectivity-debug-output.md).


