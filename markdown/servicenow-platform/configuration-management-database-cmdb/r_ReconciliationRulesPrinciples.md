---
title: Reconciliation rules
description: Reconciliation rules determine which discovery sources can update CI attributes.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Reconciliation rules

Reconciliation rules determine which discovery sources can update CI attributes.

Discovery sources, such as EventManagement, ImportSet, ManualEntry, and Tivoli, are used with the [createOrUpdateCI\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_IdentEngineScriptAPI.md) API to simulate manual updates to CIs. Without reconciliation rules, discovery sources can overwrite each other's updates to attribute values.

There are two types of reconciliation rules:

-   **Static reconciliation rules**

    Static reconciliation rules are the legacy reconciliation rules that set priorities for the various discovery sources for updating CI attributes. Static reconciliation rules specify which discovery sources can update class attributes, and the precedence order among these discovery sources.

    When creating static reconciliation rules, ensure that there is a reconciliation rule for each discovery source that is authorized to update an attribute. Reconciliation rules can be defined at the parent and the child class level.

    Static reconciliation rules are stored in the Reconciliation Definition \[cmdb\_reconciliation\_definition\] table.

-   **Dynamic reconciliation rules**

    Dynamic reconciliation rules are based on attribute values processed by [CMDB 360](../concept/multisource-cmdb.md) rather than on discovery source priority. First, CMDB 360 processes the current payload data into the CMDB 360 data store. Then, applying a dynamic reconciliation rule, IRE selects the largest or most reported value, for example, across all discovery sources. Because dynamic reconciliation rules leverage CMDB 360, you must enable that feature to use dynamic reconciliation rules.

    Creating dynamic reconciliation rules can be useful, for example, if it becomes difficult to set priority order for multiple discovery sources. Only a single dynamic reconciliation rule can exist per class attribute.

    Dynamic reconciliation rules are stored in the Dynamic Reconciliation Definitions \[cmdb\_dynamic\_reconciliation\_definition\] table.


## Examples of static reconciliation rules

The following sample static reconciliation rules are created for the **cmdb\_ci\_computer** class and its **cmdb\_ci\_linux\_server** child class:

1.  Discovery is exclusively authorized to update the **name** attribute in the **cmdb\_ci\_computer** class.

    Because reconciliation rules are derived by child classes from parent classes, this rule also authorizes Discovery to update the **name** attribute in any child classes for the **cmdb\_ci\_computer** class.

2.  ServiceWatch is exclusively authorized to update the **name** attribute in the **cmdb\_ci\_linux\_server** class.
3.  ServiceWatch is exclusively authorized to update all attributes in the **cmdb\_ci\_linux\_server** class, as configured by leaving the **Attributes** field empty in the rule.

See [Create a CI reconciliation rule](../concept/create-reconciliation-rule.md#) for details about creating a static reconciliation rule that, for example, authorizes a discovery source to update a specific attribute such as **name**.

## Using reconciliation rules

As you create reconciliation rules, keep in mind the following principles which are designed for flexibility and the refinement of rules at the attributes level:

-   **Precedence of dynamic reconciliation rules**

    When both, static and dynamic reconciliation rules exist for the same CI attribute, the dynamic reconciliation rule takes precedence over the static reconciliation rule.

-   **Authorization for all attributes in a class**

    A static reconciliation rule lets you authorize a discovery source to update all attributes in a class. However, this authorization can be overridden for some of the attributes by rules for child classes in which specific attributes are listed.

    For example, if only example rules \#1 and \#3 above are created, then Discovery is authorized to update the **name** attribute in the **cmdb\_ci\_linux\_server** class. ServiceWatch is authorized to update all other attributes in the class except for the **name** attribute.

    To override the authorization of Discovery to update the **name** attribute, example rule \#2 above is added to specifically authorize ServiceWatch to update the attribute.

-   **Authorization to only specific attributes in a class**

    To authorize a discovery source to update specific attributes in a class, create a static reconciliation rule for the discovery source, and list these attributes in the rule. A rule that grants access to specific attributes in a class overrides other static reconciliation rules with an empty attribute list that grants access to the entire class.

    Example rule \#1 above grants Discovery with exclusive authority to update the **name** attribute of the **cmdb\_ci\_computer** class. All other discovery sources are prevented from updating the **name** attribute of any CI in the **cmdb\_ci\_computer** class.

-   **Child class rules overrides parent class rules**

    Any reconciliation rules defined for a child class override the rules defined for its parent class. So if an attribute of a derived rule is overridden by a child's class rule for a specific class, then the derived rule has no effect on that attribute. This behavior applies also when the child's reconciliation rule is static and the parent's rule is dynamic \(dynamic reconciliation rules have precedence over static reconciliation rules when they are for same level class\).

    For example, rule \#1 above lets Discovery update the **name** attribute in the **cmdb\_ci\_computer** class and all of its child classes. However, rule \#2 for the **cmdb\_ci\_linux\_server** child class, which overrides rule \#1 for the parent class, explicitly authorizes ServiceWatch to update this attribute in the child class.

    As a result:

    -   Discovery cannot update the **name** attribute of the child **cmdb\_ci\_linux\_server** class. Only ServiceWatch is authorized to update this attribute.
    -   Discovery is authorized to update the **name** attribute of CI records in all other child classes of the **cmdb\_ci\_computer** class.
-   **Overlapping static reconciliation rules**

    Static reconciliation rules that authorize different discovery sources for the same attributes of the same class can coexist and do not exclude each other.

    For example, assume the following rule is added. It is similar to example rule \#1 above but authorizes a different discovery source:

    ServiceWatch is authorized to update the **name** attribute in the **cmdb\_ci\_computer** class.

    Like example rule \#1 above, this new rule applies to the **name** attribute in the **cmdb\_ci\_computer** class so both Discovery and ServiceWatch can update the attribute. Any reconciliation rules are enforced to prevent the discovery sources from overwriting each other's updates.


For more information about reconciliation rules, see the [CMDB - Data Precedence Rules Understanding the CMDB data precedence rules and troubleshooting \[KB0756709\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB0756709) knowledge base article.

## Domain separation

If Domain Separation is enabled, then you can scope reconciliation rules to specific domains. Rules of the parent domain, if not overridden, apply to CIs of child domain. All rules that are visible to a domain are applied, and a rule overriding the parent domain displays the child domain version.

-   **[Create a CI reconciliation rule](../concept/create-reconciliation-rule.md#)**  
Create a static or a dynamic CI reconciliation rule.
-   **[Create a data refresh rule](../task/create-datasource-staleness-rule.md)**  
Specify data refresh rules to determine if a CI is stale for a specific discovery source. Such CIs can then be updated by a lower-priority authorized discovery source.

**Parent Topic:**[Configuring CMDB Identification and Reconciliation](../concept/configuring-ire.md)

