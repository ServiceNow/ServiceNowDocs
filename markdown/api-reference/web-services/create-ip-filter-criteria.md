---
title: Create IP filter criteria
description: Define which IP addresses or IP ranges are permitted to connect to your ServiceNow instance via the Live Connect ODBC/JDBC driver.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/create-ip-filter-criteria.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Live Connect configuration on your ServiceNow instance, Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Create IP filter criteria

Define which IP addresses or IP ranges are permitted to connect to your ServiceNow instance via the Live Connect ODBC/JDBC driver.

## Before you begin

-   Consult your network team to identify the IP address range for your ODBC or JDBC client machines. You may need to use the external IP address rather than the internal IP address, depending on your network configuration.
-   Complete the configuration steps:
    -   [Assign roles and create service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/create-service-account.md)
    -   [Create Access Control Lists \(ACLs\) for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/create-acls-sql-api.md)

Role required: admin

## About this task

By default, all incoming IP addresses are blocked for Live Connect connections. Configure the Authentication Policy with an IP filter and policy condition to allow access only from trusted client machines.

This is the third and final configuration procedure for enabling Live Connect access on your instance. After completing this task, your user account \(personal or service account\) can connect to ServiceNow via ODBC or JDBC from the specified IP addresses.

**Note:** For additional details on IP filtering, refer to the [IP filter documentation](https://www.servicenow.com/docs/r/platform-security/authentication/create-ip-filter-criteria.html) in the ServiceNow Platform Security guide.

## Procedure

1.  Navigate to the **All** &gt; **Adaptive Authentication** &gt; **Authentication Policies** &gt; **All Policies**.

2.  Search for **Live Connect Authentication Policy** and open it.

3.  From the **Policy Inputs** tab, select **New**.

    A screen appears asking "What kind of Policy Input \(Filter Criteria\) do you want to create?"

4.  Select **IP Filter Criteria**.

5.  On the IP Filter Criteria form, enter the following information:

    -   **Name**: Enter a name to identify this IP filter group \(for example, AllowedIPRange\).
    -   **Description**: Enter a description \(for example, Allowed IP addresses for ODBC/JDBC connections\).
6.  From the **IP Range** tab, double-select the **Start IP** column to insert a new row.

    Enter the IP address range for ODBC/JDBC client machines that are allowed to connect:

    -   **Start IP**: Enter the starting IP address of the range.
    -   **End IP**: Enter the ending IP address of the range. For a single IP address, enter the same value in both Start IP and End IP.
    -   **Description**: Enter a description.
    The IP addresses you enter are the outbound IP addresses, not the internal IP addresses. Your IT team can provide this information. These are the machines from which BI tools and analytics platforms will connect to ServiceNow.

7.  Select **Submit**.

    The page returns to the Live Connect Authentication Policy form.

8.  Go to the **Policy Conditions** tab and select **New**.

9.  On the Condition form, enter the following information:

    -   **Label**: Enter a label to identify this policy condition \(for example, AllowedIPs\).
    -   **Description**: Enter a description of this policy condition \(for example, Allowed IPs for ODBC\).
10. In the Condition section, select **Add Filter Condition**.

    -   From the first drop-down list, select the name of the IP filter criteria you created earlier.
    -   From the second drop-down list, select **is**.
    -   From the third drop-down list, select **true**
    The condition evaluates whether the connecting IP address matches your allowed IP filter criteria.

11. Select **Submit**.

    The condition appears in the Policy Conditions list on the Live Connect Authentication Policy form.


## Result

You have successfully configured IP filtering for Live Connect access. Your ServiceNow instance will now accept Live Connect connections only from the specified IP addresses or IP ranges. All other connection attempts will be blocked by default.

Your user account \(personal or service account\) can now connect to ServiceNow via ODBC or JDBC from the permitted client machines.

**Parent Topic:**[Live Connect configuration on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configure-sql-api-overview.md)

