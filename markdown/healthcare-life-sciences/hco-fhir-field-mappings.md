---
title: FHIR-to-HCLS field mappings
description: For each of the four FHIR R4 resources, the Healthcare Operations HL7 FHIR Integration maps FHIR fields to Healthcare Operations target tables and upserts records — matching the primary HCLS record on the FHIR resource ID \(stored as an external identifier\) and related records on their natural keys.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-fhir-field-mappings.html
release: australia
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [field mapping, FHIR, HCLS, upsert]
breadcrumb: [EMR Provider Directory Sync, Healthcare Integrations, Healthcare and Life Sciences]
---

# FHIR-to-HCLS field mappings

For each of the four FHIR R4 resources, the Healthcare Operations HL7 FHIR Integration maps FHIR fields to Healthcare Operations target tables and upserts records — matching the primary HCLS record on the FHIR resource ID \(stored as an external identifier\) and related records on their natural keys.

Each resource's primary record is matched by its FHIR logical ID, stored as `external_id` on the Healthcare \(HCLS\) Organization, Location, and Practitioner tables. Related records that have no `external_id` column — business locations, users, and service organization memberships — are matched on their natural keys instead. The tables below summarize the principal field mappings; some fields are populated on related platform tables as a side effect of the upsert.

Some FHIR data is intentionally not mapped in this release: practitioner NPI and other identifiers \(the FHIR logical ID serves as the external identifier\), and PractitionerRole role codes and specialties.

## Organization

FHIR Organizations upsert into `sn_hcls_organization` and, based on the organization classification decision table, into either `sn_csm_business_location_internal` or `sn_csm_business_location_external`.

|FHIR field|Target field|Notes|
|----------|------------|-----|
|id|`sn_hcls_organization.external_id`|Upsert key.|
|name|`sn_hcls_organization.name`|Required; the record is skipped if it is missing.|
|type|`sn_hcls_organization.org_type`|Defaults to `other` if missing or unrecognized. Drives the internal/external business location classification.|
|partOf|`sn_hcls_organization.parent`|Resolved to a parent organization by external ID. One level of missing parent is recovered; deeper hierarchy gaps are logged.|
|address, telecom|Business location address and contact fields|Written to the internal or external business location record.|

## Location

FHIR Locations upsert into `sn_hcls_location` and the platform `cmn_location` table, and optionally create an organization-location association.

|FHIR field|Target field|Notes|
|----------|------------|-----|
|id|`sn_hcls_location.external_id`|Upsert key.|
|name|`sn_hcls_location.name`, `cmn_location.name`|Required.|
|status|`sn_hcls_location.status`|Maps directly \(active, suspended, inactive\).|
|physicalType|`sn_hcls_location.physical_type`|Mapped where a matching HCLS value exists; left empty otherwise.|
|address, position|`cmn_location` address and coordinate fields|The platform location is anchored to the HCLS location.|
|partOf|`sn_hcls_location.parent_location`, `cmn_location.parent`|Resolved by external ID, with one level of parent recovery. The parent is set on both the Healthcare Location and the platform location.|
|managingOrganization|`sn_hcls_organization_location_association`|Creates the association if the organization resolves; otherwise the association is skipped and logged, and the location still upserts.|

## Practitioner

FHIR Practitioners upsert into `sn_hcls_practitioner` and the platform `sys_user` table, and each practitioner is granted the care-team-member role.

|FHIR field|Target field|Notes|
|----------|------------|-----|
|id|`sn_hcls_practitioner.external_id`|Upsert key.|
|telecom \(email\)|`sys_user.user_name`, `sys_user.email`|Required; normalized and used to match or create the user. Practitioners without an email are skipped.|
|name \(given, family, prefix, suffix, text\)|Practitioner and user name fields|Given name defaults to `Unknown` if missing, and the run is marked Completed with errors.|
|gender|`sn_hcls_practitioner.gender`|Mapped to HCLS values; defaults to not-disclosed if missing or unknown.|
|birthDate, telecom \(phone\), address, active|Corresponding practitioner and user fields|Imported users have login enabled; admins set credentials separately.|
|\(role grant\)|`sys_user_has_role`|Each practitioner is granted the `sn_hco.care_team_member` role.|

## PractitionerRole

FHIR PractitionerRoles upsert into `sn_csm_service_organization_member` and `sn_csm_svc_org_member_responsibility`, placing a practitioner on a care team for an organization.

|FHIR field|Target field|Notes|
|----------|------------|-----|
|practitioner.reference|`sn_csm_service_organization_member.user`|Resolved through the Healthcare Practitioner record to the user. The role is skipped if the practitioner is not found.|
|organization.reference|`sn_csm_service_organization_member.service_organization`|Resolved through the Healthcare Organization to its business location. The role is skipped if the organization is not resolvable.|
|\(responsibility\)|`sn_csm_svc_org_member_responsibility.type`|Set to the Care Team Member responsibility for every imported role.|
|code, specialty|Not mapped|FHIR role codes and specialties are not captured in this release.|
|location|Not used|The role's location array is not used to infer organization membership.|

