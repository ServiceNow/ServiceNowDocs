---
title: HealthScan definitions updates: November release
description: Some HealthScan definitions are deprecated or updated between releases.
locale: en-US
release: xanadu
product: Impact Health Assessment
classification: impact-health-assessment
topic_type: reference
last_updated: "2024-10-29"
reading_time_minutes: 6
breadcrumb: [HealthScan definitions, HealthScan, Platform Health, Impact Digital Experience, Impact]
---

# HealthScan definitions updates: November release

Some HealthScan definitions are deprecated or updated between releases.

## Deprecated definitions

The following definitions have been deprecated for the November release.

|Number|Short description|Rating|Related portfolio|Category|Reason for deprecation|
|------|-----------------|------|-----------------|--------|----------------------|
|HSD0004695|Ensure gamification ranges do not overlap and have a unique start value.|Recommend|Configuration Review for CSM|Manageability|Merged with HSD0004987|

## Updated definitions

The following definitions have been updated for the November release to improve performance, reduce false positives, and meet the latest coding practices. Some of these definitions will have a positive or negative impact on your customer instance scores.

Due to process and technical constraints, a comprehensive impact analysis for the overall score impact could not be fully conducted for customer instances. As a result, there may be potential impact score drops that have not been identified or addressed.

<table id="table_h2p_mmd_fdc"><thead><tr><th>

Number

</th><th>

Short description

</th><th>

Rating

</th><th>

Category

</th><th>

Update description

</th></tr></thead><tbody><tr><td>

HSD0001041

</td><td>

Customer accounts without primary contact

</td><td>

Discuss

</td><td>

Manageability

</td><td>

-   Improved code to follow HealthScan definition guidelines
-   Documentation link update

</td></tr><tr><td>

HSD0001058

</td><td>

Scoped app uses logging utils or deprecated methods for logging rather than the verbosity method

</td><td>

Act

</td><td>

Manageability

</td><td>

-   Improved performance with more reliance on the database to filter records
-   Accurate line numbers
-   Reduced number of false positives

</td></tr><tr><td>

HSD0001128

</td><td>

Client-side code should not use synchronous AJAX methods

</td><td>

Recommend

</td><td>

Performance

</td><td>

-   Added query for catalog and client scripts: type!=onSubmit
-   Implemented updated line numbering and comment handling
-   Added try/catch to ensure better stability

</td></tr><tr><td>

HSD0001193

</td><td>

Use the condition field in Business Rules

</td><td>

Discuss

</td><td>

Manageability

</td><td>

Modified the initial query to include "Script not empty" and "when" conditions and removed it from the detailed analysis part of the HSD code

</td></tr><tr><td>

HSD0001459

</td><td>

Missing key contact details - Email or Account

</td><td>

Discuss

</td><td>

Manageability

</td><td>

-   Improved code to follow HealthScan definition guidelines
-   Valid documentation link update

</td></tr><tr><td>

HSD0001475

</td><td>

Entitlements without duration \(start and end date\)

</td><td>

Discuss

</td><td>

Manageability

</td><td>

-   Improved code to follow HealthScan definition guidelines
-   Valid documentation link update

</td></tr><tr><td>

HSD0001484

</td><td>

Missing Asset Information - Primary Contact or Location

</td><td>

Discuss

</td><td>

Manageability

</td><td>

-   Improved code to follow HealthScan definition guidelines
-   Valid documentation link update

</td></tr><tr><td>

HSD0001507

</td><td>

A dedicated integration user runs actions in place of the default admin user

</td><td>

Act

</td><td>

Security

</td><td>

-   Corrected typo leading all queries on this to fail and return all records
-   Filtered out tables that don't have a user field available on the form view
-   Filtered out baseline records
-   Added query to return the jobs running as admin \(without a user value\)
-   Added display on Findings to make this distinction clear
-   Added 1k Findings limit

</td></tr><tr><td>

HSD0001533

</td><td>

The default "system" user preference for "rows per page" should be set to 50 or less

</td><td>

Recommend

</td><td>

Performance

</td><td>

-   Replaced documentation URL
-   Always creates a statistic
-   Added defensive scripting

</td></tr><tr><td>

