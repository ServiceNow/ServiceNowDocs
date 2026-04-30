---
title: Set up optional inventor rewards in Legal Invention Disclosure
description: Set up optional rewards for inventors to be granted at three stages of applying for and acquiring a patent.
locale: en-US
release: yokohama
product: Legal Invention Disclosure
classification: legal-invention-disclosure
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Legal Invention Disclosure, Legal Invention Disclosure, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Set up optional inventor rewards in Legal Invention Disclosure

Set up optional rewards for inventors to be granted at three stages of applying for and acquiring a patent.

## Before you begin

You must update the locale settings in the system properties and then configure the system locale currency before configuring the patent rewards. For more information, see [Locale settings](https://www.servicenow.com/docs/access?context=locales&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and [Configuring FX Currency global settings](https://www.servicenow.com/docs/access?context=fx-currency-configure&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Role required: sn\_lg\_ip.patent\_config

## Procedure

1.  Set up a reward cap for the maximum reward amount.

    If there are multiple inventors, the amount is automatically divided equally among them.

    1.  Navigate to **All** &gt; **Legal Practice Apps** &gt; **Intellectual Property** &gt; **Patent Reward Caps**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        | | |
        |---|---|
        |Start Date|Date from which the patent reward cap is implemented.|
        |End Date|Date until which the patent reward cap is implemented.|
        |Reward Cap|Maximum limit of the reward amount in system currency.|

    4.  Select **Submit**.

2.  Configure the reward based on the country of residence of the inventor.

    1.  Navigate to **All** &gt; **Legal Practice Apps** &gt; **Intellectual Property** &gt; **Patent Rewards per Country**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

<table id="table_c3q_lr5_zyb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Country

</td><td>

Name of the inventor's country.

</td></tr><tr><td>

From currency

</td><td>

Currency of the selected country.

</td></tr><tr><td>

To currency

</td><td>

The system locale currency.

</td></tr><tr><td>

Country specific reward cap

</td><td>

The maximum limit of the reward amount in the inventor's country's currency and also holds stage wise rewards caps.**Note:** If multiple inventors are associated with the patent request, the reward is automatically split equally among them.

</td></tr><tr><td>

Forex Conversion Rate

</td><td>

Foreign exchange conversion rate of the amount.

</td></tr><tr><td>

Start Date

</td><td>

Date from which the country reward is implemented.

</td></tr><tr><td>

End Date

</td><td>

Date until which the country patent reward is implemented.

</td></tr></tbody>
</table>3.  Determine whether a reward is granted at various stages of the patent application process.

    1.  Navigate to **All** &gt; **Legal Practice Apps** &gt; **Intellectual Property** &gt; **Patent Rewards per Country**.

    2.  Select the amount in the **Country Specific Reward Cap** column of the new country entry.

    3.  On the Stage rewards form, select **New**.

    4.  On the form, fill in the fields.

<table id="table_wxl_jvb_1zb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Amount

</td><td>

Amount to be rewarded to the inventor for the selected status.

</td></tr><tr><td>

Patent rewards per country

</td><td>

The country of the inventor to whom the patent is granted. This field is auto-populated.

</td></tr><tr><td>

Application status

</td><td>

The status of the application at which the inventor should be rewarded.The stages of an application at which rewards can be granted are:

-   Proceed with Application
-   Patent Filed
-   Patent Granted


</td></tr></tbody>
</table>
**Parent Topic:**[Configuring Legal Invention Disclosure](../concept/configure-legal-invention-disclosure.md)

