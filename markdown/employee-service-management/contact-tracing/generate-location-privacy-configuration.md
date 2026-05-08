---
title: Generate location-based privacy configurations for Contact Tracing
description: As an administrator, generate the privacy configuration for locations set up in your instance.
locale: en-US
release: australia
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up data privacy consent settings for Contact Tracing, Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Generate location-based privacy configurations for Contact Tracing

As an administrator, generate the privacy configuration for locations set up in your instance.

## Before you begin

The privacy statement in the default template is copied in each location's privacy configuration. Ensure that you have reviewed the privacy statement in the default consent template and modified it if necessary.

Role required: sn\_imt\_tracing.admin

## About this task

You can generate a location-based, default privacy configuration for each country available in the Locations \[cmn\_location\] table. For each location, you can specify whether the privacy consent is required and update the privacy policy statement.

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Privacy** &gt; **Location Privacy Configuration**.

2.  Click **Generate Location Configurations**.

    The default configuration is created for each country and appears in the Location Privacy Configurations list.

3.  Open a location to review its configuration and modify it if necessary.

4.  Configure the privacy consent text if necessary.

<table id="choicetable_w2c_2lg_gmb"><thead><tr><th align="left" id="d404262e101">

Privacy consent status

</th><th align="left" id="d404262e104">

Action

</th></tr></thead><tbody><tr><td id="d404262e110">

**Consent is not required for the location**

</td><td>

Clear the **Needs privacy consent** check box.

</td></tr><tr><td id="d404262e122">

**Consent is required for the location**

</td><td>

Determine the privacy consent text.-   If you have defined a specific privacy consent template to assign to this location, select it from the **Privacy consent template**.

The privacy statement content from the updated template is copied in the **Privacy statement** field.

-   Retain the default privacy statement text and make any modifications.


</td></tr></tbody>
</table>5.  Click **Update**.


## Result

The location-based privacy configuration is set.

## What to do next

[Configure an email notification for a privacy consent request](configure-privacy-email.md).

**Parent Topic:**[Setting up data privacy consent settings for Contact Tracing](../concept/set-up-privacy-consent-settings.md)

