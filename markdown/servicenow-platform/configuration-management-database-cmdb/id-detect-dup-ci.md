---
title: Detecting duplicate CIs
description: When IRE identification process detects duplicate CIs, it groups each set of duplicate CIs into a de-duplication task for review and remediation. A large number of duplicate CIs might be due to weak identification rules. You can configure the identification engine to reconcile duplicate CIs.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Detecting duplicate CIs

When IRE identification process detects duplicate CIs, it groups each set of duplicate CIs into a de-duplication task for review and remediation. A large number of duplicate CIs might be due to weak identification rules. You can configure the identification engine to reconcile duplicate CIs.

During Identification and Reconciliation Engine \(IRE\) processes, handling of duplicate CIs is determined by the properties **glide.identification\_engine.skip\_duplicates** \(set to true by default\) and **glide.identification\_engine.skip\_duplicates.threshold** \(set to 5 by default\), and on the number of duplicate CIs that are detected. You can configure these properties so that duplicate CIs are automatically reconciled, skipping duplication.

-   If **glide.identification\_engine.skip\_duplicates** is true, and the number of duplicate CIs is less than the threshold specified by **glide.identification\_engine.skip\_duplicates.threshold**, then the oldest of the duplicate CIs is picked as a match and gets updated. That oldest duplicate CI also becomes the main CI for that set of duplicate CIs. The rest of the duplicate CIs are tagged as duplicates by setting their **duplicate\_of** attribute to the appropriate main CI. During matching, IRE filters out any CI that is tagged as duplicate of any CI.
-   If **glide.identification\_engine.skip\_duplicates** is false, then matching of duplicate CIs fails with an error, and none of the duplicate CIs are updated.

Also, the **glide.duplicate\_ci\_remediator.max.cis** property determines de-duplication processing for a large number of duplicate CIs. For more information, see the 'Large number of duplicate CIs' section in the [Duplicate CIs remediation](de-duplication-tasks.md) topic.

In either case, de-duplication tasks are always created.

**Note:** For a duplicate CI, if any of the CI's attributes, other than **duplicate\_of**, is updated by IRE processing, then the CI is no longer considered a duplicate CI. In that situation, the value of **duplicate\_of** is cleared in the CI.

For more information about these properties, see [Properties for Identification and Reconciliation](../reference/properties-id-reconciliation.md).

## Detecting duplicate CIs in related and lookup tables

During CI identification, IRE might detect duplicate lookup items \(Serial Number \[cmdb\_serial\_number\] table\), or duplicate related items \(Software Instance \[cmdb\_software\_instance\] table\). By default, IRE doesn't create de-duplication tasks for these duplicate items. However, you can modify this default behavior by configuring IRE to generate de-duplication tasks for specific lookup or related tables, allowing you to then remediate any duplications.

Add entries in the CMDB Deduplication Task Lookup or Related item allowed classes \[cmdb\_duplicate\_lookup\_related\_allowed\_class\] configuration table for each table for which you want IRE to generate de-duplication tasks during identification:

-   Add an entry for any lookup table in an identifier entry in the respective identification rule.
-   Add an entry for any related table in a related entry in the respective identification rule.

In the base system, this configuration table has no records, in which case IRE doesn’t generate de-duplication tasks for any duplications in lookup or related tables from the identification rule. When detecting duplication in related or lookup tables, IRE will generate de-duplication tasks only for those tables with an active entry in the configuration table:

1.  Ensure that you have the required role for the cmdb\_duplicate\_lookup\_related\_allowed\_class table.
    -   To add or update records: sn\_cmdb\_admin, cmdb\_dedup\_admin, or itil\_admin
    -   To read or create reports: sn\_cmdb\_editor, sn\_cmdb\_admin, itil, itil\_admin, cmdb\_dedup\_admin
2.  In the navigation filter, enter `cmdb_duplicate_lookup_related_allowed_class.list`.
3.  Select **New** and fill out the CMDB Deduplication Task Lookup or Related item allowed classes table form.

    |Field|Description|
    |-----|-----------|
    |Active|Is the entry active.|
    |Lookup or related item class|The lookup table \(such as Serial Number \[cmdb\_serial\_number\]\) or related table \(such as Software Instance \[cmdb\_software\_instance\]\) for which you want IRE to create de-duplication tasks when detecting duplicate records.|
    |Identifier table|The identification rule class, such as Hardware \[cmdb\_ci\_hardware\] or Operational Technology \(OT\).|


The CMDB CI Class Models ServiceNow® Store app adds class models that extend the CMDB class hierarchy, and contains meta data such as identification and reconciliation rules for the added classes. When specifying class models in this app, you can also include the cmdb\_duplicate\_lookup\_related\_allowed\_class table with entries specific to the added tables, such as the Operational Technology \(OT\) table. In which case, IRE will generate de-duplication tasks as configured in the table. For more information, see [CMDB CI Class Models app](cmdb-ci-class-models.md).

You can also add records to the cmdb\_duplicate\_lookup\_related\_allowed\_class configuration table for added classes after the CMDB CI Class Models app has been installed.

## Detecting duplicate referenced CIs during lookup-based identification

In a lookup-based identification \(lookup identifier entry in the identification rule for a class\), IRE might detect duplicate related items in the lookup table. For example, two records in which the serial numbers are identical but each referencing a different CI. In this situation, IRE selects the record with the older referenced CI as a match in the identification process.

Lookup items matching multiple CIs might be valid in some organizations and invalid in others. You can configure IRE behavior of creating de-duplication tasks to remediate such duplications, by using the **glide.identification\_engine.lookup\_match.create\_duplicate\_task\_ci.enabled** system property.

Add and then set the property to reflect on whether such duplications are valid or not in the organization, as follows:

