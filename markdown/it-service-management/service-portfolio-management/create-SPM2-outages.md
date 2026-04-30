---
title: Log outages in Service Portfolio Management
description: Log outages to adjust your business or technical service commitment availability.
locale: en-US
release: xanadu
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Service Portfolio Management, Service Portfolio Management, IT Service Management]
---

# Log outages in Service Portfolio Management

Log outages to adjust your business or technical service commitment availability.

## Before you begin

Role required: service\_editor

## About this task

Service Portfolio Management tracks and reports on outages for all business or technical service offerings that include availability commitments.

The outage is used to evaluate the availability of the offering and appears in the reports generated for this offering. There are three types of outages:

-   **Outage**: An unplanned outage that could be caused by hardware or network issues. The only type of outage that's considered when calculating the availability of a business or a technical service.
-   **Planned Outage**: A necessary, expected outage caused by planned maintenance or an upgrade.
-   **Degradation**: A problem that affects a business or technical service but doesn't result in a disruption of that service.

Outage records can relate to multiple configuration items \(CIs\). You can link a single outage to multiple CI records using the Affected CIs related list.

**Note:** An outage must be created and saved before you can add a CI relation or link an outage to multiple CI records using the Affected CIs related list.

View a unique **Outage Number** identifier for your outage records. View the Outage Number column in the Outage table records list and on the Outage form.

**Note:** The Outage Numbering plugin \(com.snc.outage\_numbering\) must be activated to introduce number data. The plugin is automatically activated for all instances and upgrades except those instances that already have a number prefix column on the Outage table. If the plugin isn't active and you want to move to the base system field, see the [Activate Outage Numbering plugin \[KB0823685\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0823685) article in the HI Knowledge Base or contact Customer Service and Support.

When an outage is opened against a business or technical service, all child offerings are added to the Affected CI related list on the outage form. A pop-up message notifies you that the outage affects all child offerings. If needed, the offerings can be removed from the Affected CIs related list.

## Procedure

1.  Navigate to **Service Portfolio Management** &gt; **Outages**.

2.  Select **New** to create an outage or find the business or technical service offering in the Outages records list **Configuration item** field to edit.

    -   If creating an outage, the Outage form opens.
    -   If editing an existing outage, select the outage in the **Type** field.
3.  Edit the **Type** field as necessary or choose **None**.

4.  Enter text in the **Message** field.

5.  Enter the length of the outage.

    -   Select the **Begin** and **End** dates and times with the calendar or
    -   Enter the **Duration** as a function of days and hours.
6.  Select and hold \(or right-click\) in the form header to save the record or select **Submit** or **Update** if editing an existing outage record.

    **Note:**

    If a single outage impacts multiple business or technical service offerings, you can add those offerings to the Affected CIs related list.

7.  To add an associated affected CI, select **Add**.

    All affected CIs are listed in the **Service Offering** configuration class.

8.  Select a single CI or group of CIs.

    Select the box next to the CI name and then select **Add Selected**. Alternatively, you can choose to add all the listed affected CIs to the outage record by selecting **Add All**.

9.  Close the Add Affected Configuration Items list window.

    The CI or CIs are added to the Affected CIs related list.

10. Select **Update**.


**Parent Topic:**[Using Service Portfolio Management](../concept/SPM2-using.md)

