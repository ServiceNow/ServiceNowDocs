---
title: Dot-walking examples
description: Access fields on a related table from a form, list, or script by dot-walking. This topic includes examples of the different ways that you can dot-walk.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Dot-walking to data in related tables, Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Dot-walking examples

Access fields on a related table from a form, list, or script by dot-walking. This topic includes examples of the different ways that you can dot-walk.

## List fields

You can dot-walk to related fields in a list, such as the field list in a filter. This example demonstrates how to filter the Incident \[incident\] table by the company of the caller who registered the incident.

When you open the list of fields that you want to filter, you see the list of available Incident table fields. The reference fields are followed by the related fields. For example, **Caller** is followed by **Caller** &gt; **User fields**, which means that **Caller** is a reference field, and the related fields are user fields on the **Caller** record.

![The Caller > User fields option.](../image/dotwalking1-ne.png)

If the related fields are not present in the list, select **Show Related Fields** at the bottom of the list. When you select **Show Related Fields**, the menu reloads to display related fields.

![The Show Related Fields option.](../image/dotwalking5-ne.png)

When you select a related field, the menu reloads with the fields of the related table. For example, when you select **Company** under **Caller → User fields**, the field then becomes **Caller.Company**Each selected reference is stored at the top of the fields menu, and the number of dots preceding the field label indicate how many dots from the initial record the user has reached.

The following example image shows that the user is at **Incident.Caller.Company**. You can return to higher levels in the hierarchy by selecting fields located at the top of the menu. For instance, selecting **Incident fields** returns to the list of incident fields.

![Dot-walked fields.](../image/dotwalking4-ne.png)

The related fields can be removed by selecting **Remove Related Fields** at the bottom of the list.

![The Remove Related Fields option.](../image/dotwalking6-ne.png)

## Condition builders

You can make a detailed query on a table by dot-walking in the condition builder.

To dot-walk in a condition builder, first select **Show Related Fields** on the fields menu. This action allows you to add fields from related tables to your query.

For example, you could dot-walk fields in a condition builder to find all Incident records assigned to one specific user, Beth Anglin.To do so, navigate to **Incident** &gt; **Open**, and then open the condition builder. In the fields menu, selects **Show Related Fields** and then open the fields menu again to select **Assigned to → User fields**. Opens the fields menu again to select **Last name**. Then, build the following condition: \[Last name\] \[is\] \[Anglin\]. Finally, select **Run**. The Incident list displays only the records assigned to Beth Anglin.

## List collectors

When selecting a list of fields from a list collector \(for example, when you're configuring a form\), you can dot-walk to fields from other forms.

To see which fields are reference fields and can be dot-walked, look for fields with a plus symbol.

![Reference fields](../image/Dotwalking7.png)

Once a reference field is highlighted, the expand icon \(![Expand icon](../image/expand-icon.png)\) appears above the add icon.

Selecting the expand icon opens the list of fields from the related list in the **Available** pane. The following example shows that the **Assigned to** fields were selected. The previous lists of fields appear at the top of the list.

![Lists of fields](../image/Dotwalking9.png)

Once the field is added to the **Selected** pane, it appears with its full dot-walked syntax. \(For example, **Assigned to.Active**\).

## Scripts

You can dot-walk within a script by invoking the dot-walk syntax. This functionality requires a knowledge of JavaScript.

For scripts that run on the server side, such as business rules, it is necessary to add `current.`

The following script, for example, is a scripted approval rule that requests an approval from the manager of the user who opened the ticket.

```
try{
  current.opened_by.manager;
}
catch(err){}
```

For scripts that run on the client side, such as client scripts, `current` is not necessary. For instance, the following Highlight VIP Caller script runs on the client side.

```
function onChange(control, oldValue, newValue, isLoading){
  //wait until there is a valid record in the field
  if(newValue){ 
    //get the caller object so we can access fields
    var caller = g_form. getReference('caller_id');
    var callerLabel = document.getElementById('label.incident.caller_id');
    var callerField = document.getElementById('sys_display.incident.caller_id');
 
  //check for VIP status
  if(caller.vip == 'true') { 
    //change the caller label to red background
    //style object is CSSStyleDeclaration, style names are not standard css names
  if(callerLabel) 
    document.getElementById('label.incident.caller_id').style.backgroundColor = 'red';
 
  //change the caller's name field to red text
  if(callerField)
     document.getElementById('sys_display.incident.caller_id').style.color = 'red';
  } 
    else { //not a VIP, remove temporary styles if(callerLabel)
     document.getElementById('label.incident.caller_id').style.backgroundColor = '';

    if(callerField)
      document.getElementById('sys_display.incident.caller_id').style.color = '';
    }
  }
}
```

## Variables

Often, you can add variables into templates, notifications, or other forms where a value is being called from the form.

For example, *$\{assigned\_to\}* is the variable for the **Assigned to** field.

As shown in the example, you can dot-walk to fields on the original record of any reference field. It is possible to dot-walk to any field on the assigned\_to record, for example, *$\{assigned\_to.manager\}*.

When you dot-walk, you can have a longer chain if you need it, as in this example: *$\{assigned\_to.department.manager.mobile\_phone\}*.

Sometimes, you can select this variable from a tree picker.

## Tree pickers

The tree picker interface has an expandable, hierarchical view that you can use to look up the following items:

-   Configuration Items \(CIs\) that are subordinate to another, higher-level CI.
-   Members of a certain group. For example, you would use a tree picker to look up a user in the Service Desk group.
-   Reference elements for any hierarchical table. A hierarchical table is any table that has a parent field pointing back at itself. The Group \[sys\_user\_group\] table, for example, would be considered a hierarchical table because certain groups are children of parent groups.

**Note:** You can configure the tree picker to pick up to 1,000 nodes when you configure the **glide.ui.group\_heirarchy.max\_nodes** property. To set the property, open the Dictionary attributes for the field, and add `tree_picker=true` to the **Attributes** field. If there are multiple attributes, use a comma to separate them without any spaces between.

**Parent Topic:**[Dot-walking to data in related tables](../concept/c_DotWalking.md)

