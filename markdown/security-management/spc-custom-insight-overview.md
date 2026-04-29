---
title: Key insights and configured insights for Security Posture Control
description: Key and configured \(custom\) insights provide you with visual reports that are created and updated by the assessment criteria that match your assets. Insights help you monitor security controls metrics on a dashboard.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Security Posture Control, Security Operations]
---

# Key insights and configured insights for Security Posture Control

Key and configured \(custom\) insights provide you with visual reports that are created and updated by the assessment criteria that match your assets. Insights help you monitor security controls metrics on a dashboard.

## Key insights

The criteria used for the assessments of your assets are provided by the policies that are included with the application.

-   Key insights use the policies that are included with the application.
-   Configured insights can be created using the policies included with the application, your own custom policies, or a combination of both.

On the Home \(landing page\) in the Security Posture Control workspace, the Key insights section below the Overview displays visual reports that are created and updated by the policies that are included with the application. These insights are also included with the application and display the following information:

-   Endpoint protection agent installed: Total number of assets that have or do not have endpoint protection.
-   Managed device coverage: Number of managed assets compared to those that are unmanaged.
-   Vulnerability scan coverage: Total number of scanned assets compared to the those that are not scanned for known vulnerabilities by a third-party vulnerability scanner.
-   Assets with critical vulnerabilities: Number of assets out of the total number of assets that have critical vulnerabilities.
-   Vulnerable items by criticality: Total number of vulnerable items broken down by their severity. A known vulnerability that matches an asset in your CMDB results in a vulnerable item. This insight requires you to install the Vulnerability Response application and at least one scanner integration: Qualys, Rapid7, or the Tenable Vulnerability Integration. All these applications are available on the ServiceNow® Store.
-   Top 3 policies by findings: Policies that return the most findings \(matches\) on your assets.

## Configured insights

You can create your own insights if you want more information not found in the Key insights. You can create these configured insights and use existing policies or your own custom policies for assessment. Your configured insights are displayed on the Configured insights dashboard module, the second icon from the top in the workspace.

Following types of insights can be configured.

-   Comparison chart: Compare results between multiple policies with bar charts.
-   Policy match count widget: View the number of devices that match a policy.
-   Policy match percentage chart: View the percentage of devices that match a policy in a pie chart. You can choose the total asset pool as either all the assets monitored by SPC or the assets that match the base policy from which the current selected policy is created.
-   Policy trend chart: View the trends of assets that match various policies.

See [Create and activate a configured insight for Security Posture Control](../task/spc-create-custom-insight.md) for more information about the steps for creating a configured insight.

## Groups

You must create or assign groups to your configured insights when you create new records in the Custom insight builder module. Groups allow you to organize your reports on the Configured insights dashboard.

Insights can be organized into groups. Each group can have 21 widgets or insights.

