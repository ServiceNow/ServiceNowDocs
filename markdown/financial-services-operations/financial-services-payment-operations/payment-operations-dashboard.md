---
title: Financial Services Payment Operations dashboard
description: With the Financial Services Payment Operations dashboard, you can get an insight into how your team and business are performing for payment inquiries, claims, and debits.
locale: en-US
release: xanadu
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Financial Services Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Financial Services Payment Operations dashboard

With the Financial Services Payment Operations dashboard, you can get an insight into how your team and business are performing for payment inquiries, claims, and debits.

**Important:** The Financial Services Payment Operations dashboard has been modernized to give you a better user experience.

You can monitor the status of these cases, see trends, and drill down into the details from a single view. For any time that you specify, you can view the details for the open cases, the new cases, and the average closing times of the payment cases.

## Required ServiceNow AI Platform roles

-   sn\_bom\_payment.manager, required to view the dashboard widgets and data.
-   sn\_bom\_payment.admin, sn\_bom\_pa.admin, and pa\_admin, required to edit the dashboard.

## Access the Financial Services Payment Operations dashboard

To access the Financial Services Payment Operations dashboard, navigate to **Workspaces** &gt; **Financial Services Workspace** &gt; **Analytics Center** \(![Analytics center icon.](../../../product/fso-personal-lines-claims/image/analytics-center-icon.png)\).

Alternatively, you can navigate to **All** &gt; **Payment Operations** &gt; **Analytics**.

