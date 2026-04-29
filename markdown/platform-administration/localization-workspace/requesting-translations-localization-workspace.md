---
title: Requesting translations in Localization Workspace
description: Create and submit translation requests in Localization Workspace. Generate informational cost estimates for review and set a due date before submitting the request.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Requesting translations in Localization Workspace

Create and submit translation requests in Localization Workspace. Generate informational cost estimates for review and set a due date before submitting the request.

## Overview of creating translation requests

As a localization requester, you can create translation requests for multiple content types into multiple languages, all in one interface.

You can save or modify a translation request before submitting it. When you submit the translation request, Localization Workspace creates and packages a project in [Localization Framework](../../localization-framework/concept/localization-framework-landing.md). Creating the project might take several minutes depending on the number of documents. When the project is ready, Localization Workspace sends the translation request to your third-party service provider.

**Note:** From version 3.0.0, you can cancel a [TMS](../../localization-framework/concept/tms-configuration.md) translation request after submitting it. However, Localization Workspace does not contact your service provider. You should notify your provider directly regarding any cancellations.

On the Localization Workspace home page, the **Request Translation** button opens a wizard displaying a four-step process.

1.  [Request translations in Localization Workspace: Languages](../task/lw-request-translations-langs.md)

    Start a translation request by selecting available target languages or language groups.

2.  [Request translations in Localization Workspace: Types](../task/lw-request-translations-types.md)

    Add content types to a translation request. You can select multiple types of documents from tables across your instance. The system retrieves all available translatable documents for each selected content type.

3.  [Request translations in Localization Workspace: Scope](../task/lw-request-translations-scope.md)

    Select or deselect specific documents from the retrieved list of content. Different documents can be selected for each language in the request.

4.  [Request translations in Localization Workspace: Estimate and Due Date](../task/lw-estimate.md)

    Generate an informational cost estimate as the last step in the Request Translation wizard. Review the estimate to plan and control your localization budget. Optionally add a due date for the request.


## Tracking translation requests

When you save or submit a translation request, its record is displayed on the Home screen of Localization Workspace in the **My Requests** list. You can edit, archive, or cancel a translation request from My Requests. For more information, see [Localization Workspace Home and translation job status](lw-status-synchronization.md).

## Translation request due dates

In the Estimate step of a translation request, the system suggests due dates based on the type of service provider. You can optionally accept the suggested due date, or you can use the calendar picker to choose another date. You can't choose a date that is earlier than the suggested date, however.

From version 3.0.0, intelligent due dates are offered when requests are submitted through a [TMS](../../localization-framework/concept/tms-configuration.md). Localization Workspace suggests a due date based on the target language's word or character count, using the following industry-standard formula.

<table id="table_hjz_5hc_j3c"><thead><tr><th>

Target language type

</th><th>

Formula used

</th></tr></thead><tbody><tr><td>

Words

</td><td>

Divide the total word count by 1500. Then add 2. The result is the expected number of days to complete the translation. Add that number to the current date.

</td></tr><tr><td>

Characters

</td><td>

Divide the total character count by 15,000. Then add 2.The result is the expected number of days to complete the translation. Add that number to the current date.

</td></tr></tbody>
</table>**Note:** The Estimate step of a translation request displays Word counts, not Character counts, even when the target language has been configured as character-based. However, the intelligent due date suggestion uses the Characters formula for languages configured as character-based.

When using a TMS to translate into multiple target languages in one request, the formula assumes that the languages are processed concurrently, not sequentially. This means that the language with the highest word or character count is used to calculate the due date suggestion.

For machine translation service providers, the default due date is the current date. Due dates in Localization Workspace correspond to the Localization Framework Project due dates.

## Due date calculation for a TMS request

The following example illustrates the due date calculation when the word count is 62,453.

1.  Divide the word count by 1500.

    62453 / 1500 = 41.6.

2.  Truncate \(round down or take the floor\) to the nearest whole integer.

    41.6 becomes 41.

3.  Add 2 days.

    41 + 2 = 43.

4.  Add the number of days to the current date.

    The suggested due date is 43 days from the current date.


