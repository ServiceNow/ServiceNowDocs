---
title: Standard currency fields
description: The standard, or default, currency fields are installed with the base system and used in most non-financial applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/currency-administration/configure-and-use-default-currency-fields.html
release: australia
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Standard currency fields

The standard, or default, currency fields are installed with the base system and used in most non-financial applications.

A standard currency field stores a currency value, a currency code, and a reference currency value.

-   Three-letter ISO code that identifies the currency that you select for the currency amount. For example, USD for the US Dollar, or EUR for the Euro.
-   The reference currency value is the currency value, expressed in the reference currency. When you save a currency value, the reference currency value is calculated using a rate conversion.

A price field is similar to a currency field, but with special features for conversion and display. To learn more, see [Price fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/currency-administration/price-fields.md).

-   **[Locale settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/currency-administration/locales.md)**  
There are two locale settings, system and user. The system locale determines the reference currency, and the user locale determines the session currency.
-   **[Session and reference currency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/currency-administration/session-and-reference-currency.md)**  
The default, or standard, currency fields in the ServiceNow AI Platform® use two kinds of currency, Session and Reference.
-   **[Single-currency mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/currency-administration/single-currency-mode.md)**  
Single-currency mode enables all users of the platform to view currency values in the same currency.
-   **[Price fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/currency-administration/price-fields.md)**  
A price field is a currency field that enables control over conversions and display.
-   **[Default currency values in forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/currency-administration/currency-values-forms.md)**  
In forms, currency values appear in the currency in which they were entered.
-   **[Default currency values in reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/currency-administration/currency-values-reports.md)**  
Currency values in reports appear in the user’s session currency, and are formatted in the user’s locale with a currency symbol.
-   **[Default currency values in lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/currency-administration/currency-values-lists.md)**  
In lists, default currency values appear in the user’s session currency, formatted for display in the user’s locale. Typically, a formatted number follows the currency symbol.
-   **[Default currency values in import and export](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/currency-administration/currency-import-export.md)**  
In general, currency values crossing the boundaries of the platform are represented in the user’s session currency and formatted in the user’s locale.
-   **[Default currency values in scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/currency-administration/currency-values-scripts.md)**  
You can use currency fields in scripts.

**Parent Topic:**[Exploring currency administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/currency-administration/explore-currency-admin.md)

**Related topics**  


[FX Currency fields]()

