---
title: RCA approvals for Manager Hub
description: After you install Manager Hub, you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Manager Hub, HR Service Delivery, Employee Service Management]
---

# RCA approvals for Manager Hub

After you install Manager Hub, you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request.

## Before you begin

-   Role required: admin
-   The RCAs that are generated after the installation are in the **Requested** state and you must manually mark the RCAs as **Allowed**, which can be time-consuming.

    To automate the RCA approvals for any record, you can run the **MH bulk RCAs approval** script where the source scope is Manager Hub. Download the MH bulk RCAs approval file from the **Supporting Links and Docs** section in [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/d20a85536b30011024ca2421ee44affa/2.0.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3Dmanager%2520hub&sl=sh). This file is a standalone script to reduce the manual effort involved. After you download the script file, perform the following steps:


## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Right-click the header and choose **Import XML**.

3.  Click **Choose file** and select the XML file that you downloaded.

4.  Search and find the **MH bulk RCAs approval** script record.

5.  Click **Run Script** to allow all the requested RCAs.

    **Note:** The fix script can approve the RCAs that exist at the time of execution. After running the RCA script, if you install new plugins, such as Human Resources Scoped App \[com.sn\_hr\_core\], Human Resources: Integrations \[sb\_hr\_integration\], Journey Accelerator \[sn\_ja\], Journey Designer \[sn\_jny\], and Document Template \[sn\_doc\], rerun the RCA script to approve the new RCAs.


**Parent Topic:**[Configure Manager Hub](set-up-managerhub.md)

**Related topics**  


[Activate a scheduled job](../reference/activate-sj-mh.md)

[Configure important dates](configure-imp-dates.md)

[Configure team requests](configure-team-requests.md)

[Configure team data](configure-team-data.md)

[Configure team column data](configure-team-columndata.md)

[Configure team filters](configure-team-filter.md)

[Set up View as Direct Reports](../../employee-center/task/view-direct-reportee.md)

[Configure daily stats](configure-daily-stats.md)

[Configure to do mappings](use-to-do-map.md)

[Configure widgets](configure-team-insights.md)

