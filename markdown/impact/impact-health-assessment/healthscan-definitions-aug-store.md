---
title: HealthScan definitions updates: August release
description: Some HealthScan definitions are deprecated or updated between releases.
locale: en-US
release: yokohama
product: Impact Health Assessment
classification: impact-health-assessment
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [HealthScan definitions, HealthScan, Platform Health, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# HealthScan definitions updates: August release

Some HealthScan definitions are deprecated or updated between releases.

## Deprecated definitions

The following definitions have been deprecated for the August release.

**Important:** This list doesn't contain the definitions for the Security category.

|Number|Short description|Category|Reason for deprecation|
|------|-----------------|--------|----------------------|
|HSD0002058|Articles that should have been made inactive are still accessible in the KB|Manageability|Replaced by HSD0002056 and HSD0002465|
|HSD0002403|Add a finding for Skipped Items during last upgrade |Upgradeability|Duplicate HealthScan definition|
|HSD0018256|Find credentials with few or no affinities|Performance|Replaced by HSD0002198 |

## Updated definitions

The following definitions have been updated for the August release to improve performance, reduce false positives, and meet the latest coding practices. Some of these definitions will have a positive or negative impact on your customer instance scores.

**Important:** This list doesn't contain the definitions for the Security category.

<table id="table_l41_1dh_xcc"><thead><tr><th>

Number

</th><th>

Short description

</th><th>

Category

</th><th>

Included in Health Assessment scans 

</th><th>

Update description

</th></tr></thead><tbody><tr><td>

HSD0001060

</td><td>

Use UI Policies Instead of Client Scripts

</td><td>

Manageability

</td><td>

X

</td><td>

Improved performance

</td></tr><tr><td>

HSD0001278

</td><td>

Before Business Rules should not update\(\) or insert\(\) records on other tables

</td><td>

Performance

</td><td>

X

</td><td>

Improved performance

</td></tr><tr><td>

HSD0001338

</td><td>

Business Rules should not be defined on the Global table \(Global Business Rule\)

</td><td>

Performance

</td><td>

X

</td><td>

Added check to ignore out-of-the-box records

</td></tr><tr><td>

HSD0001372

</td><td>

Too many fields on a form

</td><td>

User Experience

</td><td>

X

</td><td>

-   Findings will now be reported for all forms and their form views.
-   Enhanced to not report form views that have 30 or more fields out-of-the-box. If fields are added on the form views and their count exceeds the threshold of 30, then a finding will be reported. 

</td></tr><tr><td>

HSD0001378

</td><td>

Reports not run for 3 months

</td><td>

Manageability

</td><td>

X

</td><td>

Definition updated to provide Findings

</td></tr><tr><td>

HSD0001387

</td><td>

Max page list size options should not be 100 or higher

</td><td>

Performance

</td><td>

X

</td><td>

Best Practice check introduced

</td></tr><tr><td>

HSD0001391

</td><td>

Number of users with the admin role

</td><td>

Manageability

</td><td>

X

</td><td>

Improved performance

</td></tr><tr><td>

HSD0001398

</td><td>

Script Includes with duplicate names

</td><td>

Manageability

</td><td>

X

</td><td>

Improved performance

</td></tr><tr><td>

HSD0001518

</td><td>

Check for manual indicators with no scores entered

</td><td>

Manageability

</td><td>

X

</td><td>

Improved performance

</td></tr><tr><td>

HSD0001554

</td><td>

JDBC Data Sources should have the "Use last run datetime" option checked

</td><td>

Performance

</td><td>

X

</td><td>

Altered script to look at import histories and focus only where a threshold number of records are 'ignored' and the DS lacks this setting

</td></tr><tr><td>

HSD0001556

</td><td>

For domain separated instances, admins should be at the top level domain instead of Global

</td><td>

Manageability

</td><td>

X

</td><td>

-   Altered script to  anonymize sys\_user findings
-   Added statistic in all cases

</td></tr><tr><td>

HSD0001560

</td><td>

Use 'track by' in ngRepeat loops

</td><td>

Performance

</td><td>

 

</td><td>

Improved performance

</td></tr><tr><td>

HSD0001600

</td><td>

Transform Script that run onBefore should not update\(\) or insert\(\) records on another table

</td><td>

Manageability

</td><td>

X

</td><td>

-   Definition updated to remove OOTB transform scripts from the findings
-   Recommendations for the HealthScan definition updated with a more detailed solution approach

</td></tr><tr><td>

HSD0001602

</td><td>

Number maintenance fields unique

</td><td>

Manageability

</td><td>

X

</td><td>

Exclude findings where the dynamic default value is used

</td></tr><tr><td>

HSD0001632

</td><td>

Long running \(slow\) scripts

</td><td>

Performance

</td><td>

X

</td><td>

Improved performance

</td></tr><tr><td>

HSD0001926

</td><td>

Specify group types

</td><td>

Manageability

</td><td>

X

</td><td>

Resolved potential false positives

</td></tr><tr><td>

HSD0002151

</td><td>

Use AngularJS services rather than window objects.

</td><td>

Performance

</td><td>

X

</td><td>

Improved performance

</td></tr><tr><td>

HSD0002198

</td><td>

Find credentials with few or no affinities

</td><td>

Performance

</td><td>

X

</td><td>

-   Retired duplicate  HSD0018256
-   Improved the recommendation
-   Provided documentation link

</td></tr><tr><td>

HSD0002258

</td><td>

Minimize cancelled discoveries

</td><td>

Manageability

</td><td>

X

</td><td>

Improved performance

</td></tr><tr><td>

HSD0002370

</td><td>

Setup SLAs for Case Management

</td><td>

Manageability

</td><td>

 

</td><td>

-   Changed short description
-   Document URL change

</td></tr><tr><td>

HSD0002415

</td><td>

Width of the Special Handling Notes pop-up window in pixels cannot be less than 300 pixels.

</td><td>

User Experience

</td><td>

 

</td><td>

Changed recommendation

</td></tr><tr><td>

HSD0002464

</td><td>

Inactive Knowledge Author

</td><td>

User Experience

</td><td>

X

</td><td>

Active published knowledge articles are now searched for inactive users

</td></tr><tr><td>

HSD0002473

</td><td>

Targeted Communications- Recipient List needs to be Refreshed

</td><td>

User Experience

</td><td>

 

</td><td>

Removed logic to check that recipient lists assigned to an active publication has been updated or refreshed

</td></tr><tr><td>

HSD0002513

</td><td>

Service Catalog- Maximum order quantity should not exceed 10

</td><td>

User Experience

</td><td>

X

</td><td>

Improved performance

</td></tr><tr><td>

HSD0002782

</td><td>

HR PDF Template with Published Document

</td><td>

Manageability

</td><td>

X

</td><td>

Improved performance

</td></tr><tr><td>

HSD0002791

</td><td>

Number, Opened, and Opened by should be populated by default scripts

</td><td>

Manageability

</td><td>

X

</td><td>

-   Included logic to check if the dynamic filter option is customized
-   Updated the findings to return only the specific record
-   Updated recommendation on the detailed action to be taken

</td></tr><tr><td>

HSD0002827

</td><td>

All events should have a description

</td><td>

Manageability

</td><td>

 

</td><td>

Implemented a simple check for pie.isBaseline\(\)

</td></tr><tr><td>

HSD0002834

</td><td>

The number of rules associated with an order guide should be kept to a minimum

</td><td>

Performance

</td><td>

X

</td><td>

-   Updated recommendation verbiage
-   Added statistic counter

</td></tr><tr><td>

HSD0004580

</td><td>

Knowledge Management Advanced plugin should be active.

</td><td>

User Experience

</td><td>

 

</td><td>

Improved performance

</td></tr><tr><td>

HSD0004581

</td><td>

Checklist should be configured with each &amp; every Knowledge Base.

</td><td>

User Experience

</td><td>

 

</td><td>

Improved performance

</td></tr><tr><td>

HSD0004602

</td><td>

Adoption of ATF Quick Start Test 'Communities'

</td><td>

Upgradeability

</td><td>

 

</td><td>

-   Corrected the finding link
-   Added active check is required in second glide to sys\_atf\_test table

</td></tr><tr><td>

HSD0004604

</td><td>

Adoption of ATF Quick Start Test 'Customer Service Base Entities'

</td><td>

Upgradeability

</td><td>

 

</td><td>

-   Corrected the finding link
-   Added active check is required in second glide to sys\_atf\_test table

</td></tr><tr><td>

HSD0004656

</td><td>

Adoption of ATF Quick Start Test 'Customer Service Management for Orders'

</td><td>

Upgradeability

</td><td>

 

</td><td>

Improved performance

</td></tr><tr><td>

HSD0004657

</td><td>

Adoption of ATF Quick Start Test 'Customer Service Request Integration'

</td><td>

Upgradeability

</td><td>

 

</td><td>

Improved performance

</td></tr><tr><td>

HSD0004658

</td><td>

Adoption of ATF Quickstart Test 'CSM Extension for Proxy Contacts'

</td><td>

Upgradeability

</td><td>

 

</td><td>

Improved performance

</td></tr><tr><td>

HSD0004659

</td><td>

Adoption of ATF Quickstart Test 'Major Issue Management'

</td><td>

Upgradeability

</td><td>

 

</td><td>

Improved performance

</td></tr><tr><td>

HSD0004660

</td><td>

Adoption of ATF Quickstart Test 'Skill Rule'

</td><td>

Upgradeability

</td><td>

 

</td><td>

Improved performance

</td></tr><tr><td>

HSD0004973

</td><td>

Check if system property- consumer\_max\_comments\_per\_case\_daily has been modified for consumer Cases attachment limit

</td><td>

Manageability

</td><td>

 

</td><td>

-   Improved performance
-   Corrected typo in  short description, description, and recommendation

</td></tr><tr><td>

HSD0006970

</td><td>

Percent of Active Hardware and VM Instance CIs processed via IRE

</td><td>

Manageability

</td><td>

 

</td><td>

 Improved performance

</td></tr><tr><td>

HSD0010608

</td><td>

Percent of Active HW CIs without Asset linkage

</td><td>

Manageability

</td><td>

 

</td><td>

Improved performance

</td></tr><tr><td>

HSD0012874

</td><td>

Install Base Items with Business Services

</td><td>

Manageability

</td><td>

 

</td><td>

Improved performance

</td></tr><tr><td>

HSD0012929

</td><td>

Install Base Items with Application Services

</td><td>

Manageability

</td><td>

 

</td><td>

Improved performance

</td></tr><tr><td>

HSD0001015

</td><td>

Reports should typically not be made public

</td><td>

Manageability

 

</td><td>

X

</td><td>

-   Enhancement in the query to validate if the system property glide.report.published\_reports.enabled is accounted for before reporting a finding
-   Baseline findings were removed

</td></tr></tbody>
</table>