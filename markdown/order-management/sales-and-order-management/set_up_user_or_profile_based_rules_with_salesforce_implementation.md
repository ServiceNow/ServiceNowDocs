---
title: Set up user-based or profile-based rules with Salesforce implementation
description: You can set up a message rule to control access to a field based on the user's role or ID.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up user-based or profile-based rules with Salesforce implementation

You can set up a message rule to control access to a field based on the user's role or ID.

Sometimes, system administrators donʼt want to allow every sales representative to access a particular field. \(For example, perhaps that field should be edited later on in the sales cycle by users with elevated permissions.\) In this case, admins might want to lock down certain fields unless the user accessing the configuration is a Solution Manager or System Administrator. Or, maybe youʼd want them locked down unless the config is accessed by Jane Doe, your companyʼs VP of Sales. This article walks through how to set up such rules.

## Step 1

First, youʼll want to create a new field on your Quote object in SFDC. This field should be of type “Formula,” and the Formula Return Type should be “Text.” Make sure to append the “LGK” suffix to the end of the field name, as this field is going to be twinned into ServiceNow CPQ.

## Step 2

When prompted to enter the formula, this is where you must make a design decision. If you want the rule to be dependent on profile type \(for example, System Administrator\), enter `$User.ProfileId` as the formula:

![Set Up User or Profile Based Rules with Salesforce Implementation](../images/cpq-salesforce-new-custom-field.png)

If you want the rule to fire on a specific user ID, replace `$User.ProfileId` with `$User.Id`.

## Step 3

Add the formula field to the ReferencedFields field data set as you normally would to perform [Field twinning](https://logikio3.my.site.com/s/article/How-do-I-pull-Sales-Force-Quote-Information-into-Logik-io).

## Step 4

Write the rule in ServiceNow CPQ. For example, if you wanted a rule to fire on the System Admin profile, and the System Admin profileʼs ID is 00e8c000002qrLx, you might condition your rule like this:

![Set Up User or Profile Based Rules with Salesforce Implementation](../images/cpq-salesforce-new-custom-field-formula.png)

## Result

In the following screen shots, there are two system administrator users and two rules. One rule is a message rule that fires when a System Administrator accesses a quote, and the other rule fires when Jane Doe accesses the quote. This is the output when a System Admin who is not Jane accesses the configuration:

![Set Up User or Profile Based Rules with Salesforce Implementation](../images/cpq-message-rule-result-1.png)

This is the output when Jane Doe \(who is also a System Admin\) accesses the configuration:

![Set Up User or Profile Based Rules with Salesforce Implementation](../images/cpq-message-rule-result-2.png)

