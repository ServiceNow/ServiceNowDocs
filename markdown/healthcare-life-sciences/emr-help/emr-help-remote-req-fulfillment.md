---
title: Setting up the ServiceNow IT service request fulfillment process for EMR systems
description: Manage ServiceNow IT service requests from your EMR system by using either a system support module or a dedicated service portal.
locale: en-US
release: australia
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Setting up the ServiceNow IT service request fulfillment process for EMR systems

Manage ServiceNow IT service requests from your EMR system by using either a system support module or a dedicated service portal.

## Using a system support module for your EMR system

Use the pre-built ServiceNow scripted REST APIs for submitting IT service requests within your EMR system. The Remote help request API is available for integrations with your EMR system. For more information, see Remote help request API.

## Using a dedicated service portal for your EMR system

Embed the service portal page for submitting ServiceNow IT service requests within your EMR system, such as the Epic EMR system.

**Note:** For integrating external web applications into an Epic EMR system, refer to the following sections in the Setup and Support guide available on the Epic website for its users:

-   Allow users to Launch the Web Application from a Toolbar Button
-   Configure the Integration Record for HTTP GET
-   Prepare Activity and Run Parameters for Your Workflow

To learn more, contact the Epic team representative of your institution.

As an administrator, you can use the EMR Help service portal for enabling clinicians to submit IT service requests. For more information, see [Configuring the EMR Help service portal](config-emr-help-sp.md).

To use a dedicated service portal, you can create a record producer to define the fields for the help form in the record producer and then embed the form in your service portal. Clinicians can use this help form to submit IT service requests.

By default, the **EMR Incident** record producer is available for submitting IT service requests associated with incidents. You can use the default record producer to add more variables or create your own record producer. For more information, see Record Producer.

When embedding the form in your service portal, note the following points:

-   Use the following URL format to embed the service portal page for submitting IT service requests: `https://<instance name>.service-now.com/emr-assist?id=emr_assist_home_page&sysparm_source=*source\_name*`.

    For *source\_name*, provide the parameter defined in the request parameter. For more information, see [Configure request parameters for EMR systems](../task/configure-emr-help-req-parm.md).

-   You can also append any EMR variables to the service portal page URL by using the following format: `https://<instance name>.service-now.com/emr-assist?id=emr_assist_home_page&sysparm_source=*source\_name*&*var1\_id=Value1*&*var2\_id=Value2*`.

    For example, `https://<instance name>.service-now.com/emr-assist?id=emr_assist_home_page&sysparm_source=epic&sysparm_ws=Workstation&sysparm_ws=En​vironment`.

    **Note:** EMR variables include workstation ID, server, patient medical record number \(MRN\), and others. You define the EMR variables as task parameters. The EMR variable values are automatically populated, if configured to be displayed on the EMR system help form. For more information, see [Configure request parameters for EMR systems](../task/configure-emr-help-req-parm.md).


