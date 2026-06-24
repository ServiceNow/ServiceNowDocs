---
title: Capture Additional Data From Epic Within ServiceNow Record Producers
description: Update the variable values in existing record producers to capture tokenized data from Epic.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/healthcare-life-sciences/hco-update-variables-portal.html
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Embed Care Team Portal in Epic, Configure, Care Team Portal, Healthcare Operations, Healthcare and Life Sciences]
---

# Capture Additional Data From Epic Within ServiceNow Record Producers

Update the variable values in existing record producers to capture tokenized data from Epic.

## Before you begin

Role required: admin

## About this task

Record producers are used for case intake in the Care Team Portal. The variables on record producers are used to store data that is sent within the authorization token from Epic. A distinct format is used within the variables in a record producer to capture that data in ServiceNow. Use the out of box record producer titled "Report an EMR issue" as a foundational example for how to do this. To create additional record producers it's highly recommended to copy this Record Producer and the out of the box Catalog Client Scripts to ensure that the data in the authorization token from Epic is copied into the record producer. Variables can be created directly on the record producer or may be created within a variable set to apply across multiple record producers.

The value set in the "CONTEXT" field of the FDI record in Epic is what controls which data is sent from Epic to ServiceNow. For a full list of available data that can be sent from Epic as well as the contexts in which that data can be sent, refer to the Epic Token Library within Epic's product documentation.

## Procedure

1.  In the Record Producer, navigate to the **Variables** related list.

2.  Select **New**.

3.  Fill in fields as needed.

4.  Confirm that the name value of all variables begins with **sysparm\_** for any field in which you want to capture data coming from an EMR system.

5.  Select **Submit**.


