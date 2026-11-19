---
title: Retire a package version in RPA Hub
description: Retire a package version in RPA Hub so that the version can't be used again. After a package version is retired, it can’t be used again.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/retire-package-version.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Retire a package version in RPA Hub

Retire a package version in RPA Hub so that the version can't be used again. After a package version is retired, it can’t be used again.

## Before you begin

Create a package. For more information, see [Create a package to assign to a bot process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/create-package.md).

Verify that the package and associated package versions aren’t assigned to any non-retired bot process.

For a skill package version, verify that the version is not associated to any attended or unattended package versions or a bot process.

Role required: sn\_rpa\_fdn.rpa\_developer or sn\_rpa\_fdn.rpa\_admin

## About this task

You can retire a package in two ways:

-   Retire a package and all the associated package versions are also retired automatically. For more information about retiring a package, see [Retire a package in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/retire-package.md).
-   Retire only the package version, by following the steps mentioned in this task.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(\[Omitted image "rpahublist-icon.png"\] Alt text: List icon.\).

3.  On the **Lists** tab, under **Build**, select **Packages**.

4.  Open the package to retire the related package version.

5.  In the form header, select **Retire**.

6.  When you see the confirmation prompt, select **Retire**.


**Parent Topic:**[Managing RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/managing-rpa-hub.md)

