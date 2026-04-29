---
title: Package and package version in RPA Hub
description: A package is a container that groups together one or more automation logic and their related files, configurations, and dependencies. A package version is a specific release of a package.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, RPA Hub, Workflow Data Fabric]
---

# Package and package version in RPA Hub

A package is a container that groups together one or more automation logic and their related files, configurations, and dependencies. A package version is a specific release of a package.

A package refers to a set of workflows, scripts, configurations, and dependencies that are designed to automate specific tasks or processes. These packages can be published or imported onto the RPA platforms to quickly deploy automation solutions.

Packages are used to encapsulate functionalities, libraries, or applications, making it simpler for developers or RPA administrators to deploy software components.

You can create a package in two ways. Follow this procedure to create a package from RPA Hub.

To create a package from RPA Desktop Design Studio while you're publishing an automation file, follow the steps as mentioned in [Publish an automation project in RPA Desktop Design Studio](../../rpa-studio/task/publish-automation-project.md).

After a package is created, the RPA developer publishes an automation from RPA Desktop Design Studio. This process results in a new package version.

-   **[Life-cycle stage statuses \(LLCS\) of a package in RPA Hub](../reference/lifecycle-stages-package.md)**  
The State transition of a package guides you through the stages of its life cycle.
-   **[Create a package to assign to a bot process](../task/create-package.md#)**  
Create an unattended or attended package in RPA Hub to assign it to a bot process to execute an automation.
-   **[Edit a package in RPA Hub](../task/edit-package.md)**  
Edit an existing package in RPA Hub to modify the details such as the name or description.
-   **[Retire a package in RPA Hub](../task/retire-package.md)**  
Retire a package to turn it off. It is one of the life-cycle stages of a package. After you retire a package, it cannot be used further.
-   **[Download a package version in RPA Hub](../task/download-package-version.md)**  
Download a package version in RPA Hub so that it can be opened from the RPA Desktop Design Studio to build, debug, or modify the automation.
-   **[Override a skill package version for multiple bot processes in RPA Hub](../task/override-skill-version-multi-bot-process.md)**  
Override a skill package version in RPA Hub for multiple bot processes that are associated with the same attended or unattended package. You can select the latest version of the skill package without publishing the attended or unattended package again from RPA Desktop Design Studio.
-   **[Verify the HashCode of a package version in RPA Hub](../task/view-hash-code.md)**  
Verify the HashCode of a package version in RPA Hub so that you can validate the HashCode of the manually uploaded automation zip file with the associated package version record.
-   **[Retire a package version in RPA Hub](../task/retire-package-version.md)**  
Retire a package version in RPA Hub so that the version can't be used again. After a package version is retired, it can’t be used again.

**Parent Topic:**[Using RPA Hub](managing-rpa-hub.md)

