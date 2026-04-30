---
title: Transaction Manager: Integrations - Handlebars syntax
description: You can use the Handlebars templating language when you build an integration transformation template.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-12"
reading_time_minutes: 5
breadcrumb: [Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Integrations - Handlebars syntax

You can use the Handlebars templating language when you build an integration transformation template.

Handlebars is a lightweight templating language that is often used in applications to generate dynamic content. When administrators are building integration transformation templates, they may use the following key elements of Handlebar syntax, though not all of them may be used in ServiceNow CPQ integrations:

-   Expressions \(handlebars\): Enclosed in double curly braces `{{ }}`, expressions allow administrators to insert variables, functions, or properties into the template. For example, `{{user.name}}` would render the value of the name property of the user object.
-   Built-in helpers control logic and iterate through data. For example, conditional helpers let you render content based on its value.
    -   `#if` renders content if the condition is true.``

        ```
        {{#if user.isActive}} 
          Active 
        {{/if}}
        ```

        This snippet renders "Active" only if user.isActive is true.

    -   `#unless` – The opposite of \#if, it renders content if the condition is false.``

        ```
        {{#unless user.isActive}} 
          Inactive 
        {{/unless}}
        ```

        This snippet renders "Inactive" if user.isActive is false.

-   Iteration helpers allow looping through lists or modifying scope.
    -   `#each` loops through an array and renders content for each item.

        ```
        {{#each users}} 
          <li>{{this.name}}</li> 
        {{/each}}
        ```

        This snippet iterates through users and displays each user's name as a list item.

    -   `#with` changes the scope to a specific object.

        ```
        {{#with user}} 
          <p>{{name}}</p> 
        {{/with}}
        ```

        This snippet simplifies access to properties of user in the block.


By using these elements, administrators can build flexible and dynamic integration transformation templates that handle various types of data and logic in a clean and maintainable manner.

## Advanced Handlebar syntax for ServiceNow CPQ integrations

Here’s an explanation of each syntactical element used in the Logik Integration Template, which leverages Handlebars templating language.

-   `{{#if lines}} {{/if}}`

    `{{#if}}` checks whether something is true.

    The following snippet checks whether there is something in `lines`. If `lines` has a value \(like a list of items or some data\), it will do something inside the block. If `lines` is empty or doesn’t exist, it skips the block.

    ```
    {{#if lines}} 
      We have lines to process! 
    {{else}} 
      No lines available. 
    {{/if}}
    ```

    If `lines` exists, it shows "We have lines to process!". If not, it shows "No lines available."

-   `{{~#each lines~}} {{/each}}`

    `{{#each}}` repeats something for each item in a list.

    The following snippet iterates over each item in the `lines` list and renders the content inside the block for every item. The ~ symbols are whitespace control characters in Handlebars. They help remove any extra spaces or line breaks before and after the block, ensuring cleaner and more compact output. \(See below.\)

    ```
    {{~#each lines~}} 
      <p>{{this}}</p> 
    {{/each}}
    ```

    The snippet goes through each item in `lines` and puts each item in a paragraph tag.

-   `{{#if <logik line-level field varname>}} {{/if}}`

    `{{#if <logik ...}}` checks whether a specific piece of data is true or exists. It checks whether a specific field or value \(like varname\) in your data exists or is true. It's a way to check for specific information in a more complex structure \(like in a dataset\).

    ```
    {{#if logik.lineLevelField.isActive}} 
      The field is active! 
    {{else}} 
      The field is not active. 
    {{/if}}
    ```

    This snippet checks whether `logik.lineLevelField.isActive` is true \(like checking if something is "active"\). If it is, it shows "The field is active!" If not, it shows "The field is not active."


## The tilde \(~\)

The tilde \(~\), a control character, hides whitespace and line breaks, helping keep the output clean. It makes HTML more compact and prevents spacing issues in output.

In some of the examples above, a leading tilde before `#each` removes whitespace before the block starts. The trailing tilde after \#each removes whitespace after the block starts.

## The zeroIfMissing custom helper

This helper prevents errors due to missing values and ensures numerical fields always have a valid default value.

```
Custom Helper 'zeroIfMissing'
"price": {{zeroIfMissing txn.price}}, would become -> "price": 0 (or "price": 9.99, if txn.price is present)
```

## The @ symbol

The @ ensures that you're pulling the value from the outer or parent context \(not from the current context\). It’s often used when the data you need is in a parent object or a higher level in the structure, and you want to avoid confusing it with the local data of the current scope.

In the expression `"LGK__TransactionId__c": "@{parentTransaction.id}"`, the `@` symbol is used to reference a value from a parent context or object in templating systems, such as Handlebar or other similar systems.

The `@{}` syntax tells the system to look at the parent context \(the object or data outside the current scope\) and retrieve the value of `parentTransaction.id`.

For example, suppose you have an object like this:

```
{ 
  "parentTransaction": { 
    "id": "12345" 
  } 
}
```

When you use `"LGK__TransactionId__c": "@{parentTransaction.id}"`, the `id` from `parentTransaction` \(which is `12345`\) will be used as the value for `"LGK__TransactionId__c"`.

The @ symbol can also be used for conditional assignment. For example, the line `"LGK__ParentTransactionLineId__c": {{#if txn.line.custom.parentLineReferenceId}} "@{line_{{txn.line.custom.parentReferenceId}}.id}" {{else}} null {{/if}}` is part of a Handlebars template and conditionally sets the value of the field `LGK__ParentTransactionLineId__c`.

-   `LGK__ParentTransactionLineId__c` is the key where the resulting value will be placed.
-   `{{#if txn.line.custom.parentLineReferenceId}}` checks whether `txn.line.custom.parentLineReferenceId` exists and has a value.
-   `@{line_{{txn.line.custom.parentReferenceId}}.id}` creates a dynamic reference to the `id` of a specific line based on `parentReferenceId`.
-   `{{else}} null {{/if}}` sets the value to null if the condition is false.

## Concatenating Salesforce fields with conditional punctuation

In Handlebars, concatenating multiple fields together with punctuation \(like commas, spaces, and conditional checks\) can be done by combining variables in the template and using \{\{\#if\}\} blocks to handle conditional logic.

For example, you can use the following approach to concatenate fields such as street address, street address2, city, state, and zip code for an address while ensuring that a comma and space after street address2 are only included if street address2 is populated:

```
{{#if streetAddress}} 
  {{streetAddress}} 
  {{#if streetAddress2}}, {{streetAddress2}}{{/if}} 
  {{#if city}}, {{city}}{{/if}} 
  {{#if state}}, {{state}}{{/if}} 
  {{#if zipcode}}, {{zipcode}}{{/if}} 
{{else}} 
  No address available 
{{/if}}
```

This concatenates fields like streetAddress, streetAddress2, and city, ensuring that commas are only included when the corresponding fields are populated.

Example output with `streetAddress2`: `"123 Main St, Apt 4, San Francisco, CA, 94105"`

Example output without `streetAddress2`: `"123 Main St, San Francisco, CA, 94105"`

## Conclusion

By using these key elements, administrators can create dynamic, flexible, and maintainable integration transformation templates. Understanding and leveraging expressions, helpers, blocks, conditionals, and parent context references enables handling complex data and logic with ease.

For more information on Handlebars syntax, see the [Handlebars documentation](http://handlebarsjs.com/).

**Note:** Handlebars syntax does not support all the features described in this external document.

