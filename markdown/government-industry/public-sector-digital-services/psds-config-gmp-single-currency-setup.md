---
title: Configure a currency in Grants Management
description: Grants Management currently only supports single-currency mode.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-gmp-single-currency-setup.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Foundation, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure a currency in Grants Management

Grants Management currently only supports single-currency mode.

## About this task

Without this configuration, if a grant applicant uses a different currency from the program it applies to, and it will result in incorrect currency calculation like budget calculation.

## Before you begin

Role required: admin

**Note:** This may have configuration implications across all ServiceNow applications in your instance. Verify the RCA settings of other applications after completing this procedure.

## Procedure

1.  Navigate to **All**, and in the navigation filter, enter `sys_properties.list`.

2.  Under the Name column, search for the `glide.i18n.single_currency` record, and select the record to open it.

3.  Set the value to **true**.

4.  Navigate to **All**, and in the navigation filter, enter `sys_properties.list`.

5.  Under the Name column, search for **glide.i18n.single\_currency.code**, and select the property record to open it.

6.  In the Value field, enter the three-letter ISO currency code for the target currency.

    For example, to set the currency to USD, enter `USD`.

7.  Navigate to **All**, and in the navigation filter, enter `sys_properties.list`.

8.  Search for `glide.system.locale`, and open the property record.

9.  Set the value the desired locale for the currency.

    The value is in the format `Language.Country`, where the Language is an ISO 639 language code, and Country is an ISO 3166 language code. To set the locale to the US, enter `en.US`.

10. Navigate to **All** &gt; **System Localization** &gt; **Currencies**.

11. Open the record of each currency that you wish to deselect, and unselect the checkbox for **Active**.


**Parent Topic:**[Configure Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gmp-foundation.md)

**Previous topic:**[Configure a retention policy for grant cases in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gmp-setup-retention-policy.md)

**Next topic:**[Configure export application functionality in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gmp-export-pdf.md)

