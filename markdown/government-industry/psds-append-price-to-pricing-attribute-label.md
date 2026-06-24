---
title: Append price to Pricing Attribute label​
description: Prices are appended to Boolean Price Attributes by default. Client scripts must be added for the price choice attributes​ and the price control attributes to append to prices when there are price adjustments.As an admin, you can add and modify client scripts to configure forms, fields, and field attributes \(such as price choice attributes\) while the user is filling out the form​.As an admin, you can add and modify client scripts to configure forms, fields, and field attributes \(such as price control attributes\) while the user is filling out the form​.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/government-industry/psds-append-price-to-pricing-attribute-label.html
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [License and Permit Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Append price to Pricing Attribute label​

Prices are appended to Boolean Price Attributes by default. Client scripts must be added for the price choice attributes​ and the price control attributes to append to prices when there are price adjustments.

## Add Client Scripts to Price Choice Fields​

As an admin, you can add and modify client scripts to configure forms, fields, and field attributes \(such as price choice attributes\) while the user is filling out the form​.

### Before you begin

Role required: admin

### About this task

Client scripts allow the system to run JavaScript on the client \(web browser\) when client-based events occur on the Government Service Portal, such as when a constituent makes a choice, submits a form, or changes a value. For more information on client scripts, see [Client scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/application-development/scripts/client-scripts.md).

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Client Scripts**.

2.  Select **New**.

3.  Specify a name for the script​.

    For example, if you are adding a script to update the price values each time the permit type is changed by the constituent submitting the application, you may wish to label your script "Update Price Label on Permit Type Change".

4.  Set the table to the License/Permit case extension table​.

5.  Set UI type to **All**​, and set the Type to **OnChange**.

6.  Select the price choice field under the dropdown for field name.

    In the above example, the field name selected would be **Commercial Permit Type**; that is the choice the constituent makes that then determines the price values that are displayed. For more information on the client script form fields, see [Client scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/application-development/scripts/client-scripts.md).

7.  Enter the script with the content below​:

    ```
    function onChange(control, oldValue, newValue, isLoading, isTemplate) {​
    if (isLoading) {​
    return;​
    }​
    g_scratchpad.updatePriceLabel(); ​
    }​
    ```

8.  Select **Submit**.


## Add Client Scripts to Price Control Fields​

As an admin, you can add and modify client scripts to configure forms, fields, and field attributes \(such as price control attributes\) while the user is filling out the form​.

### Before you begin

Role required: admin

### About this task

Client scripts allow the system to run JavaScript on the client \(web browser\) when client-based events occur on the Government Service Portal, such as when a constituent makes a choice, submits a form, or changes a value. For more information on client scripts, see [Client scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/application-development/scripts/client-scripts.md).

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Client Scripts**.

2.  Select **New**.

3.  Specify a name for the script​.

    For example, if you are adding a script to update the price value based on whether or not the constituent communicates that they are a resident of the requested location, you may wish to label your script "Update Price Label on Resident Change".

4.  Set the table to the License/Permit case extension table​.

5.  Set UI type to **All**​, and set the Type to **OnChange**.

6.  Select the price control field under the dropdown for field name.

    In the above example, the field name selected would be **Resident**; that is the control field then determines the price value that is displayed. For more information on the client script form fields, see [Client scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/application-development/scripts/client-scripts.md).

7.  Enter the script with the content below​:

    **Note:** Remove `newValue === ''` in the script if the field type is a choice​.

    ```
    function onChange(control, oldValue, newValue, isLoading, isTemplate) {​
    if (isLoading || newValue === '') {​
    return;​
    }​
    g_scratchpad.updatePriceLabel(); ​
    }​
    ```

8.  Select **Submit**.


