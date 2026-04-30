---
title: Clone the access controls auditor suite
description: Clone and customize the default access controls auditor suite in your instance to create a new suite tailored to your organization's security practices.
locale: en-US
release: zurich
product: Security Center
classification: security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a scan suite, Scan suites, Security scanner, Security configuration console, Security Center, Platform Security]
---

# Clone the access controls auditor suite

Clone and customize the default access controls auditor suite in your instance to create a new suite tailored to your organization's security practices.

## Before you begin

Role required: admin

## About this task

The default access controls auditor suite provided with your instance can't be modified. However, if you want to add, remove, or edit checks to align with your organization's security practices, you can duplicate the access controls auditor suites. Copying the access controls auditor suites enables you to customize it and create a new suite based on the default one. The access controls auditor suites includes checks related to security best practices, covering system properties, plugins, and tables that impact the instance's security posture. The following steps demonstrate how to duplicate the default access controls auditor suites to tailor it to your organization's requirements.

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Suites**.

2.  Select **New** and enter a name for your suite, along with an optional description.

3.  Right-click the form header and select **Save**.

4.  Add the checks needed for your scan.

    1.  In the **Checks** tab, select **edit**.

    2.  Add the conditions.

        For example, to add scan checks apply the following fields, operators, values, and conditions:

        **\[Category\]\[is\]\[Security\] AND \[Application\]\[is\]\[Global\]**

        For example, it should look like the following: `Category is Security And Application is Global`.

5.  Select **run filter**.

6.  Select the scan checks that you want to add from the collection list to the check list, and then select the add \(&gt;\) button.

7.  Select **save**.

    The suite with your custom checks added have been created.

8.  Select **Execute Suite Scan**.


**Parent Topic:**[Create a scan suite](create-new-suite.md)

