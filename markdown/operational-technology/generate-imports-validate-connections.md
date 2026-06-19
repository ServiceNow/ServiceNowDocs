---
title: Generate imports and validate the connections
description: For each ServiceNow OT Discovery connection, configure the name and run as user for each import job. Each connection will generate a new Scheduled Import Set and Data Source.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/generate-imports-validate-connections.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Generate imports and validate the connections

For each ServiceNow OT Discovery connection, configure the **name** and **run** as user for each import job. Each connection will generate a new **Scheduled Import Set** and **Data Source**.

## Before you begin

Role required: admin

## Procedure

1.  Next to the **Generate imports** task, select **Configure**.

    The Generate imports for the ServiceNow OT Discovery Connection page opens.

2.  In the **Run As User** field, select System administrator.

    This is the role within the platform who will run the schedules.

3.  Select **Generate**.

    Because the Table permissions were set to Can Read, Can Create, and Can Update, this starts creating scheduled jobs in the background.

4.  When finished, the banner at the top of the page states "Successfully generated import objects for connection OT Discovery."

5.  Return to the Guided Setup and select **Mark as complete** next to the Generate imports task.

6.  For the **Validate the connection** section, select **Configure**.

7.  On the next page, check the box next to OT Discovery.

8.  Under the header, **Related Links**, select **Test Connection**

9.  Testing the connection takes a few moments and once completed, the page refreshes to show the test results.

    The connection is successful if the Status Code is 200. If there's an Error Code and Error Message, the connection failed and further troubleshooting is required.

    \[Omitted image "success.png"\] Alt text: Connection is successful

10. Select the OT Discovery link.

    This opens the Service Graph Connector OT Discovery view.

11. The table lists the connection properties, the data sources that were generated and the 7 import schedules that were created.

12. This task tests:

    -   Is the Service Graph Connector able to reach the Instance.
    -   If so, is there a valid license on the Console.
    If the connection was successful, but the Console license has expired, you may see a message in the Suggestion field asking you to reach out to your account representative.

13. Return to the Validate the connection section and select **Mark as complete**.

14. Return to the Guided Setup page.


