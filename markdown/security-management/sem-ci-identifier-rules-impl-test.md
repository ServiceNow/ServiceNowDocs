---
title: Steps to help prevent duplicate or orphaned records after running lookup rules
description: Take steps to help prevent duplicate or orphan records resulting from matching \(configuration items \(CIs\) within the CMDB.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Associating finding with a configuration item using lookup rules, Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Steps to help prevent duplicate or orphaned records after running lookup rules

Take steps to help prevent duplicate or orphan records resulting from matching \(configuration items \(CIs\) within the CMDB.

If rules aren’t carefully constructed, importing security exposure data can be taxing on an instance and performance issues with resources can occur. The logic used to iterate through and perform matching within the CMDB can result in lengthy processing times. Thorough testing and debugging of processing scripts in the rules helps alleviate the potential of issues later in the process.

## Avoid duplicate or orphaned records

-   Use small subsets of data that are specific to the lookup rule being tested.
    -   Set all lookup rules, other than the one being tested, to inactive.
    -   Analyze the imported CIs to ensure that you’re observing the expected behavior and matching is occurring properly.
-   Review matched CIs
    -   Examine the count of matched vs unmatched CIs. Ensure that the percentage is acceptable. Don’t look at the first page that is likely the first one inserted.
    -   Manually search for some CIs.
    -   Check to see if there are any naming or field problems \(such as searching for a specific domain\).

        If it seems appropriate, add additional matching rules.

-   Review Unmatched CIs
    -   Navigate to the Unmatched CIs table.
    -   Group by Configuration Item class.
    -   Review any classes that don’t look right \(certificates, network cards, images\).
        -   Figure out why didn’t they match the correct CI?
        -   Should the class be excluded?
        -   Should the class be elevated to a related class?
-   Review CI states such as **Retired**.
-   Remove Test Data
    -   Once you begin to observe the correct or expected behavior in CI matching, start over.
    -   Start over by: Deleting the data used for testing: \(see the **Deleting data from tables** section\)
        -   Discovered Items
        -   Vulnerable Items
        -   Remediation tasks
    -   Manually rerunning all the CI Matching rules.

For more information on lookup rules and Qualys, see the [KB0750656](https://support.servicenow.com/kb_view.do?sysparm_article=KB0750656) article.

For more information on lookup rules and Rapid7, see the [KB0818096](https://support.servicenow.com/kb_view.do?sysparm_article=KB0818096).

## Deleting data from tables

Sometimes you have imported data and realize something is wrong. If something is wrong in a development or performance environment, you could reclone from a better environment, but that isn’t always an option.

**Note:** Performing these actions requires ServiceNow expertise.

There are four options for deleting data from tables:

-   Using **Delete All Records** on **Table Configuration**.
-   Configure the **Table Cleaner** by navigating to **Auto Flushes** \(sys\_auto\_flush.list\) and creating a **Auto-flush** record.
-   Truncate the gs.truncateTable using a background script.

    Using **truncateTable** requires turning off the record for rollback check box in the background scripts. Otherwise, a copy of the table and related cascade tables are created, take too long, and most likely fail.

    **Note:** Never use **truncateTable** in a production environment. Consult you Support representative before executing large deletions in production or shared environments.


**Parent Topic:**[Associating finding with a configuration item using lookup rules](sem-associate-finding-configuration-item-using-lookup-rules.md)

