---
title: Configuring EMR Help
description: Set up the EMR Help application to address different types of clinician issues submitted from an EMR system.
locale: en-US
release: yokohama
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configuring EMR Help

Set up the EMR Help application to address different types of clinician issues submitted from an EMR system.

## Configuration overview

Configuring EMR Help involves installing the application, then setting up user access and data.

Hospital staff using the EMR system often encounter various challenges. In the event of an issue, they can initiate a service request directly from within the EMR system. Once a service request is created, the system automatically generates an incident in their ServiceNow instance.

![EMR Help configuration.](../image/emr-help-config.png)

Simultaneously, relevant EMR variables, such as workstation ID, patient details, clinician information, and the specific screen involved, are fetched from the EMR system and stored in a dedicated table within the EMR Help application. This additional information enhances the service request, providing fulfillers with crucial details for effective troubleshooting.

-   [Install EMR Help](../task/install-emr-help.md).

    Install the EMR Help application to integrate your ServiceNow instance with an EMR system.

-   [Configure the data table for a request type](emr-config-example.md).

    Review the data table associated with an IT request, such as the EMR Incident Data \[sn\_ind\_rmt\_help\_incident\_data\] table. Then, make sure that the table has columns to store each system variable that you're planning to fetch from an EMR system. Add new columns corresponding to the system variables that don't exist in the table.

    If a data table for an IT request doesn't exist, create another data table by extending the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table.

    For more information, see [EMR Help data model](emr-data-model.md).

-   [Configure request parameters for EMR systems](../task/configure-emr-help-req-parm.md).

    Configure the remote request parameters for an EMR system.

-   [Configure request definitions for EMR systems](../task/configure-emr-help-req-def.md).

    Create or modify request definitions to support IT service requests from an EMR system. In addition, map the remote request parameters with the columns of the request data table associated with your task.

-   [Assign roles for EMR Help users](../task/assign-emr-help-roles.md).

    Assign roles to control access to features, capabilities, and data in the EMR Help application.

-   [Configure healthcare case types for EMR Help](../task/configure-hcls-case-types-for-emr-help.md).

    Configure healthcare case types for EMR Help in to fulfill service requests made from the EMR Help portal.

    The base healthcare case type \[sn\_hcls\_case\] is an abstract case type that provides a foundation to extend from when building your own healthcare case types.

-   [Configure digest token authentication for EMR Help](configure-digest-token-authentication-for-emr-help.md).

    Configure ServiceNow single sign-on with Epic utilizing digest token authentication.

-   [Configure iFrame support for EMR Help in ServiceNow](configure-iframe-support.md)

    Configure EMR Help to launch within a frame in Epic Hyperspace and Hyperdrive.

-   [Configure the EMR session info contextual sidebar](configure-the-emr-session-info-contextual-sidebar.md).

    Configure the EMR session info contextual sidebar in Workspace to manage the fields that display there.

-   [Configuring the EMR Help service portal](config-emr-help-sp.md).

    As an administrator, you can set up the EMR Help service portal for submitting IT service requests from an EMR system.

-   [Set up the IT service request fulfillment process](emr-help-remote-req-fulfillment.md#)

    Manage IT service requests submitted from your EMR system by using either a dedicated service portal or a system support module.

-   \(Optional\) [Implement encryption in EMR Help](emr-help-encryption-support.md).

    Encrypt fields, attachments, or both to secure your EMR system data.

-   \(Optional\) [Customize the URL and REST API task parameters for EMR systems](../task/emr-help-custom.md).

    Use scripted extension points to manipulate URL parameters and REST API task parameters for an EMR system.


## Additional configuration information

-   To configure digest token authentication for EMR Help, see the [How to Configure Digest Token Authentication for EMR Help with Epic Hyperspace \[KB1002504\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1002504) article in the Now Support knowledge base.
-   To configure EMR Help to launch within an iframe in Epic Hyperspace and Hyperdrive, see the [How to configure EMR Help to launch within an iFrame in Epic Hyperspace and Hyperdrive \[KB1207128\]](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=54128a784745f590b8a4aa25126d437c) article in the Now Support knowledge base.


