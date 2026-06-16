---
title: Microsoft Azure Automation spoke release notes
description: Version history for the Integration Hub Azure Automation spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-azure-automation.html
release: store
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Azure Automation spoke release notes

Version history for the Integration Hub Azure Automation spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.0 - November 2024**
    -   New:
        -   Microsoft Azure Automation Spoke now makes use of the default alias for Microsoft Resource Management Spoke \(sn\_azure\_rm\_spoke.Microsoft\_Azure\_Resource\_Management\)
        -   New Actions with latest design pattern of complex object outputs, retry policy, connection &amp; credentials, and error evaluation making use of the new connection &amp; credential alias:
            -   Account Management:Create Account \(create\_account\_v2\), Delete Account \(delete\_account\), Look up Account \(look\_up\_account\), Look up Accounts Stream by Resource Group \(look\_up\_accounts\_stream\_by\_resource\_group\), Look up Accounts Stream by Subscription ID \(look\_up\_accounts\_stream\_by\_subscription\_id\), Update Account\(update\_account\_v2\)
            -   Job Management:Create Job \(create\_job\_v2\), Look up Job \(look\_up\_job\), Look up Job Output \(look\_up\_job\_output\), Look up Jobs Stream \(look\_up\_jobs\_stream\), Resume Job \(resume\_job\_v2\), Stop Job \(stop\_job\_v2\), Suspend Job \(suspend\_job\_v2\)
            -   Job Scheduled Management:Create Job Schedule \(create\_job\_schedule\_v2\),Delete Job Schedule \(delete\_job\_schedule\_v2\),Look up Job Schedule \(look\_up\_job\_schedule\),Look up Job Schedules Stream \(look\_up\_job\_schedules\_stream\)
            -   Runbook Management:Create Runbook \(create\_runbook\_v2\), Delete Runbook \(delete\_runbook\_v2\), Get Runbooks \(Metadata\) \(get\_runbooks\_metadata\), Look up Runbook \(look\_up\_runbook\), Look up Runbooks Stream \(look\_up\_runbooks\_stream\), Look up Runbook Content \(look\_up\_runbook\_content\), Update Runbook \(update\_runbook\_v2\)
            -   Schedule Management:Create Schedule \(create\_schedule\_v2\),Delete Schedule \(delete\_schedule\_v2\),Look up Schedule \(look\_up\_schedule\),Look up Schedules Stream \(look\_up\_schedules\_stream\),Update Schedule \(update\_schedule\_v2\)
            -   Software Update Configuration Management:Look up Software Update Configuration Run \(look\_up\_software\_update\_configuration\_run\),Look up Software Update Configuration Machine Runs Stream \(look\_up\_software\_update\_configuration\_machine\_runs\_stream\),Look up Software Update Configuration Runs Stream \(look\_up\_software\_update\_configuration\_runs\_stream\)
            -   State Configuration Management:Compile DSC Configuration \(compile\_dsc\_configuration\_v2\),Create DSC Configuration \(create\_dsc\_configuration\_v2\),Get DSC Configurations \(Metadata\) \(get\_dsc\_configurations\_metadata\),Look up DSC Configuration \(look\_up\_dsc\_configuration\),Look up DSC Configuration Content \(look\_up\_dsc\_configuration\_content\),Look up DSC Configurations Stream \(look\_up\_dsc\_configurations\_stream\),Look up Nodes Stream \(look\_up\_nodes\_stream\),Update DSC Configuration \(update\_dsc\_configuration\),Update Node DSC Configuration \(update\_node\_dsc\_configuration\_v2\)
            -   Watcher Management: Delete Watcher \(delete\_watcher\_v2\),Get Watchers \(Metadata\) \(get\_watchers\_metadata\),Look up Watchers Stream \(look\_up\_watchers\_stream\),Start Watcher \(start\_watcher\_v2\),Stop Watcher \(stop\_watcher\_v2\)
    -   Removed:
    -   -   Deprecate old credential alias for the spoke \(sn\_azure\_auto\_spke.Azure\_Automation\_Spoke\).
