---
title: Configure Service Graph Connector for OpenTelemetry
description: Set up scheduled import jobs to pull in data from ServiceNow Cloud Observability \(formerly Lightstep\) into your Configuration Management Database \(CMDB\).
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-02-27"
reading_time_minutes: 9
breadcrumb: [OpenTelemetry, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for OpenTelemetry

Set up scheduled import jobs to pull in data from ServiceNow Cloud Observability \(formerly Lightstep\) into your Configuration Management Database \(CMDB\).

## Before you begin

**Important:** Starting with the Australia release, Service Graph Connector for OpenTelemetry is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models](../concept/cmdb-ci-class-models.md).
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   Observability Commons for CMDB \(sn\_observability\), which is only required for event ingestion. For Event Management to work, the Observability Commons for CMDB app must be installed prior to installing the connector. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

**Note:** If you have an earlier version of the Service Graph Connector for OpenTelemetry, then don’t migrate data from the old connector. You must uninstall the previous version and run the new integration.

Role required: admin

## Procedure

1.  Ensure that the application scope is set to Service Graph Connector for OpenTelemetry by using the application picker.

    For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

2.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **OpenTelemetry** &gt; **Setup**.

3.  On the Getting started page, select **Get Started**.

4.  Configure the application properties to set up your organization and authentication credentials for sending requests to the ServiceNow Cloud Observability APIs.

    1.  In the Configure the connection section of the Service Graph Connector for OpenTelemetry page, select **Get started**.

    2.  For the Use OpenTelemetry task, ensure that the Cloud Observability application meets the conditions as discussed in the [ServiceNow Cloud Observability setup \[KB1527588\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1527588) article in the Now Support Knowledge Base.

        **Important:** Note down your projects, organization, and API key details of the Cloud Observability application to be used later during the installation of the connector.

        After you have set up the OpenTelemetry environment in the Cloud Observability application, return to the guided setup and mark the Use OpenTelemetry task to complete by selecting **Mark as Complete**.

    3.  Enter your Cloud Observability organization details from where you want to retrieve the projects, resources, and dependency-mapping information.

        1.  For the Set up your organization task, select **Configure**.
        2.  In the **Value** field of the Service Graph Connection Properties form, enter the name of your Cloud Observability organization.
        3.  Select **Update**.
        4.  Mark the Set up your organization task to complete by selecting **Mark as Complete**.
    4.  Enter the API key details associated with the Cloud Observability application.

        1.  For the Set up the API key task, select **Configure**.
        2.  In the **API Key** field of the API Key Credentials form, enter the API key associated with the Cloud Observability application that you noted down in step [4.b](sgc-config-opentelemetry-integ.md#api-key).
        3.  Select **Update**.
        4.  Set the Set up the API key task to complete by selecting **Mark as Complete**.
    5.  Test the Cloud Observability API connection to import data from the Cloud Observability application.

        1.  For the Test the connection task, select **Configure**.
        2.  Select the **Test Connection** related link.
        3.  When the **Status** field is set to **Success**, select **X** to close the Test the connection dialog box and return to the guided setup page.

            If any of the tests have errors, follow the suggestions for remediation.

        4.  Set the Test the connection task to complete by selecting **Mark as Complete**.
    6.  Retrieve all the projects included in your Cloud Observability organization.

        1.  For the Get projects task, select **Configure**.
        2.  Select **Get Projects**.
        3.  When the Project properties related list is populated with all the projects included in the organization you specified in step [4.c.ii](sgc-config-opentelemetry-integ.md#org), select **X** to close the Get projects dialog box and return to the guided setup page.
        4.  Set the Get projects task to complete by selecting **Mark as Complete**.
5.  Configure additional configurations to set up lookback time, add excluded projects, run project diagnostics, and configure integration settings for service maps and stale configuration items \(CIs\).

    1.  In the Advanced settings section of the Service Graph Connector for OpenTelemetry page, select **Continue**.

    2.  Set up the lookback time from when you want to retrieve resources from the projects.

        Lookback time is used to calculate the start and end time for retrieving resources from a project of an organization and should match the scheduled job frequency setting. For example, if the lookback time is set to 12 hours, resources are retrieved from the start time calculated as the current time minus 12 hours and until the end time that is the current time.

        1.  For the Set up lookback time task, select **Configure**.
        2.  In the **Value** field of the Service Graph Connection Properties form, enter the lookback time in hours.
        3.  Select **Update**.
        4.  Set the Set up lookback time task to complete by selecting **Mark as Complete**.
    3.  Select the projects from which you don't want to retrieve resources.

        1.  For the Add excluded projects task, select **Configure**.
        2.  Select a project from the **Project** column.
        3.  Select the **Exclude project** check box.
        4.  Select **Update**.
        5.  Repeat steps from [5.c.ii](sgc-config-opentelemetry-integ.md#exclude-project) to [5.c.iv](sgc-config-opentelemetry-integ.md#exclude-project-update) for each project that you want to exclude.
        6.  Select **X** to close the Add excluded projects dialog box and return to the guided setup page.
        7.  Set the Add excluded projects task to complete by selecting **Mark as Complete**.
    4.  Run project diagnostics to test the Resource API response and ensure that the API contains the Kubernetes cluster name, Kubernetes namespace, and Kubernetes nodes.

        1.  For the Run project diagnostics task, select **Configure**.
        2.  Select a project from the **Project** column.
        3.  Select **Run diagnostics**.
        4.  When the **Diagnostics status** field set to **Success**, select **X** to close the Run project diagnostics dialog box and return to the guided setup page.

            If any of the Diagnostic tests have errors, follow the instructions in the **Diagnostics message** field to resolve the errors.

        5.  Repeat the steps [5.d.ii](sgc-config-opentelemetry-integ.md#project-diagnostics) to [5.d.iv](sgc-config-opentelemetry-integ.md#project-diagnostics-done) for each project that you want to run diagnostics.
        6.  Set the Run project diagnostics task to complete by selecting **Mark as Complete**.
    5.  Configure the system properties for service maps and stale CIs.

        1.  For the Configure system properties for the connector task, select **Configure**.
        2.  Verify the default values for the properties or fill in the values for a custom configuration.
        3.  Select **Save**.
        4.  Set the Configure system properties for the connector task to complete by selecting **Mark as Complete**.
6.  Configure the scheduled jobs to import complete or incremental data from the Cloud Observability application.

    1.  In the Configure the scheduled import jobs section of the Service Graph Connector for OpenTelemetry page, select **Continue**.

    2.  Activate the scheduled job for full data import.

        By default, the **OpenTelemetry Resources** scheduled job is available for full data import. However, you must activate the job.

        1.  For the Configure the scheduled job for full import task, select **Configure**.
        2.  On the Scheduled Data Import form for the **OpenTelemetry Resources** scheduled job, verify the field values for the scheduled job and select the **Active** check box.

            For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

        3.  Select **Update**.
        4.  Set the Configure the scheduled job for full import task to complete by selecting **Mark as Complete** in the guided setup.
    3.  Activate the scheduled job for delta data import.

        By default, the **OpenTelemetry Delta Resources** scheduled job is available for delta data import. However, you must activate the job.

        **Note:** The delta data pull doesn't occur in the following scenarios:

        -   The full data import is scheduled at the same time.
        -   The **Last Run Datetime** field of a data source is empty.
        -   The last delta data pull period is more than 3 days.
        1.  For the Configure the scheduled job for delta import task, select **Configure**.
        2.  On the Scheduled Data Import form for the **OpenTelemetry Delta Resources** scheduled job, verify the field values for the scheduled job and select the **Active** check box.

            For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

        3.  Select **Update**.
        4.  Set the Configure the scheduled job for delta import task to complete by selecting **Mark as Complete** in the guided setup.
    **Note:** When adding a new project to retrieve resources, be sure to perform a full import before running a delta import to avoid partial data and populate the CMDB accurately.

7.  Manage alerts and events by sending events from the Cloud Observability application to the ServiceNow Event Management application.

    You can manage alerts and events only when the Observability Commons for CMDB application is installed.

    **Note:** Enabling this feature requires a paid Cloud Observability license, but the feature is also available to free accounts for the purpose of evaluating the product in non-production environments. You can reach out to your ServiceNow account representative for more information.

    1.  In the Manage alerts and events section of the Service Graph Connector for OpenTelemetry page, select **Continue**.

    2.  Create a webhook destination for a project.

        1.  For the Create a webhook task, select **Configure**.
        2.  Select a project that is not excluded from the **Project** column.
        3.  Select **Create Webhook** to create a webhook destination in the Cloud Observability application.
        4.  After a success message appears, select **X** to close the Create a webhook dialog box and return to the guided setup page.

            When the webhook is created successfully:

            -   The system automatically creates a user record for each webhook destination in your ServiceNow instance.
            -   The user name of the user record starts with `ls_api_*&lt;project\_name&gt;*` and the user is assigned the evt\_mgmt\_integration role.
        5.  Repeat the steps [7.b.ii](sgc-config-opentelemetry-integ.md#webhook) to [7.b.iv](sgc-config-opentelemetry-integ.md#webhook-done) for each project for which you want to create a webhook.
        6.  Set the Create a webhook task to complete by selecting **Mark as Complete** in the guided setup.
    3.  Configure the system property for ingesting events that don’t have matching CIs in the CMDB.

        1.  For the Configure the property for unmatched CIs task, select **Configure**.
        2.  In the **Value** field, enter **true**.
        3.  Select **Update**.
        4.  Set the Configure the property for unmatched CIs task to complete by selecting **Mark as Complete** in the guided setup.

**Related topics**  


[Service Graph Connector for OpenTelemetry properties](../reference/sgc-cmdb-otel-props.md)

[Accessing the connection details of Service Graph Connector for OpenTelemetry](../concept/sgc-cmdb-otel-conn.md#)

[Linking inferred services with CIs](../concept/sgc-cmdb-opentelemetry-services.md#)

