---
title: ATF Health Check checks and configuration
description: Look up all 14 ATF Health Check scans, understand what each check detects, and configure the modified-records threshold to fit your environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/atf-health-check-checks.html
release: brazil
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2026-09-18"
reading_time_minutes: 7
keywords: [ATF Health Check, instance scan, checks, automated test framework, performance, upgradability, manageability]
breadcrumb: [ATF Health Check, Automated Test Framework \(ATF\) test types and techniques, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# ATF Health Check checks and configuration

Look up all 14 ATF Health Check scans, understand what each check detects, and configure the modified-records threshold to fit your environment.

## ATF Health Check checks

ATF Health Check scans your instance for 14 common configuration issues organized across two suites:

-   ATF Core — 10 checks for core ATF features \(performance and upgradability\)
-   ATF Test Generator and Cloud Runner — 4 checks for the ATF Test Generator and Cloud Runner store app \(manageability and upgradability\)

Each check scans your instance and flags findings when issues are detected. Each finding links directly to the affected record so you can navigate and resolve the issue.

## ATF Core \(10 checks\)

These checks detect common performance and upgradability issues in your core ATF configuration. All checks are either Table Check or Script Only Check types and flag findings when conditions aren't met.

|Check Name|Type|What It Scans|Category|Finding Details|
|----------|----|-------------|--------|---------------|
|ATF Debug mode is not enabled|Table Check|System property: `sn_atf.debug`|Performance|Flags if property value is `true` \(debug mode is enabled, reducing performance\)|
|Avoid use of gs.sleep\(\) in Run Server Side Script steps|Table Check|Table: `sys_atf_step` filtered by step config = Run Server Side Script|Performance|Flags each step containing non-commented `gs.sleep(` calls in the script|
|Avoid use of gs.sleep\(\) in Custom Step Configs|Table Check|Table: `sys_atf_step_config`, field: `step_execution_generator`|Performance|Flags each custom step config containing non-commented `gs.sleep(` calls|
|ATF Tests with too many modified records|Table Check|Table: `sys_atf_test` \(active=true\), aggregates `sys_atf_modified_record_m2m` count per test|Performance|Flags tests where modified record count exceeds the configurable threshold \(default: 80\)|
|Single record modified by too many ATF Tests|Script Only Check|Aggregates `sys_atf_modified_record_m2m` grouped by record reference|Performance|Flags any single record modified by more than the threshold number of tests \(default: 80\)|
|ATF Glide Screenshots are not disabled|Table Check|System property: `sn_atf.screenshots.use_glide_screenshot`|Performance|Flags if property value is not `true` \(Glide screenshots are disabled, impacting test capability\)|
|ATF Full page screenshots are not enabled|Table Check|System property: `sn_atf.screenshots.capture_full_page`|Performance|Flags if property value is `true` \(full page screenshots are enabled, reducing performance\)|
|Do not exclude necessary ATF Tables during cloning|Table Check|Table: `clone_data_exclude`|Upgradability|Flags each of the 21 required ATF tables found in the clone exclusion list \(e.g., `sys_atf_test`, `sys_atf_step`, `sys_atf_step_config`, etc.\)|
|Reopen submitted form before UI validations|Table Check|Table: `sys_atf_test` \(active=true\), sequences test steps by order|Upgradability|Flags if a UI validation step runs when no form is open \(i.e., after a form submit without re-opening the form\)|
|ATF Tests start by creating or impersonating user|Table Check|Table: `sys_atf_test` \(active=true\), checks the first step \(step.order limit 1\)|Upgradability|Flags tests where the first step is neither an Impersonate step nor a Create User step with impersonate=true|

## ATF Test Generator and Cloud Runner \(4 checks\)

These checks validate the configuration and health of the ATF Test Generator and Cloud Runner store app. All checks only execute if plugin `sn_atf_tg` is active; if not active, the checks are automatically skipped.

|Check Name|Type|What It Scans|Category|Finding Details|
|----------|----|-------------|--------|---------------|
|Mutual Auth plugin is active|Script Only Check|Plugin: `com.glide.auth.mutual`, Property: `glide.authenticate.mutual.enabled`|Manageability|Flags if the Mutual Auth plugin is not active OR if the property is not `true`|
|Latest ATF Test Generator and Cloud Runner app is installed|Script Only Check|Table: `sys_store_app`, scope: `sn_atf_tg`|Manageability|Flags if the installed version of the Test Generator and Cloud Runner Store app is not the latest available version|
|ATF Instance has correct ADCV2 configuration|Script Only Check|REST request to: `{instanceURL}/adcv2/supports_tls`|Manageability|Flags if response status ≠ 200. Also flags if response body does not contain `true` \(inbound TLS not enabled\). Also flags if response header `server` does not contain `snow_adc` \(ADCV2 load balancer not in use\).|
|ATF Cloud User is set to valid user|Script Only Check|System property: `sn_atf_tg.username` to get configured cloud user; validates 9 user conditions|Upgradability|Flags if the cloud user does not exist, is inactive, is locked out, is web-services-only, is an internal integration user, has concurrent session limits, or needs password reset. Also flags if the user has `snc_read_only` role, lacks `admin` role, or has recent syslog errors.|

## Configuring the modified-records threshold

Two checks in the ATF Core suite measure how many records are modified by ATF tests:

-   ATF Tests with too many modified records: flags individual tests that modify too many records
-   Single record modified by too many ATF Tests: flags individual records modified by too many tests

Both checks use the same `sys_properties_list.do` configurable threshold system property.

<table id="table_fvh_hjn_rkc"><thead><tr><th>

Property

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Property Name

</td><td>

`sn_atf.scan.max_records_modified_by_test`

</td></tr><tr><td>

Type

</td><td>

Integer

</td></tr><tr><td>

Default Value

</td><td>

80

</td></tr><tr><td>

Read/Write Role

</td><td>

`admin`

</td></tr><tr><td>

Purpose

</td><td>

Sets the maximum threshold for the number of records modified by a single ATF test, or the maximum number of tests that can modify a single record. When either limit is exceeded, a finding is flagged by the respective check.For example, raise the threshold if 80 is too strict for your test suite design; lower it if you want scans to flag shared-data risk earlier.

</td></tr></tbody>
</table>## Resolving ATF Health Check issues

Review the following information to resolve the issues for ATF Health Check:

<table id="table_yr5_vln_rkc"><thead><tr><th>

Issue

</th><th>

What it means

</th><th>

Resolution options

</th></tr></thead><tbody><tr><td>

No findings appear when I run a scan

</td><td>

The scan ran successfully but detected no issues. Your ATF configuration meets the health check standards.

</td><td>

Check that all checks have a Pass status in the scan results

</td></tr><tr><td>

I ran the scan and got zero findings for the Test Generator and Cloud Runner suite

</td><td>

Checks for ATF Test Generator and Cloud Runner only run when the store app is active. If the app is not installed, an empty result for that suite is expected.

</td><td>

You can install and activate the ATF Test Generator and Cloud Runner store app to see the findings

</td></tr><tr><td>

Can a check’s script or condition be edited

</td><td>

No, all checks are delivered as read-only \(sys\_policy = read\).

</td><td>

If a check doesn't fit your environment, use Instance Scan's standard exclusion options to skip it in your scan runs.

</td></tr><tr><td>

Do these checks change anything on my instance?

</td><td>

No, every ATF Health Check only reads configuration and data to produce findings; none of them modify records.

</td><td>

You can manually resolve a finding.

</td></tr><tr><td>

Some checks are skipped or show "Not Applicable

</td><td>

The checks for ATF Test Generator and Cloud Runner suite only run if `sn_atf_tg` plugin is active. If the plugin is not active, those 4 checks are automatically skipped.

</td><td>

You can install and activate the ATF Test Generator and Cloud Runner store app plugin to execute its checks

</td></tr><tr><td>

Findings for "too many modified records"

</td><td>

Either a single test is modifying more than the threshold number of records, OR a single record is being modified by more than the threshold number of tests.

</td><td>

1.  Open the check finding to see which test or record is affected
2.  Review the specific test\(s\) or record\(s\) mentioned in the finding
3.  Consider refactoring the test\(s\) to modify fewer records, or decreasing the number of tests that modify that specific record
4.  Alternatively, adjust the threshold property `sn_atf.scan.max_records_modified_by_test` if your use case requires higher limits

</td></tr><tr><td>

Findings for excluded ATF tables during cloning

</td><td>

One or more essential ATF tables have been excluded from your clone configuration, which could cause issues when upgrading or cloning your instance.

</td><td>

1.  Open the check finding to identify which ATF tables are excluded
2.  Navigate to Clone Configuration Exclusions
3.  Remove the excluded ATF tables from the exclusion list
4.  Test your clone process after removing the exclusions

</td></tr><tr><td>

Findings for "Reopen submitted form before UI validations"

</td><td>

One of your ATF tests has a UI validation step that runs after a form has been submitted without being re-opened. This can cause the step to fail because the form is no longer open.

</td><td>

1.  Open the flagged test from the finding link
2.  Review the test steps in sequence to identify where the form is submitted
3.  After the Submit Form or Submit Record Producer step, add a step to reopen the form \(for example, Open Existing Record, Open New Form, Navigate Module, etc.\)
4.  Then add your UI validation step

</td></tr><tr><td>

Findings for "ATF Cloud User is set to valid user"

</td><td>

The cloud user configured in property `sn_atf_tg.username` does not meet one or more of the 9 required conditions for a valid ATF Cloud User.

</td><td>

1.  Open the finding to see which conditions aren't met
2.  Verify the user account exists and is active in your instance
3.  Confirm the user has the `admin` role and does NOT have the `snc_read_only` role
4.  Check that the user is not locked, does not need password reset, and has no concurrent session limits
5.  Review syslog for any errors associated with this user
6.  If the user can't be fixed, configure a different valid user in property `sn_atf_tg.username`

</td></tr><tr><td>

Findings for "ATF Instance has correct ADCV2 configuration"

</td><td>

Your instance does not have the correct ADCV2 configuration for the ATF Test Generator and Cloud Runner to function properly.

</td><td>

1.  Open the finding to see which specific condition\(s\) aren't met
2.  Verify that your instance is behind an ADCV2 load balancer \(ServiceNow ADCV2 service must be active\)
3.  Verify inbound TLS is enabled for your instance
4.  Contact ServiceNow support if ADCV2 configuration issues persist

</td></tr></tbody>
</table>**Parent Topic:**[ATF Health Check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/automated-test-framework-atf/atf-health-check-suites.md)

