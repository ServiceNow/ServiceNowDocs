---
title: Identify potentially exposed users
description: When a user has indicated a health condition on a self-report, use Emergency Exposure Management to identify other users who might have come in contact with the affected user. You can analyze multiple data sources, such as location, meetings, workspace reservations, badge scans, and Wi-Fi access data of the affected user to identify potentially exposed users.
locale: en-US
release: yokohama
product: Emergency Exposure Management
classification: emergency-exposure-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Emergency Exposure Management, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Identify potentially exposed users

When a user has indicated a health condition on a self-report, use Emergency Exposure Management to identify other users who might have come in contact with the affected user. You can analyze multiple data sources, such as location, meetings, workspace reservations, badge scans, and Wi-Fi access data of the affected user to identify potentially exposed users.

## Before you begin

To query through multiple data sources, the Emergency Exposure Management requires the following applications, plugins, and configurations available on your instance.

-   **[Microsoft Office 365](set-up-emergency-exposure-mgmt.md)**

    Register and configure to scan Microsoft Outlook meeting data.

-   **[Contact Tracing](../../contact-tracing/task/install-contact-tracing.md#)**

    Badge reader scan, user daily contact log, Wi-Fi access log, handheld or wearable device proximity data,and visitor data.

-   **[Employee Health Screening](../../employee-health-screening/task/install-emp-health-screening.md#) and Contact Tracing**

    Scans visitor data.

-   **[Field Service Management](https://www.servicenow.com/docs/access?context=t_ActivateFieldServiceManagement&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US) \(com.snc.work\_management\)**

    Scans field service task data.


**Important:**

If you are an on-premise customer with Microsoft Office 365 and you need assistance in configuring Emergency Exposure Management, contact your sales representative or contact Customer Service and Support at [https://support.servicenow.com/now?draw=case](https://support.servicenow.com/now?draw=case).

Role required: sn\_imt\_diagnosis.diagnostics\_admin or admin

## About this task

**Note:** You cannot create or run a diagnostic request for affected users who have not consented to use their data for contact tracing. For more information, see [User privacy consent for Contact Tracing](../../contact-tracing/concept/contact-tracing-user-privacy.md).

## Procedure

1.  Navigate to **All** &gt; **Emergency Exposure Management** &gt; **Create New**.

    The **Report generation status** field is set to **Not Initiated** and the **Active** check box is selected.

2.  From the **Affected user** field, select the user's name.

3.  Click the lock icon \(![lock icon](../image/lock-icon.png)\) in the **Tracing system** field and select one or more tracing system options to query corresponding data sources.

    You can select multiple sources together for better identification of potentially impacted users.

<table id="table_sgm_ndx_cmb"><thead><tr><th>

Tracing system\(Required application/plugin\)

</th><th>

Query

</th></tr></thead><tbody><tr><td>

**Location**

</td><td>

Users co-located with the affected user, for example, on the same floor or building.

</td></tr><tr><td>

**Outlook meetings** \( Microsoft Office 365\)

</td><td>

Users who accepted the same meetings as the affected user during the specified time period.

</td></tr><tr><td>

**Workplace reservations** \( Workplace Core\)

</td><td>

Users who had reservations for the same shifts as the affected user during the specified time period.

</td></tr><tr><td>

**Badge reader** \( Contact Tracing\)

</td><td>

Users who swiped their badge on the same badge reader devices as the affected user, during the specified time period.

</td></tr><tr><td>

**Employee daily log** \( Contact Tracing\)

</td><td>

The list of users with whom the affected users interacted during the specified time period.

</td></tr><tr><td>

**Visitor log** \( Contact Tracing and Employee Health Screening\)

</td><td>

The list of visitors who interacted with the affected user during the specified time period. Visitors who are invited by the affected user and have been screened through and let in are queried.

</td></tr><tr><td>

**Wi-Fi access log** \( Contact Tracing\)

</td><td>

Users who used the same Wi-Fi access points as the affected user during the specified dates.Wi-Fi access log data used to identify potentially impacted users depends on the Wi-Fi location preferences and the available integrations.

 For more information, see [Retrieving Wi-Fi access log data](../../contact-tracing/concept/wifi-access-management.md).

 **Note:** Data received via a real-time API will be for a period based on the data retention policy of your Wi-Fi service provider.

</td></tr><tr><td>

**Handheld/Wearables** \( Contact Tracing\)

</td><td>

Users using handheld or wearable devices in the close proximity with the affected user for more than the permissible time during the specified time period.

</td></tr><tr><td>

**Kinexon SafeZone** \( Contact Tracing\)

</td><td>

Users who with KINEXON wearables who were in close proximity with other KINEXON users during the specified dates. Data acquired from the KINEXON SafeZone API. Requires an active KINEXON integration.For more information, see [Configure KINEXON integration](../../contact-tracing/task/configure-kinexon-integration.md).

 **Note:** Users who are required to agree to a privacy consent but have not done so are excluded even if they are potentially exposed contacts.

</td></tr><tr><td>

**Field service** \( Field Service Management\)

</td><td>

Customers attended by an affected field agent during the specified time period. Also queries other field agents who interacted with the affected agent or visited the same customer as the affected agent during the specified time period.

</td></tr></tbody>
</table>4.  When required for a selected tracing system, provide the start and end dates.

    1.  In the **Start date** field, provide the estimated date of infection.

        Because the infection window that you're concerned about may vary, pick a start date such as 14 days prior to the date of reported symptoms.

    2.  In the **End date** field, provide the date of reported symptoms, at least one day prior to today.
5.  Click **Save**.

    Related lists appear that are filled in after you run a diagnostics report.

6.  Click **Run Diagnostics**.

    A scheduled job fetches potentially impacted user data from the selected sources and loads the data in corresponding related lists. Refresh a list to see the potentially impacted users immediately.

    If you selected the **Handheld/Wearables** option, a diagnostic request task is created. Follow the instructions in the task to fetch the potentially exposed users.

    If you selected the **Wi-Fi access log** option, the Wi-Fi data queried is based on the location preference set for the affected user's location. The available options are:

    -   Mist Systems integration: The Wi-Fi data is fetched from Mist Systems when you run the diagnostic request.

        If the site network is Bluetooth LE-enabled and the organization has provided users with a BLE device, the Wi-Fi access using the BLE devices is used to identify potentially exposed users.

    -   Cisco DNA Spaces integration: The Wi-Fi data is available based on the Cisco tier value set in the **sn\_imt\_tracing.wifi\_log\_cisco\_tier** property:
        -   If the **wifi\_log\_report** value is set, the data is imported from the Wi-Fi access data files for the specified days from the SFTP server and queried by the location path to identify potentially exposed users.
        -   If the **proximity\_report** value is set, a diagnostic request task is created to fetch the potentially exposed users. Follow the instructions in the task to fetch data on potentially impacted users from the selected data source. For more information, see [Fetch potentially exposed user data from a data source](work-on-diagnostic-req-task.md#).
    -   Manual import: The Wi-Fi data is imported from a Microsoft Excel spreadsheet into the Wi-Fi Access Register table.
7.  Add manually the potentially affected users, for example, users who visited a location with an affected user.

    1.  In the Impacted users added manually list, click **New**.

    2.  Select the potentially affected user.

    3.  Add comments about why you added the user.

        Entering comments helps identify other users who might be potentially impacted by this user if this user starts to show symptoms.

    4.  Click **Submit**.

    The user appears in the Impacted users added manually related list.


## Result

The related lists display potentially impacted users. The Impacted visitors, Impacted customers, and Impacted field agents related lists appear only if relevant users exist.

**Note:** Users who have not consented to use their data are filtered out from the list of potentially impacted users. However, you can add them to the potentially impacted users list manually.

<table id="table_l4l_rrb_hmb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All Impacted users

</td><td>

All users who might have been potentially exposed. This list is a combination of all the records in the other related lists.Under the **Tracing system** column, you can see the source of the exposure for an user.

</td></tr><tr><td>

Impacted users added manually

</td><td>

This list is empty unless a user with the sn\_imt\_diagnosis.diagnostics\_admin role manually adds additional potentially impacted users.

</td></tr><tr><td>

Impacted visitors

</td><td>

Visitors invited by the affected user who cleared the health screening and interacted with the affected user during the specified time period.

</td></tr><tr><td>

Impacted customers

</td><td>

Customers added from the field service work order analysis. Potentially impacted customers are determined by the work orders attended by an affected field agent between the specified dates.

</td></tr><tr><td>

Impacted field agents

</td><td>

Field agents added from the field service work order analysis. Potentially impacted field agents are determined if they interacted with an affected agent or visited the same customer as the affected agent between the specified dates.

</td></tr></tbody>
</table>If the diagnostics fail to run, click the **Show related jobs** link to check the status of all jobs that have been launched. You can view the details, including the log message, to determine the reason of failure.

**Note:** Failed jobs are automatically retried three times, the default setting in the Emergency Exposure Management properties. To retry the job after you fix the issue, click **Reprocess**.

## What to do next

Depending on the applications and plugins installed, you can take the following actions:

-   Click **Download Report** to download a spreadsheet listing all affected users. The report includes the email address and location of each user, and the source of identification, such as location, workplace reservation, collaboration, badge reader data, or field service work orders. For manually added users, the comment is included.
-   Click **Download Visitor Report** to download a spreadsheet listing all potentially exposed visitors who met the affected user. The report includes the email address and name of each visitor.

    **Note:**

    The button is available only when you have selected the **Visitor log** tracing system.

-   The case manager can create a case for the affected user and add potentially impacted users from the related list to the case to follow up on their health status. For more information, see [Create a case for an affected employee](../../contact-tracing/task/create-exposure-case.md).
-   The manager of the affected field agents can take further actions such as blocking their future work order assignments. For more information, see [Emergency Exposure Management for field service agents](https://www.servicenow.com/docs/access?context=monitoring-analytics-fsm&version=yokohama&pubname=yokohama-field-service-management&section=exposure-management-for-agents&ft:locale=en-US) .


-   **[Fetch potentially exposed user data from a data source](work-on-diagnostic-req-task.md#)**  
Work on the diagnostic request task to get information about potentially impacted users from a selected data source and populate the corresponding related lists on the Diagnostic Request form.

**Parent Topic:**[Emergency Exposure Management](../concept/emergency-exposure-management.md)

