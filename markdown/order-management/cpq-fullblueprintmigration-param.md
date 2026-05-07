---
title: The fullBlueprintMigration parameter
description: Learn the effects of enabling or disabling the fullBlueprintMigration parameter on sources in various configurations. The fullBlueprintMigration parameter controls how thoroughly a blueprint is updated during migration.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up blueprints, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# The fullBlueprintMigration parameter

Learn the effects of enabling or disabling the fullBlueprintMigration parameter on sources in various configurations. The fullBlueprintMigration parameter controls how thoroughly a blueprint is updated during migration.

## The fullBlueprintMigration parameter

When migrating an edited blueprint from a source environment to a destination environment where an earlier version of the same blueprint exists, **fullBlueprintMigration: true** instructs the destination environment to perform the migration more aggressively than it otherwise would. In the matrix below, common scenarios performed on the source environment blueprint are noted in the first column. The destination environment performs the corresponding migration task according to the true or false setting of fullBlueprintMigration, corresponding to the rightmost columns.

<table id="table_yym_3cf_rgc"><thead><tr><th>

Activity on source before migration

</th><th>

Parameter = false

</th><th>

Parameter = true

</th></tr></thead><tbody><tr><td>

Picklist option deleted

</td><td>

Picklist option retained on destination

</td><td>

Picklist option deleted on destination

</td></tr><tr><td>

Rule removed from blueprint \[see Note below\]

</td><td>

The rule remains associated to blueprint on destination

</td><td>

Rule removed from blueprint on destination**Note:** If the rule is not associated with any other blueprint on the destination, the rule is removed from the global rule list on the destination,

</td></tr><tr><td>

Rule action removed from rule

</td><td>

Rule Action retained on destination

</td><td>

Rule Action deleted on destination

</td></tr><tr><td>

Product is removed from ProductList on Simple Product Action

</td><td>

Product remains in ProductList on destination

</td><td>

Product is removed from ProductList on destination

</td></tr></tbody>
</table>## Notes

CPQ administrators do not directly associate or remove rules to or from blueprints. Instead, a rule is associated with a blueprint only if all its referenced fields are associated with the blueprint. Therefore, the admin manipulates a rule's association with a blueprint by associating or removing \(deassociating\) its fields. A rule will be removed from a blueprint in several circumstances, including:

-   A field referenced by the rule is removed from the blueprint.
-   In the rule, the admin adds a reference to a field that is not associated with the blueprint.
-   A new rule action that references a field not associated with the blueprint, is added to the rule.
-   The rule condition is modified to include a reference to a field that is not associated with the blueprint.

**Related topics**  


[Testing in non-production environments before migration](../concept/cpq-env-to-env-bp-migration-intro.md)

