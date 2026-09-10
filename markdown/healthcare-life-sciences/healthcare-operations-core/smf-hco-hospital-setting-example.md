---
title: Example: Service Model Foundation in a hospital setting
description: See how Service Model Foundation \(SMF\) tables for healthcare organizations and locations come together for a real hospital system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/healthcare-operations-core/smf-hco-hospital-setting-example.html
release: australia
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 5
breadcrumb: [Organizations and locations overview, Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Example: Service Model Foundation in a hospital setting

See how Service Model Foundation \(SMF\) tables for healthcare organizations and locations come together for a real hospital system.

## The scenario

Riverside Health System operates one flagship hospital, Riverside General Hospital, which includes a Cardiology department and a Biomedical Engineering team that repairs and maintains clinical equipment. Riverside Health System also has an affiliate practice, Lakeside Family Practice, whose clinicians log in to Riverside's Epic environment through Epic Community Connect to report EMR issues.

The following sections show the records that this scenario creates across the Service Model Foundation \(SMF\) tables, from the internal hierarchy down to a sample case.

**Note:**

This example doesn't show sample records for **Business Organization**, **Organization Core**, or **common location** \[cmn\_location\].

Business Organization and Organization Core are extension ancestors of Internal Organization and External Organization, not tables you populate directly. Every Internal Organization or External Organization record created in this scenario already exists as a row in both of those parent tables through table extension. It's not a separate record you author, so no sample row is shown for them here. For more information, see the important note in [Understanding Service Model Foundation in Healthcare Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/healthcare-operations-core/understanding-service-model-foundations-hco.md).

Common location only enters the picture once address data is added to a Business Organization record, through the process described in "Importing location data" in [Understanding Service Model Foundation in Healthcare Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/healthcare-operations-core/understanding-service-model-foundations-hco.md). This scenario doesn't introduce address data, so no common location record is created.

## Internal Organization records

Riverside Health System, Riverside General Hospital, the Cardiology department, and the Biomedical Engineering team are all internal to Riverside, so each is represented as an Internal Organization record. The Parent Organization field builds the hierarchy between them.

|Record name|Parent Organization|Notes|
|-----------|-------------------|-----|
|Riverside Health System|—|Top of the hierarchy; no parent.|
|Riverside General Hospital|Riverside Health System|The flagship hospital.|
|Riverside General Hospital – Cardiology|Riverside General Hospital|A department within the hospital; the requesting service org on the sample case.|
|Riverside General Hospital – Biomedical Engineering|Riverside General Hospital|A department within the hospital; the supporting service org on the sample case.|

## External Organization

Lakeside Family Practice is external to Riverside, so it's represented as an External Organization record rather than an internal one. Because its clinicians report EMR issues through Epic Community Connect, it also requires the corresponding membership setup.

|Record name|Parent Organization|Notes|
|-----------|-------------------|-----|
|Lakeside Family Practice|Riverside Health System|Affiliate practice; members of that practice require an membership to the external organization.|

## Healthcare organization profiles

Each Business Organization record in this scenario has a linked healthcare organization record that stores its healthcare-specific profile fields, such as organization type. The healthcare organization hierarchy mirrors the Business Organization hierarchy, but the two are separate tables connected one-to-one.

|Healthcare organization|Organization type|Linked Business Organization|
|-----------------------|-----------------|----------------------------|
|Riverside Health System|Provider|Riverside Health System \(internal\)|
|Riverside General Hospital|Provider|Riverside General Hospital \(internal\)|
|Riverside General Hospital – Cardiology|Provider|Riverside General Hospital – Cardiology \(internal\)|
|Riverside General Hospital – Biomedical Engineering|Provider|Riverside General Hospital – Biomedical Engineering \(internal\)|
|Lakeside Family Practice|Provider|Lakeside Family Practice \(external\)|

**Note:**

Each healthcare organization record here shares a name with its linked Business Organization record, but they're two different tables. The healthcare organization stores the profile fields and reporting hierarchy; the Business Organization record remains the record that's referenced elsewhere, such as on the case.

## Healthcare locations

Healthcare locations represent the physical spaces within Riverside General Hospital, down to the Cardiology unit. The healthcare organization location association table then links the Cardiology healthcare organization to the Cardiology unit, determining which common locations that care team is responsible for.

|Record name|Physical type|Parent location|
|-----------|-------------|---------------|
|Riverside Campus|Campus|—|
|Riverside General Hospital Building|Building|Riverside Campus|
|3 West – Cardiology Unit|Unit|Riverside General Hospital Building|

A healthcare organization location association record links the Riverside General Hospital – Cardiology healthcare organization to the 3 West – Cardiology Unit healthcare location, so care team members in Cardiology only see common locations within that unit when they report an issue.

## A sample case

A clinician in the Cardiology unit reports that a vital signs monitor in room 3W-204 is unresponsive. The resulting case is populated as follows:

|Field|Value|
|-----|-----|
|Requesting service org|Riverside General Hospital – Cardiology \(the Internal Organization record, not the Cardiology healthcare organization\)|
|Supporting service org|Riverside General Hospital – Biomedical Engineering \(the Internal Organization record that fulfills the case\)|
|Short description|Vital signs monitor in room 3W-204 is unresponsive.|

Because requesting service org points to the Internal Organization record, out-of-box case visibility works correctly for everyone in the Cardiology unit. If this field pointed to the Cardiology healthcare organization instead, shared visibility wouldn't apply, since the healthcare organization is a profile record rather than the requesting organization.

Supporting service org identifies Biomedical Engineering as the fulfiller, but it doesn't drive shared case visibility the way requesting service org does. That field isn't used in every SMF implementation, and Riverside populates it here only because it has a dedicated team that fulfills equipment cases.

## What happens if requesting service org points to the wrong record

Suppose Riverside's admin had configured the case differently: instead of setting requesting service org to Riverside General Hospital – Cardiology, they set it to the Cardiology healthcare organization, since that's the record most setup documentation focuses on. The case still saves. Every field is populated. The work order to Biomedical Engineering still generates.

But shared visibility depends on requesting service org pointing to the Business Organization record, not the healthcare organization. Because the healthcare organization is a profile record rather than a Business Organization record, none of the other members of the Cardiology unit can see the case. The charge nurse's case list stays empty. No one on shift knows the monitor in room 3W-204 is down until someone walks over and finds it dead. A nurse spends part of the shift hunting the floor above for a spare monitor; by the time it's found, another nurse who needed it has already carried it off to a different room. The unit loses time that should have gone to patients, not because Biomedical Engineering failed to fulfill the case, but because no one except the reporting nurse ever knew there was a case to look at.

Nothing in this scenario failed loudly. The case existed, the fields were filled in, and the work order ran. The only difference from the working example above is a single field pointing at a profile record instead of a Business Organization record, and that's enough to silently break the shared visibility the requesting service org field exists to provide.

