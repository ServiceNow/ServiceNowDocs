---
title: Run Have I Been Pwned enrichment integration
description: Run the Have I Been Pwned \(HIBP\) enrichment on an email address or domain name observable to determine whether it has been involved in a known data breach.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-02-24"
reading_time_minutes: 5
keywords: [Have I Been Pwned, HIBP, observable enrichment, integration, breach detection]
breadcrumb: [Observable Enrichment, Run Enrichment operations in TISC, Observables, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Run Have I Been Pwned enrichment integration

Run the Have I Been Pwned \(HIBP\) enrichment on an email address or domain name observable to determine whether it has been involved in a known data breach.

## Before you begin

Role required: sn\_sec\_tisc.analyst

Ensure that the Have I Been Pwned integration is configured and enabled by your administrator. For more information, see [Configure and enable Have I Been Pwned integration](tisc-config-hipw-integration.md).

## About this task

The integration queries the HIBP database to identify whether a submitted observable has been exposed in a publicly known data breach.

**Note:** The integration supports only the following observable types:

-   Email address
-   Domain name

Submitting an unsupported observable type such as an IP address or file hash results in the observable being excluded from enrichment with an alert message indicating that an unsupported observable type. Observables on the allow list are also excluded from submission.

You can initiate enrichment from an individual observable record or from the **Artifacts** tab of a case when working with multiple observables.

## Procedure

1.  Navigate to the observable record you want to enrich.

    1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intelligence Library** and open any observable record from the Threat Intelligence Library.

        ![TISC Observables form view](../image/tisc-hibp-obs-enrichment.png)

    2.  \(Alternatively\) open a case, navigate to the **Artifacts** tab, and select the **Observables** related list from Case to run observable enrichment.

        ![image.tisc-case-obs-enrich-result]

2.  Select the observable or observables you want to submit for enrichment.

    When working from a case, you can select multiple observables at a time. Only observables of supported types are submitted. Unsupported types and allow listed observables are automatically filtered out.

3.  Click **Run Observable Enrichment**.

4.  Select **Have I Been Pwned** from the list of available integrations.

5.  Click **Submit**.

    An activity stream entry is created indicating that enrichment has been initiated. After processing completes, a result record is created in the enrichment results table.


## Result

To view the enrichment results:

1.  Navigate to any observable record.
2.  Go to **Enrichment Results** tab.
3.  Select **Observable Enrichment Results** and open the result record.

    ![Observable enrichment results section](../image/tisc-hibp-obs-enrich-view.png)


## What to do next

**Viewing enrichment results**

The enrichment displays the corresponding results in the following sections:

-   **Details**: Provides the summary of the observable enrichment integration for the selected observable. This section includes total number of breaches identified and a concise summary of the most recent breaches. It also provides the raw response returned by the integration for reference.

<table id="table_wvb_3lg_m3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique system generated identifier for the Have I Been Pwned enrichment record.

</td></tr><tr><td>

Observable

</td><td>

An observable record such as email address or domain submitted for breach identification.

</td></tr><tr><td>

Created

</td><td>

Date and time when the observable enrichment was executed and the observable enrichment results record was created.

</td></tr><tr><td>

Result

</td><td>

Displays the outcome of the observable. When an observable is associated with breaches, the result will show **Breaches Found**.If no breaches are identified, the result indicates **Breaches Not Found**.

</td></tr><tr><td>

Summary

</td><td>

Provides an overview of observable enrichment results including:-   total number of breaches identified.
-   the most recent breaches.
-   key details such as breach title, domain, and breach date \(for a domain type of observable\).
View the summary section for a quick review of breach results.

</td></tr><tr><td>

Raw Result

</td><td>

Displays the response returned by the Have I Been Pwned API in JSON format. This field is intended for validation and troubleshooting purposes.

</td></tr></tbody>
</table>    ![TISC HIBP observable enrichment results- details view](../image/tisc-hibp-enrich-details-view.png)

-   **Breaches**: Displays breach records associated to the observable domain or email, as retrieved from the HIBP integration. Each record includes the breach title, domain, breach date, number of affected accounts, exposed data classes, and the date the breach was added to HIBP.

    |Field|Description|
    |-----|-----------|
    |Have I Been Pwned Entry|Unique entry for the enrichment record.|
    |Title|title for the breach unique across all breaches.|
    |Domain|The domain of the primary website the breach occurred on.|
    |Added to HIBP|The date and time \(precision to the minute\) the breach was added to the system in ISO 8601 format.|
    |Breach Occurred|The date \(with no time\) the breach originally occurred on in ISO 8601 format \(This is not always accurate\).|
    |Modified Date|The date and time \(precision to the minute\) the breach was modified in ISO 8601 format. This will only differ from the AddedDate attribute if other attributes represented here are changed or data in the breach itself is changed.|
    |Affected Accounts|The total number of accounts loaded into the system.|
    |External Link|Link to the respective breach record in Have I Been Pwned.|
    |Data Classes|Describes the nature of the data compromised in the breach.|
    |Description|Contains an overview of the breach.|
    |Logo Path|A URL that specifies where a logo for the breached service can be found.|
    |Attribution|Sometimes requested by the party that provides the data to HIBP.|
    |Disclosure URL|Hyperlink that contains public forum information such as news reported on the breach.|

    ![TISC HIBP observable enrichment results breaches.](../image/tisc-hibp-enrich-breach.png)


**View HTML Response**: Select this button to view the complete `html` response returned by the Have I Been Pwned integration for the selected observable. This view shows the unprocessed source data exactly as received. Use this option for validation, troubleshooting, or audit purposes to review the response payload.

You can also view the Have I Been Pwned flags, which indicate the attributes identified in the unprocessed source data, as described in the following table.

|Related Record|Description|
|--------------|-----------|
|Verified|Indicates that the breach is considered unverified. An unverified breach is still loaded into HIBP when there's sufficient confidence that a significant portion of the data is legitimate.|
|Malware|Indicates that the data was sourced from a malware campaign rather than a security compromise of an online service.|
|Sensitive|Indicates that the breach is considered sensitive. The public API will not return any accounts for a breach flagged as sensitive.|
|Fabricated|Indicates that the breach is considered fabricated. However, it still contains legitimate email addresses.|
|StealerLog|Indicates if the breach is sourced from stealer logs.|
|Retired|Indicated that this data has been retired \(permanently removed\) and will not be returned by the API.|
|SpamList|Indicates that the data has not come as a result of a security compromise \(or is a spam list\).|
|Subscription Free|Indicates if the breach is subscription-free.|

![TISC HIBP Observable enrichment results - View HTML Response](../image/tisc-hibp-view-html-response.png)

**Note:** The HIBP integration provides breach awareness only. It does not support actions to remediate or resolve breaches, as the breaches originate from external third-party systems.

**Parent Topic:**[Observable Enrichment](../concept/tisc-observable-enrichment.md)

**Related topics**  


[Configure Observable Enrichment](configure-observable-enrichment.md)

[Configure and enable Have I Been Pwned integration](tisc-config-hipw-integration.md)

