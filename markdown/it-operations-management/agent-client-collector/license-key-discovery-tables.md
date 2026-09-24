---
title: License key discovery tables and configuration
description: License key discovery uses configuration tables to define file-matching rules and extraction parsers, and stores results in dedicated tables for reporting and reconciliation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/license-key-discovery-tables.html
release: brazil
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [license key discovery, configuration tables, results tables, file-based discovery]
breadcrumb: [ACC-VC reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# License key discovery tables and configuration

License key discovery uses configuration tables to define file-matching rules and extraction parsers, and stores results in dedicated tables for reporting and reconciliation.

## Configuration tables

Two configuration tables work together to define and execute the license key discovery framework.

## sn\_acc\_vis\_content\_license\_file\_config

Defines which files to treat as license files and which parser to invoke when a file is found.

|Column name|Type|Description|
|-----------|----|-----------|
|display\_name|String|Unique name identifying the rule.|
|file\_name|String|File name or partial name to match.|
|file\_name\_condition|Choice|How to match file\_name: `exact_match` \(default\), `starts_with`, `ends_with`, `contains`.|
|file\_extension|String|Optional file extension to further narrow the match \(no leading dot before the extension\).|
|parser|Reference|Reference to `sn_acc_vis_content_license_parser` record that processes matched files.|
|platform|Choice|Operating system\(s\) where the rule applies: `all` \(default\), `windows`, `linux`, `mac`.|
|order|Integer|Priority when multiple rules could match the same file \(default 100; lower values win\).|
|active|Boolean|Indicates whether the rule is currently in use \(default = **true**\).|

## sn\_acc\_vis\_content\_license\_parser

Holds the extraction logic for one license file format. A single parser can be referenced by multiple file-matching rules.

|Column name|Type|Description|
|-----------|----|-----------|
|parser\_name|String|Unique name identifying the parser.|
|parsing\_script|Script|Server-side JavaScript that reads file content and sets `answer` to an array of extracted results.|
|sample\_input|String|Representative file content used with Test Parser action.|
|sample\_output|String|Expected extraction result for sample\_input, used to validate the parser.|
|active|Boolean|Whether the parser is currently in use \(default = **true**\).|

## Results tables

Once a file has been scanned and parsed, the results flow through three tables, each holding a distinct stage of the outcome.

## sn\_acc\_vis\_content\_license\_file\_content

The raw, per-file result of scanning one file on one computer — captured regardless of whether a product match was later found.

|Column name|Type|Description|
|-----------|----|-----------|
|ci|Reference|Reference to `cmdb_ci_computer` — the computer where the file was found.|
|license\_file\_config|Reference|Reference to `sn_acc_vis_content_license_file_config` — the rule that matched this file.|
|file\_path|String|Folder path where the file was found.|
|file\_name|String|Name of the file.|
|file\_size|Long Integer|Size of the file in bytes.|
|file\_version|String|File version, if available.|
|discovered\_product\_name|String|Product name extracted by the parser.|
|discovered\_vendor|String|Vendor name extracted by the parser.|
|discovered\_license\_key|String|License key extracted by the parser.|
|discovered\_expiry\_date|Date|Expiry date extracted by the parser, if present in the file.|
|discovered\_file\_content|Long Text|Raw file content, stored only when parsing fails \(for troubleshooting\).|
|scan\_id|String|Identifier of the scan that produced this result.|
|last\_scanned|Date|When this file was last scanned.|
|parse\_status|Choice|`parsed` or `parse_failed`.|
|absent|Boolean|Set to **true** when the file is no longer found in a later scan \(default = **false**\).|

## sn\_acc\_vis\_content\_license\_keys

The final, resolved license key tied to a computer and a recognized software product — the table which is reported on.

|Column name|Type|Description|
|-----------|----|-----------|
|ci|Reference|Reference to `cmdb_ci` — the computer the license key belongs to.|
|product|Reference|Reference to `samp_sw_product` — the matched catalog product.|
|user|Reference|Reference to `sys_user` — user associated with the CI, if resolved.|
|license\_file\_config|Reference|Reference to `sn_acc_vis_content_license_file_config` — the rule that led to this result \(file-method only\).|
|license\_file\_path|String|Path of the source license file \(file-method only\).|
|license\_key|String|The resolved license key.|
|last\_scanned|Date|When this license key was last confirmed.|
|absent|Boolean|Set to **true** when no longer found in a later scan \(default = **false**\).|

**Note:** Columns `license_key_config` and `resolved_registry_path` also exist on this table but are populated only by the older registry-based discovery method.

## sn\_acc\_vis\_content\_license\_file\_unresolved

A holding area for discovered product names that could not be automatically matched to the software catalog.

|Column name|Type|Description|
|-----------|----|-----------|
|discovered\_product\_name|String|Product name as extracted by the parser \(unmatched\).|
|discovered\_vendor|String|Vendor name as extracted by the parser.|
|parser|Reference|Reference to `sn_acc_vis_content_license_parser` — the parser that produced this discovery.|
|normalised\_product\_name|Reference|Reference to `samp_sw_product` — set by the customer to manually map this discovery to a real catalog product.|

## Framework constraints

The following constraints are built into the framework:

-   **File read permission** — The account under which the ACC agent service runs must have read permission on the folders and files being scanned. This is an operating-system-level requirement. If the agent encounters a file or folder it cannot read, it logs a permission error for that item and continues scanning.
-   **File size limit** — License file content is capped at 1 MB. Files larger than this limit are skipped and not read for license key extraction.

These constraints are intentional guardrails and cannot be changed through configuration.

## Product reconciliation

Once a parser successfully extracts a product name from a license file, the discovery is reconciled against the software catalog \(`samp_sw_product`\). If a confident match is found, a final record is created in `sn_acc_vis_content_license_keys`. If no confident match is possible, the discovery is placed in `sn_acc_vis_content_license_file_unresolved` for manual review and mapping.

Manual mappings are performed only once per unique product name. After a customer sets the **normalised\_product\_name** field, all future scans reporting the same discovered product name resolve automatically with no repeated manual effort.

## System properties and policies

|Component|Role|
|---------|----|
|System property `sn_acc_vis_content.enable_license_key_discovery`|Master on/off switch \(default = **false**\). Must be **true** for license key data from either discovery method to be processed and stored.|
|Policy `File Based Discovery Policy - License Key`|Instructs the agent during its regular file-scanning activity to watch for files matching an active License File Configuration rule. Depends on the File Based Discovery Background Policy also being active.|
|Check definition `File Based Discovery - License Key`|Defines the concrete agent command executed \(files.rb --compact --no-delta, scoped to the license-key scan identifier\) and its timeout \(10 minutes\)|

**Parent Topic:**[Agent Client Collector for Visibility Content reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/agent-client-collector-for-visibility-references.md)

