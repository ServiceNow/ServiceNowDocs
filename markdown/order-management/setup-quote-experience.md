---
title: Set up ServiceNow Quote Experience
description: Use the Quote Experience guided setup to connect your ServiceNow instance to your ServiceNow CPQ Microservice instance and set up system-to-system authentication with JWT and OAuth.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/setup-quote-experience.html
release: australia
topic_type: task
last_updated: "2026-10-27"
reading_time_minutes: 2
breadcrumb: [With guided setup, Setting up ServiceNow CPQ, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up ServiceNow Quote Experience

Use the Quote Experience guided setup to connect your ServiceNow instance to your ServiceNow CPQ Microservice instance and set up system-to-system authentication with JWT and OAuth.

## Before you begin

Role required: admin

## About this task

Complete the prerequisites before you start. For more information, see [Prerequisites for setting up ServiceNow CPQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/prereq-for-cpq-config.md).

**Note:** If Quote Management is installed, run the fix script in [Disable Quote Management application objects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/disable-quote-management-fix-script.md) before you start.

## How to access

In ServiceNow Workspace, go to **All** &gt; **Quote Experience** &gt; **Guided Setup**.

If Guided Setup isn't available, upgrade the ServiceNow Quote Experience application to the minimum version for your release. See the minimum app versions table below.

## Minimum app versions

|Release|Minimum ServiceNow Quote Experience version|
|-------|-------------------------------------------|
|Brazil|2.2.8|
|Australia|2.2.8|
|Zurich|1.2.8|

## Procedure

1.  Select through the **Prerequisites for CPQ** section.

    Verify you completed these items in the prerequisites. For more information, see [Prerequisites for setting up ServiceNow CPQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/prereq-for-cpq-config.md).

2.  Complete the **Certificate Setup** section.

    For detailed certificate generation information, see [Generate JWT certificates for ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/quote-exp-jwt-certificates.md).

    1.  For **Public Certificate**, copy and paste the contents of the `certificate.pem` file.

    2.  For **Private Key**, copy and paste the contents of the `private_key.pem` file.

        **Note:** For Public Certificate and Private Key, copy and paste the file contents starting with “-----BEGIN CERTIFICATE-----" and ending with “-----END CERTIFICATE-----". Both marker lines should be included.

    3.  Enter the keystore password, the password you chose when you created the certificate files, in the **Shared key** field.

        **Note:** If **Shared key** isn't editable, follow the prompt to edit the record in the Quote Experience application.

3.  Complete the guided setup.

4.  Add the Logik Integrator user as an OAuth application user for the Logik.ai API application registry.

    1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

    2.  Change the scope to **CPQ Integration**.

    3.  Add the **OAuth Application User** column to the table view.

    4.  Double-click the **OAuth Application User** cell on the **Logik.ai API** application registry record.

    5.  Select the **Logik Integrator** user.

5.  Add the **useraccount** auth scope to the Logik.ai JWT Bearer API application registry.

    1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

    2.  Change the scope to **Quote Experience**.

    3.  Open the **Logik.ai JWT Bearer API** application registry record.

    4.  In the **Auth Scope** section, double-click **Insert a new row...**.

    5.  Select **useraccount**.


