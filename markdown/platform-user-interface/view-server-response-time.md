---
title: View the server response time
description: View the server response times that are associated with your Next Experience instance by using the client interaction table.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Measuring the performance of your instance, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# View the server response time

View the server response times that are associated with your Next Experience instance by using the client interaction table.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Logs** &gt; **Client Interactions**.

2.  Select the personalized list icon \( ![Personalize list icon.](../../../use/using-lists/image/PersonalizeListIcon.png)\) within the Unified Navigation banner frame.

3.  Select the Interaction ID from the Available column and move it to the Selected column.

4.  Select **OK**.

    The client interaction table reloads to show the changes.

5.  Copy the interaction ID for the URL that you want to investigate.

6.  From the filter navigator, enter `syslog_transaction.list` in the search field.

7.  From the transaction table, select the personalize list icon ![](../../../use/using-lists/image/PersonalizeListIcon.png), within the banner frame.

8.  From the Available column, select the Client Interaction ID and move it to the Selected column.

9.  Select **OK**.

10. In the Transaction log list, select the Client Interaction ID and paste the interaction ID into the **Search** field.

11. Press **Enter**.

    The server response times for that particular interaction are displayed.


**Parent Topic:**[Measuring the performance of your instance in Next Experience](../concept/measuring-performance-next-experience.md)