-   **false \(default\)**

    IRE selects the older CI as a match but doesn't create a de-duplication task to handle the duplication. Use this setting when such duplication isn't considered a duplication problem. For example, records with identical serial numbers where each is referencing a different CI. However, each serial number actually represents a different type of hardware, and therefore, this situation isn't considered a duplication problem requiring reconciliation.

-   **true**

    IRE selects the older CI for the matching process and generates a de-duplication task to remediate the duplication. Use this setting when such duplication is considered a problem that requires remediation.

    IRE doesn't create de-duplication tasks even when **glide.identification\_engine.lookup\_match.create\_duplicate\_task\_ci.enabled** is **true**, in the following circumstances:

    -   **Enforce exact count match** is set to **false**. For information about where it's set, see the advanced options in the 'Use attributes from another table \(Lookup table\)' option in [Create a CI identification rule](../task/t_CreateCIIdentificationRule.md).
    -   During identification, the number of matching CIs in the lookup table is greater than 1.

See the following examples of lookup records, input payloads, and the results of identification processes:

-   Example 1

    Lookup table cmdb\_serial\_number contains duplicate lookup records and multiple CIs matching both lookup items ABC123 and DEF456:

    |Serial Number|Configuration Item|
    |-------------|------------------|
    |ABC123|CI1|
    |ABC123|CI1|
    |ABC123|CI2|
    |DEF456|CI1|
    |DEF456|CI2|
    |DEF456|CI2|

    ```
    var payload = {
       "items": [
          {
             "className": "cmdb_ci_linux_server",
             "lookup": [
                {
                   "className": "cmdb_serial_number",
                   "values": {
                      "serial_number": "ABC123",
                      "serial_number_type": "system",
                      "valid": "true"
                   }
                },
                {
                   "className": "cmdb_serial_number",
                   "values": {
                      "serial_number": "DEF456",
                      "serial_number_type": "system",
                      "valid": "true"
                   }
                }
             ],
             "values": {
                "name": "CI_New"
             }
          }
       ],
       "relations": []
    };
    var jsonUntil = new JSON();
    var input = jsonUntil.encode(payload);
    var output = SNC.IdentificationEngineScriptableApi.createOrUpdateCIEnhanced("ServiceNow", input, {});
    gs.print(output);
    
    
    ```

<table id="table_bls_v2g_ygc"><thead><tr><th>

Exact count match

</th><th>

Property to create de-duplication task = true

</th><th>

Property to create de-duplication task = false

</th></tr></thead><tbody><tr><td>

True

</td><td>

-   CI1, the oldest, is matched and updated.
-   De-duplication task is created for CI1 and CI2 \(Linux Server class.\)
-   De-duplication task is created for ABC123/system &amp; CI1 \(Serial Number lookup table\).
-   De-duplicate task is created for DEF456/system &amp; CI2 \(Serial Number lookup table\).


</td><td>

-   CI1, the oldest, is matched and updated.
-   De-duplication task isn't created for CI1 and CI2.
-   De-duplication task is created for ABC123/system &amp; CI1 \(Serial Number lookup table\).
-   De-duplicate task is created for DEF456/system &amp; CI2 \(Serial Number lookup table\).


</td></tr><tr><td>

False

</td><td>

Same as above

</td><td>

Same as above

</td></tr></tbody>
</table>-   Example 2

    No duplicate lookup records are found in the lookup table cmdb\_serial\_number, but there are 2 CIs each matching ABC123 and DEF456 respectively:

    |Serial Number|Configuration Item|
    |-------------|------------------|
    |ABC123|CI1|
    |DEF456|CI2|

    ```
    var payload = {
       "items": [
          {
             "className": "cmdb_ci_linux_server",
             "lookup": [
                {
                   "className": "cmdb_serial_number",
                   "values": {
                      "serial_number": "ABC123",
                      "serial_number_type": "system",
                      "valid": "true"
                   }
                },
                {
                   "className": "cmdb_serial_number",
                   "values": {
                      "serial_number": "DEF456",
                      "serial_number_type": "system",
                      "valid": "true"
                   }
                }
             ],
             "values": {
                "name": "CI_New"
             }
          }
       ],
       "relations": []
    };
    var jsonUntil = new JSON();
    var input = jsonUntil.encode(payload);
    var output = SNC.IdentificationEngineScriptableApi.createOrUpdateCIEnhanced("ServiceNow", input, {});
    gs.print(output);
    
    ```

<table id="table_qrv_vsg_ygc"><thead><tr><th>

Exact count match

</th><th>

Property to create de-duplication task = true

</th><th>

Property to create de-duplication task = false

</th></tr></thead><tbody><tr><td>

True

</td><td>

-   No CI match is found.
-   De-duplication task isn't created for CI1 and CI2.
-   No de-duplication tasks are created for lookup items.


</td><td>

-   No CI match is found.
-   De-duplication task isn't created for CI1 and CI2.
-   No de-duplication tasks are created for lookup items.


</td></tr><tr><td>

False

</td><td>

-   CI1, the oldest, is matched and updated.
-   De-duplication task is created for CI1 and CI2.
-   No de-duplication tasks are created for lookup items.


</td><td>

-   CI1, the oldest, is matched and updated.
-   De-duplication task isn't created for CI1 and CI2.
-   No de-duplication tasks are created for lookup items.


</td></tr></tbody>
</table>
## Remediating de-duplication tasks

For information about reviewing and remediating de-duplicate tasks, and how the main CI is used, see [Duplicate CIs remediation](de-duplication-tasks.md).

**Parent Topic:**[CMDB Identification and Reconciliation \(IRE\)](c_CMDBIdentifyandReconcile.md)