You can also access the dashboard from the Platform Analytics Workspace. For more information about the Platform Analytics Workspace, see [Analytics Center](https://www.servicenow.com/docs/access?context=analytics-center&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

If you have upgraded from an earlier version, you can access the existing Core UI dashboard layout as usual by navigating to **All** &gt; **Payment Operations** &gt; **Dashboard**.

## Use cases

For examples of how different people in your organization can use this dashboard, see the use cases in the following table.  

<table id="table_jhd_dgj_t4b"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Payment manager

</td><td>

Needs to gain visibility into the real-time status of the payment cases and do the following tasks:-   Monitor all the open payment cases that have breached an Service Level Agreement \(SLA\)
-   Monitor the volume of each payment case type and their trend
-   Review agent productivity
-   Review the average closing time of cases for a service, agent, or group
-   Monitor the details of claims by error type
-   Drill down into the details in an error category

</td></tr><tr><td>

Payment admin

</td><td>

Needs to be able to customize views.

</td></tr></tbody>
</table>## Indicators

-   **% of open internal claims having customer error based upon payment processor**

    Percentage of the open internal claims that have a customer error based on the payment processor. The score is calculated according to this formula:

    ```
    ([Total Number of open internal claims having customer error grouped by payment processor]/[Total Number of open internal claims having customer error])*100
    ```

-   **% of closed external claims having bank error based upon actual treatment**

    Percentage of the closed external claims that have a bank error based on the actual treatment where the breakdown is Outcome reason. The score is calculated according to this formula:

    ```
    ([Number of closed external claims having bank error based upon outcome]/[Total number of closed external claims having bank error used in total number recovery])*100
    ```

-   **% of open internal claims having bank error based upon error category**

    Percentage of the open internal claims that have a bank error based on the error category where the breakdowns are Age and Bank error category. The score is calculated according to this formula:

    ```
    ([Total Number of open internal claims having bank error based upon error category]/[Total number of open internal claims having bank error])*100
    ```

-   **% of total claim amount refunded for external claims having customer error**

    Percentage of the total claim amount refunded for external claims that have a customer error where the breakdowns is Actual treatment. The score is calculated according to this formula:

    ```
    ([Sum of refund amount for closed external claims having customer error based upon Actual treatment]/[Total sum of refund amount for closed external claims having customer error])*100
    ```

-   **% of closed external claims having customer error based upon actual treatment**

    Percentage of the closed external claims that have a customer error based on the actual treatment where the breakdown is Outcome reason. The score is calculated according to this formula:

    ```
    (([Total number of closed external claims having customer error based upon outcome]/[Total number of closed external claims having customer error])*100)||0
    ```

-   **% of open internal claims having bank error based upon requested treatment**

    Percentage of the open internal claims that have a bank error based on a requested treatment where the breakdowns are Age and Payment processor. The score is calculated according to this formula:

    ```
    ([Total Number of open internal claims having bank error grouped by payment processor]/[Total count of open internal claims having bank error based upon requested treatment])*100
    ```

-   **% of open internal claims having requested treatment as exception**

    Percentage of the open internal claims that have a requested treatment as an exception where the breakdowns are Age and Error type. The score is calculated according to this formula:

    ```
    ([Number of open cases having requested treatment as Exception]/[Total Number of open cases having requested treatment as Exception])*100
    ```

-   **% closing Time of payment cases**

    Percentage of the closing time of payment cases where the breakdowns are Age, Payment cases, and Payment agent. The score is calculated according to this formula:

    ```
    [Summed Duration of Payment Closed Cases]/[Number of Payment Closed Cases] /24
    ```

-   **% of total claims recovered for external claims having refunded amount**

    Percentage of the total claims recovered for external claims that have a refunded amount where the breakdown is Actual treatment. The score is calculated according to this formula:

    ```
    ([Sum of refund amount for closed external claims having bank error]/[Total sum of refund amount for closed external claims having bank error])*100
    ```

-   **% of closed external claims having bank error for actual split treatment**

    Percentage of the closed external claims that have a bank error for an actual split treatment where the breakdown is Actual treatment. The score is calculated according to this formula:

    ```
    ([Total number of closed external claims having bank error based upon actual treatment]/[Total number of closed external claims having bank error])*100
    ```

-   **% of open internal claims having customer error based upon requested treatment**

    Percentage of the open internal claims that have a customer error based on the requested treatment where the breakdowns are Age and Customer error category. The score is calculated according to this formula:

    ```
    ([Total Number of open internal claims having customer error with custom error category]/[Total Number of open internal claims having customer error])*100
    ```

-   **% of closed external claims having customer error for actual treatment**

    Percentage of the closed external claims that have a customer error for the actual treatment. The score is calculated according to this formula:

    ```
    ([Total number of closed external claims having customer error based upon actual treatment]/[Total number of closed external claims having customer error])*100
    ```

-   **% of internal claims having requested treatment as protected**

    Percentage of the internal claims that have a requested treatment as protected where the breakdowns are Age and Error type. The score is calculated according to this formula:

    ```
    ([Number of open cases having requested treatment as Protected]/[Total number of open cases having requested treatment as Protected])*100
    ```

-   **Number of closed external claims having customer error with requested treatment as exception**

    Number of the closed external claims that have a customer error with a requested treatment as an exception where the breakdown is Actual Treatment.


## Breakdowns

-   Actual Treatment
-   Age
-   Bank Error Category
-   Customer Error Category
-   Error Type
-   Outcome Reason
-   Payment Agent
-   Payment Cases
-   Payment processor
-   Payment Service
-   Payment Type

## Filters

The following table shows the available filters in the Payment Operations dashboard.

|Name|Type|Description|
|----|----|-----------|
|Actual Treatment|Choice|Shows the choices available for the actual treatment of payment claims.|
|Age|Bucket|Shows the age ranges in days for the payment cases.|
|Bank Error Category|Choice|Shows the choices available for the bank error category for payment claims.|
|Customer Error Category|Choice|Shows the choices available for the customer error category for payment claims.|
|Error Type|Choice|Shows the choices available for the error type for payment inquiries.|
|Outcome Reason|Choice|Shows outcome choices available for payment claims.|
|Payment Agent|Script|Fetches the assigned payment agents with the sn\_bom\_payment.claim\_agent or sn\_bom\_payment.inquiry\_agent role from the User Role table.|
|Payment Cases|Script|Fetches the payment case records from the Task table.|
|Payment Processor|Choice|Shows the choices available for Payment Processor for methods of payments.|
|Payment Service|List|Fetches the records for all payment tasks.|
|Payment Type|Script|Fetches the payment case records from the Task SLA table.|

**Parent Topic:**[Platform Analytics Solutions for Financial Services Operations](../../application-content-packs/concept/fso-content-pack.md)