-   Deprecated Actions that make use of old credential alias:
    -   Account Management:Create Account \(Deprecated\) \(create\_account\), Delete Account \(Deprecated\) \(copy\_of\_delete\_profile\), Get Account \(Deprecated\) \(get\_account\), Look up Accounts By Resource Group \(Deprecated\) \(look\_up\_accounts\_by\_resource\_group\), Look up Accounts By Subscription \(Deprecated\) \(look\_up\_accounts\_by\_subscription\), Update Account \(Deprecated\) \(update\_account\)
    -   Job Management:Create Job \(Deprecated\) \(create\_job\), Get Job \(Deprecated\) \(get\_job\), Get Job Output \(Deprecated\) \(get\_job\_output\), Look up Job By Automation Account \(Deprecated\) \(look\_up\_software\_update\_configuration\_machine\_runs\), Resume Job \(Deprecated\) \(resume\_job\), Stop Job \(Deprecated\) \(stop\_job\), Suspend Job \(Deprecated\) \(suspend\_job\)
    -   Job Scheduled Management:Create Job Schedule \(Deprecated\) \(create\_job\_schedule\),Delete Job Schedule \(Deprecated\) \(delete\_job\_schedule\),Get Job Schedule \(Deprecated\) \(get\_job\_schedule\) ,Look up Job Schedules By Automation Account \(Deprecated\) \(look\_up\_job\_schedules\)
    -   Runbook Management: Create Runbook \(Deprecated\) \(create\_runbook\), Delete Runbook \(Deprecated\) \(delete\_runbook\), Get Runbook \(Deprecated\) \(get\_runbook\), Get Runbook Content \(Deprecated\) \(copy\_of\_get\_runbook\_content\), Look up Runbook By Automation Account \(Deprecated\) \(look\_up\_runbook\_by\_automation\_account\), Update Runbook \(Deprecated\) \(update\_runbook\)
    -   Schedule Management:Create Schedule \(Deprecated\) \(create\_schedule\),Delete Schedule \(Deprecated\) \(delete\_schedule\),Get Schedule \(Deprecated\) \(get\_schedule\),Look up Schedules By Automation Account \(Deprecated\) \(look\_up\_schedules\_by\_automation\_account\),Update Schedule \(Deprecated\) \(update\_schedule\)
    -   Software Update Configuration Management:Create Windows/Linux Update \(Deprecated\) \(create\_update\),Delete Windows/Linux Update \(Deprecated\) \(delete\_windowslinux\_update\),Get Software Update Configuration Runs By Id \(Deprecated\) \(get\_software\_update\_configuration\_runs\_by\_id\),Look up Windows/Linux Update \(Deprecated\) \(look\_up\_windowslinux\_update\),Look up Software Update Configuration Machine Runs \(Deprecated\) \(look\_up\_software\_update\_configuration\_runs\),Look up Software Update Configuration Runs \(Deprecated\) \(list\_job\_by\_automation\_account\)
    -   State Configuration Management:Compile DSC Configuration \(Deprecated\) \(compile\_dsc\_configuration\),Create DSC Configuration \(Deprecated\) \(create\_dsc\_configuration\),Get DSC Configuration \(Deprecated\) \(get\_dsc\_configuration\),Get DSC Configuration Content \(Deprecated\) \(get\_dsc\_configuration\_content\),Look up DSC Configuration \(Metadata\) \(Deprecated\) \(delete\_dsc\_configuration\),Look up Nodes By Automation Account \(Deprecated\) \(look\_up\_nodes\_by\_automation\_account\),Update DSC Configuration \(Deprecated\) \(update\_dsc\_configuration1\),Update Node DSC Configuration \(Deprecated\) \(update\_node\_dsc\_configuration\)
    -   Watcher Management:Delete Watcher \(Deprecated\) \(delete\_watcher\), Look up Watchers By Account Name \(Metadata\) \(Deprecated\) \(copy\_of\_look\_up\_watchers\_by\_account\_name\), Start Watcher \(Deprecated\) \(start\_watcher\), Stop Watcher \(Deprecated\) \(stop\_watcher\)
-   **Version 1.0.5 - December 2023**

    Fixed: Visibility of actions in the action picker.

-   **Version 1.0.4 - September 2023**

    Fixed: The license requirements.

-   **Version 1.0.3 - April 2023**
    -   Changed: Spoke name from "Azure Automation Spoke" to "Microsoft Azure Automation Spoke"
    -   Fixed: Improve installation performance of spoke
-   **Version 1.0.2 - August 2021**

    Patch release of the Azure Automation spoke for IntegrationHub. This version fixes null value in the payload using Create Job action.

-   **Version 1.0.1 - July 2021**

    Patch release of Azure Automation spoke for IntegrationHub. This version adds KMF modules for additional security of password2 fields and Rome compatibility.

-   **Version 1.0.0 - October 2020**

    Provides actions to automate the management of runbooks, jobs, software updates, and state configuration in Azure Automation.


