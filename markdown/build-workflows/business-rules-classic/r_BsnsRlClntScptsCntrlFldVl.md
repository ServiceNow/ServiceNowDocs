---
title: Control field values using business rules and client scripts
description: Implement both business rules and client scripts for a field to enable users to set record values properly using both forms and lists, and to see immediate changes to the values in forms as edits are made.The string NULL has a particular role in scripts and is a reserved word.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/business-rules-classic/r\_BsnsRlClntScptsCntrlFldVl.html
release: brazil
product: Business rules \(Classic\)
classification: business-rules-classic
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Classic Business rules, Build workflows]
---

# Control field values using business rules and client scripts

Implement both business rules and client scripts for a field to enable users to set record values properly using both forms and lists, and to see immediate changes to the values in forms as edits are made.

The problem with using only a client script or a business rule to control updates to a field is that fields can be changed on either a form or a list. Client scripts and UI policies run on forms only \(client-side\) and do not apply to list editing. Allowing list editing with client scripts running on fields in a form can result in incorrect data being saved to the record. For systems in which client scripts or UI policies apply to forms, either disable list editing or create appropriate business rules or access control to control the setting of values in the list editor. A side effect of this is that security measures implemented in client scripts are easy to circumvent. The user only needs to edit the field in a list.

Business rules on a form are not dynamic, the user must update the record for the change to be seen. This makes using client scripts the preferred method for controlling field values on forms.

When using both a business rule and client script to control field values, the update behavior is the same across the system. This means that updated values are not different depending on whether a list of form is used to make the change. This means that the same functionality must be implemented twice, once in a client script and once in a business rule or access control.

## Example: Use a business rule to create email addresses during user record import

An organization has a client script that sets the email address for a user to `first.last@company.com`. Administrators do this so they can see the email address immediately when they enter the user's information. The administrator then performs a bulk import of users from a spreadsheet containing the users' first and last names. The expectation is that each user's email address will be set automatically, as they are when they edit the form. Since the client script runs only on the form \(the interface to the record\), it has no effect on data imported into the record from outside that interface, and no email addresses are created. To solve this problem, the administrator implements a business rule that runs when the import occurs and creates the email addresses.

## Example: Prevent list edit for a field that is not editable in the form

An organization wants to hide the **Priority** field on an incident form if the assignment group is **Development**. They create a UI policy on the incident form to do this, but their users can still see and edit the **Priority** field using the list editor. To rectify this, apply an access control to prevent read access to the **Priority** field when the assignment group is **Development**.

**Parent Topic:**[Classic Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/c_BusinessRules.md)

## Using NULL as a field value

The string NULL has a particular role in scripts and is a reserved word.

The reserved word is NULL in all capital letters. A field with the value **Null** or **null**, for example, is acceptable. Only use NULL to clear out a particular field.

Any NULL field values obtained from an import set data source are inserted into the staging table as empty field values. You should not use the term NULL as a field value in import set transform maps or anywhere in the **First name** or **Last name** fields. Also, do not use NULL in reference fields as the system interprets the value as a string containing the word NULL, not as a reserved word.

