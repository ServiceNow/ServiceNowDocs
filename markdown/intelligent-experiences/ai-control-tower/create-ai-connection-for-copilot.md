---
title: Create AI connection for Copilot
description: Create an AI connection for Copilot in AI Control Tower using the  AI Service Graph Connector for Microsoft.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft, Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# Create AI connection for Copilot

Create an AI connection for Copilot in AI Control Tower using the  AI Service Graph Connector for Microsoft.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and n\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower workspace** &gt; **Configurations** &gt; **AI connections**.

2.  Select **Add**.

3.  Select **AI connector for Microsoft** from all the available connectors.

4.  Select **Create connection**.

5.  Select the Microsoft Copilot check box.

6.  Review setup instructions page displays.

    **Note:** Verify to follow all the prerequisite steps.

7.  Expand Create Copilot connection section.

8.  Select **Continue**.

9.  Setup page appears

10. **Configure and test Copilot connection**

    1.  Enter the **Connection name**.

    2.  Enter the **Connection URL** \(https://&lt;provider-domain-name&gt;.com\).

    3.  Enter the **OAuth client ID**.

    4.  Enter the OAuth client secret.

    5.  Enter the OAuth token URL \(Tenant id\).

    6.  Select **Create and test connection**

    7.  Select **Continue**.

11. **Configure import schedule**

    1.  Verify that both the parent-scheduled jobs, Discovery and Execution are active as they’re shipped base system inactive.

        Verify to execute the Discovery-scheduled job first.

    2.  Set the run frequency.

    3.  To run frequency by demand, select Execute now to run.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  Select **Continue**.

    5.  Select **View all connections** to view the newly created connection.


## Result

An AI connection is created for Copilot.

