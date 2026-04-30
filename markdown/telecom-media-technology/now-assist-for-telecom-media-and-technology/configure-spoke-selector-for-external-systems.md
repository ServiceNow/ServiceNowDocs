---
title: Configure the spoke selector for external systems
description: Configure the spoke selector for Aria to enable the configuration and execution of billing requests.
locale: en-US
release: yokohama
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2025-04-14"
reading_time_minutes: 2
breadcrumb: [Help remediate bill issues, Customer Service Problem Management agentic workflows, Use agentic workflows, Now Assist for Telecommunications, Media and Technology \(TMT\), Telecommunications, Media, and Technology]
---

# Configure the spoke selector for external systems

Configure the spoke selector for Aria to enable the configuration and execution of billing requests.

## Before you begin

Role required: admin

## About this task

The spoke selector application provides a common framework that enables the configuration and execution of integration requests. It operates by selecting the matching implementations based on the configured input parameters for each request.

## Procedure

1.  Navigate to **All** &gt; **Spoke selector** &gt; **Request type**.

2.  Select **Billing request**.

    The billing request is configured with a request definition that invokes Aria APIs. This demo implementation serves as a reference for configuring a new request definition that retrieves billing-related data from third party systems.

3.  Create the Integration request definitions.

    By giving an appropriate value for **Order** or by defining the **Selection condition** the new request definition that fetches the billing-related data is triggered.

4.  To create Integration request definitions, navigate to **All** &gt; **Spoke selector** &gt; **Request definition**.

5.  In the Integration request definitions screen, select **New** in the header section.

    ![Integration request definitions screen.](../image/aiagent-integration-request-definition.png)

6.  On the form, fill in the fields.

<table id="table_y44_y2z_z2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the integration request type.

</td></tr><tr><td>

Type

</td><td>

Billing request selection is made as the integration request type.

</td></tr><tr><td>

Description

</td><td>

Brief description of the request definition.

</td></tr><tr><td>

Order

</td><td>

Request definition is executed in the least order value.

</td></tr><tr><td>

Adapter type

</td><td>

Flow

</td></tr><tr><td>

Request adapter

</td><td>

Name of the Flow configured to fetch the records for the respective configuration type.**Note:** The sys\_hub\_flow record with the correct flow inputs, flow outputs, and flow snapshots.

</td></tr><tr><td>

Application

</td><td>

Store application details.

</td></tr><tr><td>

Domain

</td><td>

Global

</td></tr><tr><td>

Condition

</td><td>

Condition to trigger the request adapter.

</td></tr></tbody>
</table>    The following parameters must be included in the request for the Get Account Details Request for Aria API request adapter:

    ```
    
    {"api_name":"get_acct_details","request_body":{"client_acct_id":"FT0010001"}}
    
    ```

    The following parameters must be included in the response for the Get Account Details Response for Aria API request adapter:

    ```
    {"status_code":"1","status_reason":"","response_body":{"master_plan_info_list":{"48477095":"Business Internet + 
               Cellphone PI0001061"},"company_name":"Flash Telecom","acct_no":"27045400"}}
    ```

    The following parameters must be included in the request for the Get Invoice History Request for Aria API request adapter:

    ```
    {"api_name":"get_invoice_history","request_body":{"acct_no":"27045400"}}
    
    ```

    The following parameters must be included in the response for the Get Invoice History Response for Aria API request adapter:

    ```
    {"status_code":"1","status_reason":"","response_body":{"invoices":
    [{"amount":135.7,"invoice_no":254547358,"due_date":"2024-11-
    30","outstanding_amount":135.7,"usage_bill_from":"2024-10-01","usage_bill_thru":"2024-10-31"},
    {"amount":190.26,"invoice_no":254547359,"due_date":"2024-12-
    31","outstanding_amount":190.26,"usage_bill_from":"2024-11-01","usage_bill_thru":"2024-11-30"},
    {"amount":172.95,"invoice_no":254547360,"due_date":"2025-01-
    31","outstanding_amount":172.95,"usage_bill_from":"2024-12-01","usage_bill_thru":"2024-12-31"},
    {"amount":437.07,"invoice_no":254547361,"due_date":"2025-02-
    28","outstanding_amount":0,"usage_bill_from":"2025-01-01","usage_bill_thru":"2025-01-31"}]}}
    ```

    The following parameters must be included in the request for the Get Invoice Details Request for Aria API request adapter:

    ```
    {"api_name":"get_invoice_details","request_body":{"acct_no":"27045400","invoice_no":"254547361"}}
    
    ```

    The following parameters must be included in the response for the Get Invoice Details Response for Aria API request adapter:

    ```
    {"status_code":"1","status_reason":"","response_body":{"line_items":
    [{"usage_type_no":10058138,"amount":0,"service_name":"Mobile Data
    GB","sold_product_number":"PI0001065","service_no":11196572,"description":"Mobile Data GB (10 gigabytes @
    $0)"},{"usage_type_no":10058138,"amount":14.35,"service_name":"Mobile Data
    GB","sold_product_number":"PI0001065","service_no":11196572,"description":"Mobile Data GB (18.847 gigabytes
    @ $1)"},{"usage_type_no":10058140,"amount":255.73,"service_name":"International Roaming Calls from
    EU","sold_product_number":"PI0001065","service_no":11197966,"description":"International Roaming Calls from
    EU (93 minutes @ $2.75)"},{"usage_type_no":10058144,"amount":0.5,"service_name":"Domestic
    Minutes","sold_product_number":"PI0001065","service_no":11196568,"description":"Domestic Minutes (9.91
    minutes @ $.05)"},{"usage_type_no":10058146,"amount":11.75,"service_name":"International Calls to
    Asia","sold_product_number":"PI0001065","service_no":11196570,"description":"International Calls to Asia (6.56
    minutes @ $1.79)"}]}}
    ```

7.  Select **Save**.


## Result

Once the condition is set and the request condition matched, the defined flow executes and the records for the configuration are fetched from the external provider that you selected, into your ServiceNow instance.

