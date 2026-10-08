---
title: Set up the environment and instance for ServiceNow Quote Experience
description: Provision and configure the ServiceNow instance and the CPQ microservice instance, set up authentication between them, and configure the users and settings that ServiceNow Quote Experience requires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-exp-env-instance-setup-task.html
release: brazil
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 2
breadcrumb: [Without guided setup, Set up CPQ, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up the environment and instance for ServiceNow Quote Experience

Provision and configure the ServiceNow instance and the CPQ microservice instance, set up authentication between them, and configure the users and settings that ServiceNow Quote Experience requires.

## Before you begin

Role required: admin

**Important:** Complete all steps in this section before you create a quote.

## Procedure

1.  Provision a ServiceNow instance, then install and configure the required applications.

    For the list of required applications, see the [ServiceNow Store listing](https://store.servicenow.com/store/app/aa2ef860c3428f10ef46d0af050131a4).

    **Note:** Do not install the Quote Management application. ServiceNow Quote Experience and Quote Management cannot run concurrently on the same instance. If Quote Management is already installed, complete the next step.

    Install and configure the following applications only if you use the corresponding capability:

    |Application name|Application ID|
    |----------------|--------------|
    |Opportunity Management Data Model|`sn_opty_mgmt_core`|
    |Opportunity Management Application|`sn_opty_mgmt`|
    |Advanced Approval Management|`sn_adv_appr_mgmt`|

2.  If the Quote Management application is installed, run the fix script that disables its objects.

    For more information, see [Disable Quote Management application objects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/disable-quote-management-fix-script.md).

3.  Provision a CPQ microservice instance.

    For more information, see [Request a CPQ tenant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/set-up-logik-instance.md).

    Then configure the tenant settings that ServiceNow Quote Experience requires. For more information, see [ServiceNow Quote Experience tenant settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-exp-tenant-settings.md).

4.  Integrate the ServiceNow and CPQ microservice instances.

    For more information, see [Setting up CPQ Configurator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/setup-cpq-integrator.md).

5.  Set up system-to-system authentication \(JWT and OAuth\) and add it to the connection.

    For more information, see [Set up JWT and OAuth authentication for ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-exp-jwt-oauth-connection.md).

6.  Set up the administrator user.

    ServiceNow users with the platform admin role cannot access quote records within the CSM/FSM workspace. Before accessing a quote, impersonate a user who has the required quote-access permissions but not the platform admin role. For the required permissions, see the access-control documentation.

7.  Set up the integration user.

    An integration user is created and assigned a set of roles during the CPQ integration setup \(see [Set up instance for CPQ integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/cpq-integration-create-certificates.md)\). Manually add the following additional roles:

    -   `sn_l2c_core.viewer`
    -   `sn_csm_pricing.pricing_integrator`
    -   `sn_adv_appr_mgmt.approval_request_writer`
    -   `sn_adv_appr_mgmt.approval_request_viewer`
8.  Configure the transaction blueprint.

    For general transaction blueprint guidance and ServiceNow capability configuration, see [Quote Experience documentation](https://www.servicenow.com/docs/r/order-management/quoting-experiences-overview.html).

9.  Ensure that web embeddables are enabled by setting the **glide.uxf.lib.embeddables.enabled** system property to `true`.


