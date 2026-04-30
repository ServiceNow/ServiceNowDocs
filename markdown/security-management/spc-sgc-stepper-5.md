---
title: Map API response to SPC attributes
description: Map API response properties to SPC attributes.￼ After you have mapped the attributes, you publish your connector so it imports data.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-20"
reading_time_minutes: 3
breadcrumb: [Creating your own API connector, Use the workspace, Security Posture Control, Security Operations]
---

# Map API response to SPC attributes

Map API response properties to SPC attributes.￼ After you have mapped the attributes, you publish your connector so it imports data.

## Before you begin

For this step, you map parameters to SPC attributes and policies from the data you imported with your API connector.

-   Select and use the API response sample in the list in the Reference section for SPC attributes.
-   Select the API response schema sample in the list for API attributes to help you map the properties to dedicated SPC attributes.

These schema and samples are provided for you after you enter values and save your edits in the [previous step](spc-sgc-template-stepper-4.md). The response schema is aggregated. To see all observed properties, change the reference list to **API response schema**.

You have the option to get guidance for selecting a template with a Now Assist skill for this step. See [Exploring Now Assist for Vulnerability Response](../../now-assist-vulnerability-response/concept/exploring-ai-for-now-assist-for-vulnerability-response.md) for more information about the generative AI skill and [Using Now Assist for Vulnerability Response in Security Posture Control](../../now-assist-vulnerability-response/concept/using-now-assist-api-connector.md) about using the skill in connector framework.

**Note:** Regardless of whether you enter your parameters manually, or if you choose use Now Assist to generate your parameters automatically, you must [Validate your API connector](spc-sgc-validate-api-connector.md) before you can publish it.

Roles required:

-   sn\_sec\_spc\_core.developer
-   sn\_spc\_cxf.admin - required for advanced scripting

## Procedure

1.  Add required attributes.

    Select the tooltips for more information and context about the fields on this page.

    The Host name attribute and Asset identifier attributes are required. Other fields are optional. All attribute values can be scripted with the script toggle. To commit your script, you must select **Save and Close script**. If you no longer want to script an attribute, select the scripting toggle to deactivate it.

    The Collection field applies the same collection to all attributes, and this value helps you fill out the form quickly. This field auto-populates any fields that aren’t yet mapped.

    1.  Add an Asset identifier.

        An asset identifier is a unique combination of properties returned by the API to identify configuration items.

    2.  Add a Host name attribute.

    3.  Create an SPC custom attribute if you want to add a property.

        Only create custom properties if they aren’t included as part of the default attributes that are provided. Use the following steps to create custom properties.

2.  As an example, create an attribute, `osName` for an asset's operating system from the reference samples.

    1.  Select **API response sample** in the Reference window.

    2.  Locate the object, for example, `"operatingSystem"`, and note it might have a property such as `"osName"`.

    3.  Select **Add attribute**.

    4.  Select the Collection field to apply a filter to the API attribute list, in this example, this might be something like, **$.operatingSystem**.

    5.  Select the API attribute field and select **osName** from the list.

        The Type list persists the mapped value to that type. Select the type that you want this attribute to be stored as. This field is required.

        Use the Transformer field to augment the value coming back from the API. For example, if you select **Date** for the Type, you can use the Transformer field to cast between types. Using the transformer is optional.

    6.  Add properties so you can filter data so that it identifies specific types of assets with this attribute.

    7.  Select the Asset identifier attributes field and add the properties you want, for example, **address** and **assetType**.

        Adding these properties not only helps you identify specific assets, but additionally it might help you identify an asset that is reported differently by multiple security tools. One tool might import it using **address**, for example, and another might report the **assetType**. Adding these attributes can help you avoid creating duplicate findings for the same asset.

3.  After you have completed the mapping, select **Save and continue** to save your changes.

    You must save your changes before you can continue.


