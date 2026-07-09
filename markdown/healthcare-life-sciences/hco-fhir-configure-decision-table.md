---
title: Configure the organization classification decision table
description: Edit the decision table that classifies imported FHIR Organizations as internal or external business locations, so that the classification matches how your organization defines internal and external entities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-fhir-configure-decision-table.html
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 1
keywords: [decision table, business location, organization type]
breadcrumb: [Prerequisites for the FHIR integration, EMR Provider Directory Sync, Healthcare Integrations, Healthcare and Life Sciences]
---

# Configure the organization classification decision table

Edit the decision table that classifies imported FHIR Organizations as internal or external business locations, so that the classification matches how your organization defines internal and external entities.

## Before you begin

Role required: `sn_hco_intg_fhir.admin`.

## About this task

When the integration imports a FHIR Organization, it uses a decision table named `FhirOrgTypeToBusinessLocationClass` to decide whether to create an internal or external business location, based on the organization type. By default, the organization types `pay`, `pharma`, `crs`, `govt`, `edu`, `reli`, `cg`, and `bus` are classified as external; all other types default to internal. You can edit these rules without changing code.

## Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Decision Tables**.

2.  Open the **FhirOrgTypeToBusinessLocationClass** decision table.

3.  Add or edit rules to map each organization type to **internal** or **external**.

    For example, to classify provider organizations \(`prov`\) as external, add a rule: if **org\_type** is `prov`, then **business\_location\_class** is `external`.

4.  Save the decision table.


## Result

The updated classification applies on the next sync run.

