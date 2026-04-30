---
title: Agent Client Collector release notes
description: The ServiceNow Agent Client Collector application enables you to monitor the service availability, performance, and infrastructure of your system. Agent Client Collector was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Agent Client Collector release notes

The ServiceNow® Agent Client Collector application enables you to monitor the service availability, performance, and infrastructure of your system. Agent Client Collector was enhanced and updated in the Yokohama release.

## Agent Client Collector highlights for the Yokohama release

-   Agent Client Collector for Visibility: Starting in version 1.1.0, ACC for Visibility has been renamed Agent Client Collector for Visibility - Content. CNO for Visibility has been extracted from Agent Client Collector for Visibility - Content and is now a separate application.
-   Store instance credentials in the Google Cloud Secret Manager when the Kubernetes Visibility Agent Informer uses Google Kubernetes Engine \(GKE\).
-   Use a custom CA to enable Kubernetes Visibility Agent Informer to communicate with the instance when using a custom root Certificate Authority \(CA\).
-   Configure Agent Client Collector without a MID Server by ßusing MID-less configuration.

See [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

**Important:** Agent Client Collector is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Scan your resource directories for file attributes](https://www.servicenow.com/docs/access?context=directory-scan-checks-policies&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 3.13.0, run a check to receive information on the directory file's integrity, size, space, response time, and age.

-   **[Conserve MID Server resources by using MID-less installation for Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-itom-cloud-services&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 3.6.5, conserve MID Server resources for more persistent features by using the MID-less installation when installing Agent Client Collector. With this installation, you don't need a MID Server in your system architecture.

-   **[Create tasks to address Agent Client Collector errors](https://www.servicenow.com/docs/access?context=create-error-task&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 4.3.0, create tasks to resolve errors relating to the Agent Client Collector. Tasks are assigned to personnel who investigate the underlying issues and work to resolve the errors.

-   **[Use a proxy server with MID-less installation](https://www.servicenow.com/docs/access?context=acc-yml-options&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 4.3.0, enable using a proxy server when installing Agent Client Collector without a MID Server.

-   **Discovery MSSQL server components**

    Starting in version 1.3.0, enable discovery of MSSQL components by running Discovery as a local system user.

-   **Java certification Discovery through file-based discovery**

    Starting in version 1.3.0, discover java file information using Agent Client Collector for Visibility - Content \(ACC-VC\) file based discovery. File based discovery locates java files that are installed on the system but not running, enabling retrieval of data used for licensing and auditing.

-   **[Enable high volume upgrade of agents](https://www.servicenow.com/docs/access?context=acc-high-volume-upgrade&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 4.3.0, enhance efficiency by performing high-volume upgrade of large numbers of Agent Client Collector installations at once.

-   **[Block event creation for non-existent entities](https://www.servicenow.com/docs/access?context=prevent-events-nonexistent-entities&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 3.13.0, block the creation of events and alerts if the process monitoring and log files don't exist in their indicated location.

-   **[Control how check results are sent](https://www.servicenow.com/docs/access?context=create-edit-policies&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 3.6.5, configure the circumstances when check results are sent.

-   **[Configure and receive notifications of agent key expiration](https://www.servicenow.com/docs/access?context=agent-registration-key-configuration&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 3.6.5, receive notifications that indicate when an agent registration key is expiring.

-   **[Monitor network host availability](https://www.servicenow.com/docs/access?context=network-host-availability-check&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 4.1.0, use a new check to verify network host availability.

-   **[Identify software running on Linux and Windows devices](https://www.servicenow.com/docs/access?context=acc-visibility-checks-policies&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 4.1.0, identify the software that is running on your Linux and Windows servers and devices by using file-based Discovery. File-based Discovery enables you to maintain the records of your software licenses and helps you to evaluate any threats from unwanted files.

-   **[Store ServiceNow instance credentials in the Google Cloud Secret Manager when the Informer uses Google Kubernetes Engine \(GKE\)](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    If your organization uses Google Kubernetes Engine \(GKE\) you can store the secret in Google Cloud Secret Manager. The Kubernetes Visibility Agent Informer can then pull the ServiceNow credentials for accessing your instance from the Google Cloud Secret Manager.

-   **[Use a custom CA to enable the Informer to communicate with the ServiceNow instance when using a custom root CA](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Mount a custom certificate authority into the Kubernetes Visibility Agent Informer pod to enable the Informer to communicate with the instance when a custom root CA is used.


## Changed in this release

-   **[Explore metrics with Metric Explorer independent of Agent Client Collector Monitoring](https://www.servicenow.com/docs/access?context=agent-workspace-ops-intelligence&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 4.1.0, view and monitor metric data with Metric Explorer, even if you have not installed Agent Client Collector Monitoring.

-   ****

    Starting in version 1.1.0, ACC for Visibility has been renamed as Kubernetes Visibility Agent and consists only of what is currently CNO for Visibility. The term CNO for Visibility has been deprecated and replaced with Kubernetes Visibility Agent. All other ACC for Visibility functions are now part of Agent Client Collector for Visibility - Content.


## Activation information

Agent Client Collector is available with activation of the Agent Client Collector Framework plugin \(sn\_agent\) and the Agent Client Collector Monitoring plugin \(sn\_itmon\) in an instance on which Event Management is installed.

