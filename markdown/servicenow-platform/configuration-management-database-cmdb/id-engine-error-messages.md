---
title: IRE error messages
description: The Identification and Reconciliation Engine \(IRE\) generates the following errors and messages. Depending on settings, these messages appear in the Identification Logging pane and in the system logs.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Reference, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# IRE error messages

The Identification and Reconciliation Engine \(IRE\) generates the following errors and messages. Depending on settings, these messages appear in the Identification Logging pane and in the system logs.

For information about lookup-based CI identification and qualifier chains, see [Create a CI identification rule](../task/t_CreateCIIdentificationRule.md).

**Note:** IRE performs an initial verification of a payload before processing identification rules. If IRE detects any duplicate CIs based on any class identifiers, the payload is rejected and processing stops.

For information about CMDB Identification Payload error: "FAILED TRYING TO EXECUTE ON CONNECTION", see [CMDB Identification Payload error - "Insertion failed with error Error during insert of cmdb\_ci...", where node logs show "FAILED TRYING TO EXECUTE ON CONNECTION" "Duplicate entry 'XXX' for key 'XXX'"](https://support.servicenow.com/kb_view.do?sysparm_article=KB0812609) knowledge base article.

## Error- IDENTIFICATION\_RULE\_MISSING

<table id="table_k1v_mml_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Identity Rule Missing for table \[xyz\]

</td><td>

-   **Description:**

Identification rule is missing for a class.

-   **Resolution:**

Ensure that there is an identification rule for table \[xyz\], and that the rule is active.


</td></tr></tbody>
</table>## MISSING\_MATCHING\_ATTRIBUTES

<table id="table_zz3_lbj_h1b"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

In payload missing minimum set of input values for criterion \(matching\) attributes from identify rule for table \[xyz\]. Add these input values in payload item 'abc'

</td><td>

-   **Description:**

Missing minimum set of values for criterion attributes for an identification rule.

-   **Resolution:**

In the payload, add minimum set of values for criterion attributes for CI Identifier for table \[xyz\]. Open the [CI Class Manager](../task/t_CreateCIIdentificationRule.md), click **Hierarchy** and select the \[xyz\] class. Check the identification rule and the identifier entries for table \[xyz\].


</td></tr></tbody>
</table>## Error- NO\_CLASS\_NAME\_FOR\_INDEPENDENT\_CI

<table id="table_kyc_nml_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Cannot have 'sys\_class\_name' as a key field in an Independent Identity Rule on 'xyz'

</td><td>

-   **Description:**

The class attribute was added to the CI identifier which is not supported.

-   **Resolution:**

Remove the class attribute from CI Identifier for table \[xyz\].


</td></tr></tbody>
</table>## Error- IDENTIFICATION\_RULE\_FOR\_LOOKUP\_MISSING

<table id="table_cjk_nml_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Identity Rule for table \[xyz\] missing Lookup Rule for class \[abc\]

</td><td>

-   **Description:**

The payload has a lookup class name, but the corresponding lookup rule is missing.

-   **Resolution:**

Add lookup identifier entry with \[Search on table\] as \[abc\] for CI Identifier for table \[xyz\].


 For more information about this error message, see [Identification error "Identity Rule for table \[cmdb\_ci\_table\_name\] missing Lookup Rule for class \[table\_name\]" \[KB0786444\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB0786444).

</td></tr></tbody>
</table>## Error- IDENTIFICATION\_RULE\_FOR\_RELATED\_ITEM\_MISSING

<table id="table_zhw_3nl_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Identity Rule for table \[xyz\] missing Related Rule for class \[abc\]

</td><td>

-   **Description:**

The payload has a related class name, but the corresponding related rule is missing.

-   **Resolution:**

Add related entry with \[Related table\] as \[abc\] within CI Identifier for table \[xyz\].


</td></tr></tbody>
</table>## Error- NO\_LOOKUP\_RULES\_FOR\_DEPENDENT\_CI

<table id="table_mxb_jnl_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Cannot have Lookup Rule for a Dependent Identity Rule on 'xyz'

</td><td>

-   **Description:**

Cannot have Lookup Rule for a Dependent Identity Rule.

-   **Resolution:**

Remove lookup identifier entry from dependent CI Identifier for table \[xyz\].


</td></tr></tbody>
</table>## Error- INVALID\_INPUT\_DATA

<table id="table_bff_jnl_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Found invalid sys\_id in payload. No record with sys\_id \[xyz\] exist in table \[abc\] or is a duplicate record with \[duplicate\_of\] field set to a main CI

</td><td>

-   **Description:**

The payload has a reference to an invalid sys\_id.

-   **Resolution:**

Remove the referenced sys\_id, or provide a valid sys\_id.


</td></tr><tr><td>

In payload no data source exist. You need to provide choice value from choice field \[discovery\_source\] in table \[cmdb\_ci\]

</td><td>

-   **Description:**

In payload no data source exists.

-   **Resolution:**

In the payload, provide a valid choice value from choice field \[discovery\_source\] from table \[cmdb\_ci\].


</td></tr><tr><td>

In payload invalid data source \[xyz\] exist. You need to provide a valid choice value from field \[discovery\_source\] in table \[cmdb\_ci\]

</td><td>

-   **Description:**

The payload contains an invalid data source.

-   **Resolution:**

In the payload, provide a valid choice value from choice field \[discovery\_source\] from table \[cmdb\_ci\].


</td></tr><tr><td>

No such relationship with name \[xyz\] exist in table \[cmdb\_rel\_type\]. If out-of-box relationship for \[xyz\] has been removed or renamed, it should be restored

</td><td>

-   **Description:**

The payload is referencing a relationship that does not exist in the \[cmdb\_rel\_type\] table.

-   **Resolution:**

Verify that the reference to the relationship is accurate. Or, if it is a new relationship, add it to the \[cmdb\_rel\_type\] table. Or, If out-of-box relationship for \[xyz\] has been removed or renamed, restore it.


</td></tr><tr><td>

Payload relations 'xyz' has invalid parent record index: \[0\]

</td><td>

-   **Description:**

Payload references invalid parent indexes.

-   **Resolution:**

Check payload indexes and ensure that they are all valid.


</td></tr><tr><td>

Payload relations 'xyz' has invalid child record index: \[0\]

</td><td>

-   **Description:**

Payload references invalid child indexes.

-   **Resolution:**

Check payload indexes and ensure that they are all valid.


</td></tr></tbody>
</table>## Error- DUPLICATE\_RELATIONSHIP\_TYPES

<table id="table_tbl_jnl_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Duplicate relationship type records exists with name \[xyz\] in table \[cmdb\_rel\_type\] having sys\_ids: \[abc\]

</td><td>

-   **Description:**

There are duplicate records in the \[rel\_ci\_type\] table for the relationship.

-   **Resolution:**

Remove the duplicate records.


</td></tr></tbody>
</table>## Error- DUPLICATE\_PAYLOAD\_RECORDS

<table id="table_jww_cpl_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Found duplicate items in the payload \(index 0 and 1\), using className \[xyz\] and fields \[abc\]. Remove duplicate items from payload

</td><td>

-   **Description:**

The payload contains two items whose criterion attributes have identical values.

-   **Resolution:**

Remove one of the duplicate items.


</td></tr></tbody>
</table>## Error- LOCK\_TIMEOUT

<table id="table_y2j_2pl_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Failed to acquire synchronization lock for xyz

</td><td>

-   **Description:**

Failed to acquire the system mutex lock.

-   **Resolution:**

Increase the mutex expiration time by adding the system property **glide.identification\_engine.mutex\_expiration\_time** and setting to an integer value that is greater than the default value \(15 min\).


</td></tr></tbody>
</table>## Error- MULTIPLE\_DUPLICATE\_RECORDS

<table id="table_zjm_2pl_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Found duplicate records in table \[xyz\] using fields \[abc\]

</td><td>

-   **Description:**

Found duplicate records in the specified table.

-   **Resolution:**

Fix the duplicate records found by the identification engine. Check de-duplication tasks for information about all duplicates.


</td></tr></tbody>
</table>## Error- REQUIRED\_ATTRIBUTE\_EMPTY

<table id="table_apq_2pl_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Missing mandatory field \[xyz\] in table \[abc\]. Add input value for mandatory field in payload

</td><td>

-   **Description:**

A required attribute is missing in the payload.

-   **Resolution:**

In the payload, add input value for mandatory field \[xyz\] in table \[abc\].


</td></tr></tbody>
</table>## Error- MISSING\_DEPENDENCY

<table id="table_wgv_2ql_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

In payload no relations defined for dependent class \[xyz\] that matches any containment/hosting rules: \[abc\]. Add appropriate relations in payload for 'def'

</td><td>

-   **Description:**

No relations defined for the dependent class that matches any of its metadata rules.

-   **Resolution:**

In payload add appropriate relations for dependent class \[xyz\] that matches any containment/hosting rules: \[abc\].


</td></tr></tbody>
</table>## Error- METADATA\_RULE\_MISSING

<table id="table_e5y_pf2_5z"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

No containment or hosting rules defined for dependent class \[xyz\]. Add containment/hosting rules for ‘abc'

</td><td>

-   **Description:**

There are no containment or hosting rules defined for dependent class.

-   **Resolution:**

Add containment or hosting rules for dependent class \[xyz\].


</td></tr></tbody>
</table>## Error- MULTIPLE\_DEPENDENCIES

<table id="table_c2x_fql_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Found multiple dependent relation items \[xyz\] and \[abc\] in payload

</td><td>

-   **Description:**

Multiple dependent relation items exist.

-   **Resolution:**

Remove one of the multiple dependent relation items \[xyz\] or \[abc\].


</td></tr><tr><td>

Multiple paths leading to the same destination: xyz -&gt; abc

</td><td>

-   **Description:**

Multiple paths leading to the same destination.

-   **Resolution:**

Remove duplicate relationship/qualifier chains that might exists between xyz -&gt; abc.


</td></tr></tbody>
</table>## Error- ABANDONED

<table id="table_w1c_gql_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Abandoning processing payload item 'xyz', since its depends on payload item 'abc' has errors

</td><td>

-   **Description:**

Dependent payload item has errors, so abandoning processing.

-   **Resolution:**

Resolve the error on the dependent payload item ‘abc'.


</td></tr><tr><td>

Can't find matched record with sys\_id \[xyz\] in table \[abc\]

</td><td>

-   **Description:**

Matched sys\_id does not exist in the corresponding table.

-   **Resolution:**

Check in table \[abc\] whether matched record is a valid record based on input payload.


</td></tr><tr><td>

Identification engine API got called recursively, aborting...

</td><td>

-   **Description:**

The Identification engine API was called recursively.

-   **Resolution:**

Avoid calling the Identification engine API recursively.


</td></tr><tr><td>

Detected error while processing payload from xyz

</td><td>

-   **Description:**

Error occurred during processing payload.

-   **Resolution:**

Resolve all errors mentioned in the output payload from xyz.


</td></tr><tr><td>

While processing relations encountered errors in payload item: xyz

</td><td>

-   **Description:**

Payload item has errors.

-   **Resolution:**

Resolve errors in payload item ‘xyz'.


</td></tr><tr><td>

Error occurred during parsing input json payload: xyz

</td><td>

-   **Description:**

Error occurred during parsing JSON payload.

-   **Resolution:**

Ensure that input JSON payload has correct JSON format.


</td></tr></tbody>
</table>## Error- MULTI\_MATCH

<table id="table_xwf_gql_yy"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Duplicate dependent records found having relationship \[xyz\] with same CI \(className:\[abc\], sysId:\[def\]\)

</td><td>

-   **Description:**

Found duplicate dependent CIs.

-   **Resolution:**

Check de-duplication tasks for information about all duplicates, and then delete duplicate records.


</td></tr><tr><td>

Found multiple relations between payload items: 'xyz' and 'abc'

</td><td>

-   **Description:**

Found multiple relations between payload items.

-   **Resolution:**

Check for duplicate relationship chains and qualifier chains that might exist.


</td></tr><tr><td>

Found duplicate records in lookup table \[xyz\] using fields \[abc\] and reference field \[def\]

</td><td>

-   **Description:**

Found duplicate records in lookup table.

-   **Resolution:**

Check de-duplication tasks for information about all duplicates, and then delete duplicate records.


</td></tr></tbody>
</table>## Error- QUALIFICATION\_LOOP

<table id="table_gm3_knp_4z"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Qualification chain has loop that contains relation 'xyz'

</td><td>

-   **Description:**

Qualification chain has a loop.

-   **Resolution:**

Remove the loop from the qualification chain with relation ‘xyz'.


</td></tr></tbody>
</table>## Error- TYPE\_CONFLICT\_IN\_QUALIFICATION

<table id="table_izs_vnp_4z"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Invalid payload, qualification chain has multiple possible paths for payload items: 'xyz' and 'abc'

</td><td>

-   **Description:**

Multiple qualification paths found.

-   **Resolution:**

Remove multiple possible qualification paths between items ‘xyz’ and ‘abc'.


</td></tr></tbody>
</table>## Error- RECLASSIFICATION\_NOT\_ALLOWED

<table id="table_pj4_hsp_4z"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

CI Reclassification not allowed from class: \[xyz\] to \[abc\]

</td><td>

-   **Description:**

CI reclassification not allowed.

-   **Resolution:**

Check reclassification tasks for information about reclassification, and check if reclassification from class: \[xyz\] to \[abc\] is valid.


</td></tr></tbody>
</table>## Error- DUPLICATE\_RELATED\_PAYLOAD

<table id="table_i15_qyp_4z"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Found duplicate Related items \(0 and 1\) in the payload index 1 using fields xyz

</td><td>

-   **Description:**

Duplicate Related items present.

-   **Resolution:**

Remove one of the duplicate related items present in the payload.


</td></tr></tbody>
</table>## Error- DUPLICATE\_LOOKUP\_PAYLOAD

<table id="table_w3h_typ_4z"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Found duplicate Lookup items \(0 and 1\) in the payload index 1 using fields xyz

</td><td>

-   **Description:**

Duplicate lookup items present.

-   **Resolution:**

Remove one of the duplicate lookup items present in the payload.


</td></tr></tbody>
</table>## INSERT\_NOT\_ALLOWED\_FOR\_SOURCE

<table id="table_dlz_lcg_kjb"><thead><tr><th>

Message

</th><th>

Description and Resolution

</th></tr></thead><tbody><tr><td>

Insert into \[xyz\] is blocked for data source \[abc\] by IRE data source rule

</td><td>

-   **Description:**

An [IRE data source rule](../task/create-ire-data-source-rule.md) is configured to prevent data source \[abc\] from inserting CIs of the \[xyz\] class.

-   **Resolution:**

Delete or update the appropriate IRE data source rule to let data source \[abc\] insert CIs of the \[xyz\] class.

Or, wait for another permitted data source to create the same CI.


</td></tr></tbody>
</table>