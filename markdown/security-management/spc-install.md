---
title: Install the supported applications for Security Posture Control
description: The applications required for this integration are available on the ServiceNow Store. Some applications have dependencies that you must download and install separately.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-01-28"
reading_time_minutes: 5
breadcrumb: [Explore, Security Posture Control, Security Operations]
---

# Install the supported applications for Security Posture Control

The applications required for this integration are available on the ServiceNow Store. Some applications have dependencies that you must download and install separately.

## Before you begin

Role required: admin for download, installation, and activation of all applications.

## Procedure

1.  Download the required applications from the ServiceNow Store into your ServiceNow instance.

    The Security Posture Control \(SPC Core\) application provides the core framework and is required for Asset Security Posture Management \(ASPM\). The Configuration Compliance application and its dependencies permit you to create remediation tasks for the security control gaps you find using Asset Security Posture Management.

    |Application|App ID|
    |-----------|------|
    |Asset Security Posture Management|\(Plugin id: sn\_sec\_caasm\)|
    |ITOM Discovery License|\(Plugin id: com.snc.itom.discovery.license\)|
    |Security Posture Control Core|\(Plugin id: sn\_sec\_spc\_core\)|
    |Mitigation Controls Monitoring|\(Plugin id: sn\_sec\_mit\_ctr\)|
    |Configuration Compliance \(includes child app secops\_shared\_components\) |\(Plugin id: sn\_vulc\)|
    |Vulnerability Response Licensing and Usage|\(Plugin id: sn\_vul\_licensing\)|

    |Application|App ID|
    |-----------|------|
    |Discovery Plugin|\(Plugin id: com.snc.discovery\)|
    |Cloud Configuration Governance|\(Plugin id: sn\_itom\_ccg\)|
    |CCG Content Pack|\(Plugin id: sn\_itom\_ccg\_cp\)|
    |CMDB CI Class Models|\(Plugin id: sn\_cmdb\_ci\_class\)|
    |Cloud Action Library|\(Plugin id: com.sn.itom.cal\)|

    |Application|Application ID and version|
    |-----------|--------------------------|
    |Security Posture Control API Connectors|sn\_spc\_cxf v1.0.3|
    |Security Posture Control|sn\_sec\_spc\_core v6.3.2|
    |Asset Security Posture Management|sn\_sec\_caasm v5.4.1|
    |Mitigation Controls Monitoring|sn\_sec\_mit\_ctrl v4.1.0|

    |Plugin|Plugin ID|
    |------|---------|
    |ServiceNow IntergationHub Action Template - Data Stream|com.glide.hub.action\_type.datastream|

    See [Creating your own API connectors in Security Posture Control](../concept/spc-creating-sgc-template.md) for more information.

    For more information about downloading and activating applications, see the following topics:

    -   [Download an application from the ServiceNow Store for the first time](../../security-incident-response/reference/download-app-first-time.md).
    -   [Activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).
2.  After you have downloaded the applications, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

3.  Locate the applications that you downloaded and select **Install** to activate them along with their dependencies.

    Any dependency applications that are also installed automatically along with an application are displayed in the Application installation dialog. However, if you are prompted to install dependency plugins during the installation, follow the prompts provided. Verify you have all the applications and dependencies listed in the previous table installed and activated.

    A dialog is displayed after an application is successfully activated.

    For more information about downloading and installing applications from the ServiceNow Store:

    -   To Opt in to ServiceNow products, follow the steps in [Opt in to the ServiceNow Store products](https://www.servicenow.com/docs/access?context=optin-optout-prod&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
    -   To install an application that you have purchased from the ServiceNow Store, follow the steps in [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
    -   Alternatively, if you want to manage your entitlement for the applications on other ServiceNow AI Platform instances, follow the steps in [Manage entitlements from your ServiceNow instance](https://www.servicenow.com/docs/access?context=entite-app&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
4.  After you have installed and activated the applications, assign users to the following Security Posture Control groups:

    These groups inherit all the roles necessary to read and edit SPC records.

    -   **SPC Admin Group**

        Users in this group have full read and write access to all the records for the product, including licensing information. Granular roles for this group include: \[sn\_sec\_caasm.analyst, sn\_sec\_caasm.caasm\_security\_admin, and sn\_sec\_spc\_core.configure\].

    -   **SPC Analyst Group**

        Users in this group have full read and write access to all the records for the product but cannot view licensing information. Granular roles for this group include \[pa\_power\_user and sn\_sec\_spc\_core.analyst\].

    -   **SPC Analyst Read Only Group**

        Users in this group have full read access to all the records for the product but cannot view licensing information. Granular roles for this group include \[pa\_power\_user, sn\_sec\_spc\_core.analyst\_read, sn\_sec\_caasm.read, and cmdb\_ms\_user\].

    -   **Supporting application roles**

        The following roles are required by the applications listed in the preceding table that support SPC and Asset Security Posture Management.

        -   Configuration Compliance Admin \[sn\_vulc.admin\] - Configures the Configuration Compliance application, has visibility to all records, and can modify properties. Assigns roles in the Configuration Compliance application.
        -   Vulnerability Response Admin \[sn\_vulc.admin\] - Configures the Vulnerability Response application and the vulnerability risk calculators.
        -   MID Server \[mid\_server\] - Configures a MID Server.
5.  Set the glide.identification\_engine.multisource\_enabled system property to **true**.

    Security Posture Control relies on data from service graph connectors that is populated in the CMDB 360 Data \[cmdb\_multisource\_data\] table. This data is populated only when the glide.identification\_engine.multisource\_enabled system property is set to true. You must have the cmdb\_ms\_admin role to modify property values. To set the property, navigate to **All** &gt; **Configuration** &gt; **CMDB 360 Properties**.

6.  Set the **ignoreCIClass** \[sn\_sec\_cmn.ignoreCIClass\] system property to ignore some configuration item \(CI\) classes when running CI Lookup Rules.

    As an SPC Admin and SPC Analyst, you might need to ignore certain hardware or virtual classes so that you do not ingest information about assets you do not want to control. See [Create a Vulnerability Response CI lookup rule](../../security-operations-common/task/create-ci-identifier-rules.md) and [Ignore CI classes](../../security-operations-common/task/ignore-CI-classes.md) for more information.

7.  Modify reconcilation and recompute CMDB data sources to set the source of truth for attribute values.

    The CMDB 360 dashboard provides aggregations and analysis of CMDB 360 data. CMDB 360 collects data about all the discovery sources reporting attribute values for CIs. Use the CMDB 360 view in Configuration Management Database \(CMDB\) Workspace to track activities and identify potential issues of discovery sources. See [CMDB 360 view in CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace-cmdb360-view&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.