HSD0001623

</td><td>

Read ACLs \(Security rules\) should not have GlideRecord, GlideAggregate, or GlideRecordSecure in script

</td><td>

Act

</td><td>

Performance

</td><td>

-   Improved code
-   Avoided use of ScriptUtils performMatch and search override
-   Fixed incorrect line numbering
-   Resolved multiple inquiries
-   Considered GlideRecordSecure in the findings along with GlideRecord and GlideAggregate

</td></tr><tr><td>

HSD0001627

</td><td>

Do not query audit log in custom integrations and code

</td><td>

Recommend

</td><td>

Performance

</td><td>

-   Improved performance with more reliance on the database to filter records
-   Accurate line numbers
-   Reduced number of false positives

</td></tr><tr><td>

HSD0001662

</td><td>

Differs from baseline: Business Rules

</td><td>

Recommend

</td><td>

Upgradeability

</td><td>

-   Excludes custom applications
-   Queries for customized business rules from store apps
-   Resolved multiple inquiries
-   Improved accuracy and performance
-   Increased the number of findings
-   Added findings limit and defensive scripting

</td></tr><tr><td>

HSD0001664

</td><td>

Differs from baseline: Script Includes

</td><td>

Recommend

</td><td>

Upgradeability

</td><td>

-   Excludes custom applications
-   Improved performance by not checking twice for baseline

</td></tr><tr><td>

HSD0001665

</td><td>

Differs from baseline: Client Scripts \(and UI Scripts\)

</td><td>

Recommend

</td><td>

Upgradeability

</td><td>

-   Excludes custom applications
-   Queries for customized client scripts from store apps
-   Resolved multiple inquiries
-   Improved accuracy and performance
-   Increased the number of findings
-   Added findings limit and defensive scripting

</td></tr><tr><td>

HSD0001877

</td><td>

Customer Contact should not have the snc\_internal role

</td><td>

Act

</td><td>

Manageability

</td><td>

Improved code to follow HealthScan definition guidelines

</td></tr><tr><td>

HSD0002056

</td><td>

Knowledge articles older than 12 months may be unduly aging

</td><td>

Recommend

</td><td>

Manageability

</td><td>

-   Added logic to not create the single Finding on zero results
-   Added try/catch logic
-   Added Statistical score for visibility on zero

</td></tr><tr><td>

HSD0002295

</td><td>

Service Contracts without duration \(Start and End Date\)

</td><td>

Recommend

</td><td>

Manageability

</td><td>

Improved code to follow HealthScan definition guidelines

</td></tr><tr><td>

HSD0002299

</td><td>

Feature adoption: Automated Case Assignment

</td><td>

Recommend

</td><td>

Manageability

</td><td>

Improved code to follow HealthScan definition guidelines

</td></tr><tr><td>

HSD0002300

</td><td>

CSM Demo Data Plugin Installation

</td><td>

Discuss

</td><td>

Manageability

</td><td>

Improved code to follow HealthScan definition guidelines

</td></tr><tr><td>

HSD0002371

</td><td>

Product Adoption: Use CSM to streamline your Customer Service operations

</td><td>

Discuss

</td><td>

Manageability

</td><td>

-   Improved code to follow HealthScan definition guidelines
-   Changed execution type from Statistical to Automated

</td></tr><tr><td>

HSD0002372

</td><td>

Feature Adoption: Self-registration for customer contacts

</td><td>

Discuss

</td><td>

Manageability

</td><td>

Improved code to follow HealthScan definition guidelines

</td></tr><tr><td>

HSD0002437

</td><td>

Check whether strict mode for GlideRecord queries is active

</td><td>

Recommend

</td><td>

Manageability

</td><td>

Added defensive scripting by means of try/catch/finally structure to ensure a statistic

</td></tr><tr><td>

HSD0002534

</td><td>

Duplicate Cases created with the same number

</td><td>

Discuss

</td><td>

User Experience

</td><td>

-   Improved code to follow HealthScan definition guidelines
-   Restricted Max finding to 75

</td></tr><tr><td>

HSD0002828

</td><td>

All events should have the "fired by" field populated

</td><td>

Recommend

</td><td>

Manageability

