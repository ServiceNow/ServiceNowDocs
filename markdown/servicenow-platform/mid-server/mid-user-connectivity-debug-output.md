---
title: Interpreting MID Server user debugging output
description: Debugging output from the system log is available in either a summary or detailed view for MID Server user issues, but must be enabled manually.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Resolving MID Server issues, MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Interpreting MID Server user debugging output

Debugging output from the system log is available in either a summary or detailed view for MID Server user issues, but must be enabled manually.

To enable debugging and display all connectivity issues in either of the available formats, you must run a method manually on your instance. For instructions on enabling debugging, see [Test remediation efforts for MID Server user connectivity issues](mid-server-connectivity-issues.md#). For information about each error condition and how records are created in the MID Server Issue \[ecc\_agent\_issue\] table, see [MID Server user connectivity issues](mid-server-connectivity-issues.md#).

## Available formats

You can configure the instance to generate a simple summary of the issue or a detailed output that identifies users and MID Servers. Summaries provide a quick look at the issue conditions, by count, while the detailed view allows you to examine roles, MID Server associations, and login activity by named users.

In this summary example of an authorization issue, the instance evaluates each condition and indicates how many users met that condition. You can see that a MID Server is down and that one of two users configured for a MID Server failed authorization. Because this is a summary, neither the MID Server nor the users are named.

![Sample summary debug output](../image/DebugAuthorizationSummary.png "Sample summary debug output")

## Authentication failure

When a MID Server user cannot authenticate on the instance, the system displays these error messages in the detailed output:

-   **Login authentication failure for User &lt;user name&gt; associated with 1 down MID Server. Check password on MID server.**
-   **Login authentication failure for User &lt;user name&gt; associated with &lt;n&gt; down MID Servers. Check password on MID servers.**
-   **Login authentication failure for User &lt;user name&gt; with mid\_server role not associated with a MID Server.**

In this example, three users with the mid\_server role, **midserver2**, **local-midserver**, and **ardis.maison**, failed to authenticate. Two of these users were configured for MID Servers that were **Down**, and the other user was not configured for any MID Servers. Each of these users has an authentication failure and is named in the appropriate error message.

![Detailed debugging log for authentication failure](../image/MIDIssuesAuthDebugging.png "Detailed debugging log for authentication failure")

## MID Server ID map

The debugging output lists all MID Servers that are marked as **Down** and maps them to their user accounts by the MID Server **sys\_id**. This map includes all user accounts that have the mid\_server role, whether or not they are associated with a MID Server. If there are no **Down** MID Servers, the map is not displayed in the debugging output.

The map is presented in three sections:

-   User accounts not associated with any MID Servers.
-   User accounts associated with **Down** MID Servers, identified by their **sys\_id**.
-   The **sys\_id** of each **Down** MID Server, identified by name.

![MID Server ID map](../image/MIDDebugLookupTable.png "MID Server ID map")

## Authorization failure

If a user is missing any of the required roles, the instance generates these authorization failure messages:

-   **Login authorization failure for User &lt;user name&gt; associated with 1 down MID Server. Re-assign mid\_server role to grant all required roles.**
-   **Login authorization failure for User &lt;user name&gt; associated with &lt;n&gt; down MID Servers. Re-assign mid\_server role to grant all required roles.**
-   **Login authorization failure for User &lt;user name&gt; with mid\_server role not associated with a MID Server.**

In this example, three users with the mid\_server role, **midserver2**, **local-midserver**, and **ardis.maison** have failed authorization. One user is not associated with any MID Server, but the other two users are. The system has logged an authorization failure, indicating that the user is missing at least one critical role. To see what roles are missing, look at the comma separated list in the **Parm2** field in the **login.authorization.failed** event record. This record is the most recent login attempt in the Event \[sysevent\] table for the user account within the reporting period.

![Detailed debugging log](../image/MIDDebugAuthorizationFail.png "Detailed debugging log for authorization failure")

## Network issues

Network issues may exist for these users who are associated with MID Servers, but who have not attempted to log in during the reporting period:

-   **User &lt;user name&gt; is associated with 1 down MID Server. No login attempts within reporting period.**
-   **User &lt;user name&gt; is associated with &lt;n&gt; down MID Servers. No login attempts within reporting period.**

Network issues may also exist for these users who are NOT associated with MID Servers, and who have not attempted to log in during the reporting period: **User &lt;user name&gt; with mid\_server role is not associated with a MID Server. No login attempts within reporting period.**

In this example, no login attempts have been detected for **midserver2**, **local-midserver**, and **ardis.maison**, all of whom have the mid\_server role. Two of those users are associated with MID Servers that are marked **Down**. The other user is not associated with any MID Server. None of these users has attempted to log in to the system within the configured reporting interval. The system assumes that these users would make an attempt to log in unless network issues prevented them from doing so.

**Note:** By default, the sampling period is 4 hours. However, during debugging or remediation, the sampling period can be reset to a value that matches the MID Server heartbeat interval of 5 minutes, or greater.

![Detailed debugging log](../image/MIDDebugNetworkIssue.png "Detailed debugging log for network connection issues")

## Configuration issues

Any of the following messages can indicate a user configuration issue:

-   **Login authentication failure for User &lt;user name&gt; with mid\_server role not associated with a MID Server.**
-   **Login authorization failure for User &lt;user name&gt; with mid\_server role not associated with a MID Server.**
-   **User &lt;user name&gt; with mid\_server role successfully connected but not associated with a MID Server. The mid-server role should be reserved for MID Server use only.**
-   **User &lt;user name&gt; with mid\_server role is not associated with a MID Server. No login attempts within reporting period.**

In this example, a user with the mid\_server role has logged in successfully within the configured sampling interval. However, this user is not configured for a MID Server and might have the role in error.

![Detailed debugging log for MID Server user account login](../image/MIDDebugLoginSuccessful.png "Detailed debugging log for MID Server user account login")

**Parent Topic:**[Resolving MID Server issues](r_MIDServerTroubleshooting.md)

