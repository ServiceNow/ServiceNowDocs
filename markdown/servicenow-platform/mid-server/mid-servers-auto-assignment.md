---
title: Using MID Server IP range auto-assignment
description: Discovery Quick Start can automatically assign ranges of IP addresses, called subnets, to qualified MID Servers. This subnet auto-assignment requires SNMP credentials for read-only access to routers Discovery uses. The Automation Status Set form shows summary details of subnet Discoveries and the IP range assignments for associated MID Servers.Customers who use network service providers must request specific SNMP access to use MID Server IP range auto-assignment.The Automation Status Set form shows summary details of a subnet Discovery and the subsequent IP range assignments for MID Servers selected for automatic subnet assignment.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Using MID Server IP range auto-assignment

Discovery Quick Start can automatically assign ranges of IP addresses, called subnets, to qualified MID Servers. This subnet auto-assignment requires SNMP credentials for read-only access to routers Discovery uses. The Automation Status Set form shows summary details of subnet Discoveries and the IP range assignments for associated MID Servers.

<table id="table_gvt_qs4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>To be automatically assigned to a subnet, a MID Server must be:

-   In a running **\(Up\)** state.
-   Successfully validated.
-   Able to access one or more subnets in your network.

The subnet assignments that the instance makes for your MID Servers are stored in the Automation Status Set \[automation\_status\_set\] table. For details about MID Server auto-assignment, see [Discovery Quick Start](https://www.servicenow.com/docs/access?context=discovery-quick-start&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).

**Important:** You must auto-assign at least one MID Server to create a schedule automatically.

**Parent Topic:**[Configuring MID Servers](c_MIDServerConfiguration.md)

## Required SNMP OIDs for MID Server IP range auto-assignment

Customers who use network service providers must request specific SNMP access to use MID Server IP range auto-assignment.

IP range auto-assignment requires SNMP credentials for read-only access to all routers that Discovery uses to identify subnets. In addition, your service provider must grant the following SNMPWALK access:

-   iso.org.dod.internet.mgmt.mib-2.ip.ipRouteTable \(1.3.6.1.2.1.4.21\)
    -   ipRouteDest \(1.3.6.1.2.1.4.21.1.1\)
    -   ipRouteNextHop \(1.3.6.1.2.1.4.21.1.7\)
    -   ipRouteType \(1.3.6.1.2.1.4.21.1.8\)
    -   ipRouteMask \(1.3.6.1.2.1.4.21.1.11\)
-   iso.org.dod.internet.mgmt.mib-2.ip.ipForward.ipCidrRouteTable \(1.3.6.1.2.1.4.24.4\)
    -   ipCidrRouteDest \(1.3.6.1.2.1.4.24.4.1.1\)
    -   ipCidrRouteMask \(1.3.6.1.2.1.4.24.4.1.2\)
    -   ipCidrRouteNextHop \(1.3.6.1.2.1.4.24.4.1.4\)
    -   ipCidrRouteType \(1.3.6.1.2.1.4.24.4.1.6\)

## View automation status sets and IP range assignments

The Automation Status Set form shows summary details of a subnet Discovery and the subsequent IP range assignments for MID Servers selected for automatic subnet assignment.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Automation Status Sets**.

2.  Select a status record for a subnet Discovery you want to view.

    The form contains read-only status information about the selected Discovery, the subnets found, and the range assignment process for the MID Servers you selected for auto assignment.

    **Important:** IP ranges assigned manually prior to using auto-assignment in the [Discovery Quick Start](https://www.servicenow.com/docs/access?context=discovery-quick-start&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) are affected as follows:

    -   Individual IP ranges are retained and appended to the ranges assigned automatically by the system for the designated MID Server.
    -   If the MID Server was configured with the **ALL** ranges selection, the auto-assignment feature overwrites that designation with the ranges it finds.
    ![Automation Status Set form](../image/AutomationStatusSet.png "Automation Status Set form")

3.  Select the **Subnets Discovered** related list to view the list of subnets available for assignment.

    ![Subnets Discovered](../image/SubnetsDiscovered.png)

4.  Select the **IP Range Assignments** related list to view the IP ranges that were assigned to a MID Server.

    **Warning:** IP ranges identified by Discovery are stored in the IP collection \[ip\_address\_collection\] table, which is only used for MID Server IP range auto-assignment in the Jakarta release. This table is intended for future development and **should not** be used in any customizations, including column additions, business rules, or scripting actions.

    ![IP range assignments](../image/IPRangeAssignments.png)