</td><td>

-   Returns multiple findings up to a maximum of 1000
-   Each finding groups flagged events by application and displays the event count per app
-   Each finding links to a list page of flagged events for the same application
-   Returns custom \(rather than OOTB\) events
-   Defensive scripting in case of table accessibility issues
-   Statistic is always returned
-   Statistic represents the cumulative count

</td></tr><tr><td>

HSD0003784

</td><td>

Check for unhandled duplicate CI tasks

</td><td>

Discuss

</td><td>

User Experience

</td><td>

-   Added defensive scripting by means of try/catch/finally structure to ensure a statistic
-   Added check for short\_description field exists
-   Migrated to GlideAggregrate for overall count
-   Added 30 days filter to Findings
-   Added 1000 Findings limit

</td></tr><tr><td>

HSD0004419

</td><td>

Deactivate stale user accounts

</td><td>

Recommend

</td><td>

Manageability

</td><td>

-   Returns finding if 1 or more inactive users are found
-   Always returns statistic
-   Filters out users created less than 1 month ago
-   Defensive scripting in case of issues with tables

</td></tr><tr><td>

HSD0004672

</td><td>

Every Knowledge Base should have Knowledge Manager populated

</td><td>

Recommend

</td><td>

User Experience

</td><td>

-   Improved code to follow HealthScan definition guidelines
-   Fixed spelling errors

</td></tr><tr><td>

HSD0004689

</td><td>

Enables session caching.

</td><td>

Recommend

</td><td>

User Experience

</td><td>

Improved code to follow HealthScan definition guidelines

</td></tr><tr><td>

HSD0004690

</td><td>

Enables the user-mentions functionality in Communities content.

</td><td>

Recommend

</td><td>

User Experience

</td><td>

Improved code to follow HealthScan definition guidelines

</td></tr><tr><td>

HSD0004692

</td><td>

Enables Google re-CAPTCHA on the self-registration page with Communities

</td><td>

Recommend

</td><td>

Security

</td><td>

Improved code to follow HealthScan definition guidelines

</td></tr><tr><td>

HSD0004693

</td><td>

Enable Gamification on Community

</td><td>

Recommend

</td><td>

User Experience

</td><td>

Improved code to follow HealthScan definition guidelines

</td></tr><tr><td>

HSD0004974

</td><td>

Check if system property sn\_customerservice.consumer\_max\_new\_cases\_daily has been modified for consumer Cases per day

</td><td>

Recommend

</td><td>

Manageability

</td><td>

Improved code to follow HealthScan definition guidelines

</td></tr><tr><td>

HSD0004987

</td><td>

Ensure gamification has a unique level range name, that gamification ranges do not overlap, and have a unique start value.

</td><td>

Recommend

</td><td>

Manageability

</td><td>

Improved code to follow HealthScan definition guidelines

</td></tr><tr><td>

HSD0005255

</td><td>

Regression testing for ATF Quick Start Test "Major Issue Management"

</td><td>

Recommend

</td><td>

Upgradeability

</td><td>

Improved code to follow HealthScan definition guidelines

</td></tr><tr><td>

HSD0006666

</td><td>

Check if current.update\(\) is used in a business rule

</td><td>

Act

</td><td>

Performance

</td><td>

-   Improved code to follow HealthScan definition guidelines
-   Resolved multiple inquiries
-   Rectified incorrect line numbering

</td></tr><tr><td>

HSD0011774

</td><td>

Hardware Models should have Manufacturer and Model Number

</td><td>

Recommend

</td><td>

Manageability

</td><td>

Added a check: If there are 0 models, do not create a finding

</td></tr><tr><td>

HSD0012251

</td><td>

Hardware Asset Tags are unique

</td><td>

Discuss

</td><td>

Manageability

</td><td>

-   Updated documentation URL to the latest playbook
-   Removed finding when there are 0 duplicate asset tags

</td></tr><tr><td>

HSD0014977

</td><td>

GlideRecord.insert\(\) method should check for Null

</td><td>

Recommend

</td><td>

Manageability

</td><td>

-   Updated definition with latest comment handling
-   Added try/catch
-   Many performance improvements

</td></tr></tbody>
</table>