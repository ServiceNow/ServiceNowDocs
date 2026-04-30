---
title: Configure the Recommended for you
description: The Recommended for you widget displays catalog items and knowledge articles, enabling you to view information that is most relevant to you based on the taxonomy.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Recommended for you, Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Configure the Recommended for you

The Recommended for you widget displays catalog items and knowledge articles, enabling you to view information that is most relevant to you based on the taxonomy.

## Before you begin

Role required: sp\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Administration** &gt; **Portal configuration**.

2.  Edit the portal to suit your needs.

    For more information on the portal form fields and description, see [Create a portal](https://www.servicenow.com/docs/access?context=create-a-portal&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

3.  Map the **Taxonomy** that you created or use the default **Employee** taxonomy at the portal level.

    For more information on taxonomy, see [Unified Taxonomy for Employee Center](../concept/config-taxonomy.md).

4.  Navigate to **System Definition** &gt; **Fix Scripts**.

    1.  Search for **Set primary topics for Employee taxonomy script**.

    2.  Run the script manually to update the **taxonomy\_topic** field for the articles and catalog items associated to the employee taxonomy.


## Result

The script fixes the **Recommended for you** and search, if Employee taxonomy is associated to the portal. Updates the taxonomy\_topic column in the knowledge articles and catalog items to the corresponding mapping found in m2m\_connected\_content table.

From the content associated to the taxonomy, most viewed or recommended articles or catalog items are fetched and displayed to the employee.

## What to do next

You can proceed to configure the instance options to control the appearance of the widget, see [Modify the Recommended for you widget display](config-recommended-for-you.md)

