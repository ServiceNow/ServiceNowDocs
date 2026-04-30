---
title: Using the Recommended Actions application
description: Through the Recommended Actions application, use the recommended actions of type guidance and guided decision tree in your workspace to resolve cases quickly. Use the field recommendation to get recommendations on the field values. Use the AI search option to search the relevant resources from various sources.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Automate and optimize, Use, Customer Service Management]
---

# Using the Recommended Actions application

Through the Recommended Actions application, use the recommended actions of type guidance and guided decision tree in your workspace to resolve cases quickly. Use the field recommendation to get recommendations on the field values. Use the AI search option to search the relevant resources from various sources.

## Recommended actions

Recommended actions appear as cards in the contextual side panel of your workspace. Depending on the open record type, these cards contain information to help find the fastest resolution path, minimizing time spent researching and gathering information from different sources.

You can take three types of actions:

-   **Guidance**: An action that can be performed or helpful information to share.
-   **Decision tree**: A guided flow to follow that walks you through a series of questions that help you determine the appropriate action.
-   **Field recommendations**: Recommended values to use for the fields in the record. Recommended field values are auto-filled or shown as messages underneath the fields for the new records. The recommended field values are shown as messages only underneath the fields for the existing records.

![Case record view with recommended actions in the contextual side panel with Guidance and Decision trees as recommendations with relevant resources and input](../image/ra-side-panel.png "Recommended action cards in a workspace")

Recommended action cards display the following information:

-   Hint that briefly describes the recommendation.
-   Preview that shows a short summary of the recommended action, which can include an image and links to helpful articles.
-   Options to accept or dismiss the action.

When multiple cards are displayed, they’re arranged according to the Order value set when they were created.

## Primary and secondary actions

The recommendation that you select determines what is displayed next in the contextual side panel or subtab and how the record is updated. Some actions involve a single selection that is performed immediately such as **Acknowledge**, **Attach and add link in comment**. Other actions might have secondary actions that you can enable after selecting the primary action in the card. The following table explains a few primary and secondary actions.

<table id="table_njr_y1y_1dc"><thead><tr><th>

Primary action

</th><th>

Secondary action

</th><th>

Guidance name

</th></tr></thead><tbody><tr><td>

Select the **View and attach article** to open the knowledge article in the side panel for review.

</td><td>

Select secondary actions, such as **Dismiss** to cancel the recommendation or **Attach article** to attach it to the case or select an option from the More actions icon \(![Displays secondary actions such as copying a link or flagging an article](../image/more_vertical_icon.png)\).![More actions enables the user to mark an article as helpful, flag an article, copy or expand the article](../image/ra-secondary-actions.png)

Select back to go back to the recommended cards list.

</td><td>

Review and attach article

</td></tr><tr><td>

Select **Attach and add link in comment** to compose a comment and **Post comments**.

</td><td>

Select secondary actions from the More actions menu \(![Displays secondary actions such as copying a link or flagging an article](../image/more_vertical_icon.png)

 ![More actions enables the user to read the article, attach and add a link in email, add a link in a work note, or copy a link](../image/ra-secondary-actions2.png)

**Note:** The primary and secondary actions are configurable.

</td><td>

Attach and share article

</td></tr></tbody>
</table>## Recommended Actions process

<table id="table_nr1_hv4_bvb"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Single-click action

</td><td>

-   The guidance moves to the in-progress or completed state.
-   A message indicates that the action was performed or completed. The system updates the record accordingly.

-   The selected recommendation card moves from the **Recommended actions** or **Search** tab to **Action history**.

The card displays the action performed for the recommendation and any outputs, such as a credit report and credit score generated for the customer.


</td></tr><tr><td>

Contextual side panel or subtab action

</td><td>

-   When the action button is selected, the guidance doesn't move to the in-progress state. Other users can still see and act on this guidance.
-   When the action button is selected in the detail experience, the guidance moves to in-progress or completed state.
-   A message indicates that the action was performed or completed. The system updates the record accordingly.
-   The selected recommendation card moves from the **Recommended actions** or **Search** tab to **Action history**.

 **Note:** For the guided decision trees, when the preview button is selected, the guidance opens in the side panel and moves to the in-progress state.

</td></tr><tr><td>

Error handling

</td><td>

If an action ends up in the error state, the following occurs:-   An error notification is shown. The system updates the record accordingly.

-   The card displays the error state for the recommendation.

-   When dismissed, the card moves to **action history**.

</td></tr></tbody>
</table>## Field recommendations

Field recommendations are messages that display either under fields on a form or auto-fill a recommended value within the field. For example, a field recommendation can recommend an assignment group based on the text in a case's short description.

You can read the description of the recommendation and use the recommended value in the fields.

## AI search

AI search enables you to search for the relevant resources to resolve cases or customer issues. Depending on the AI search configuration, the AI search tab displays search results, genius result answers, or both. AI search results appear in the form of guidances that you can act on. Genius result answers are the most relevant answers or the top results for the search query along with the action that you can take directly from the card.

![AI search cards in the contextual side panel with genius and search results.](../image/ra-ai-search.png "AI search cards in a workspace")

<table id="table_vj1_qqm_xyb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search count

</td><td>

Displays counts of the total number of matching search results. The search filters show the number of matching results for each search source.**Note:** The Search results that are displayed and the total search count might vary due to security permissions or if the search result has already been executed. The executed guidances are moved to **Action history** and reflect in the total search count but the executed guidances won't show up in the search results.

</td></tr><tr><td>

Search bar

</td><td>

Accepts the search query that produces the search results. You can modify this search query and search again to view different results.

</td></tr><tr><td>

Search filters

</td><td>

Displays filter options for refining search results by search source.

</td></tr><tr><td>

Full view search

</td><td>

Displays the search results in a new subtab with an expanded view.

</td></tr><tr><td>

Sort search results

</td><td>

Sorts the search results based on the selected option.

</td></tr><tr><td>

Search result cards

</td><td>

Displays the search icon, search source, title, summary field values, and text snippet for each search result, with search query terms highlighted in title and text snippets. You can select a result to view its source record in full or select the action to act on the guidance.

</td></tr><tr><td>

Genius result cards

</td><td>

Displays the genius result icon, title, summary of the answer, and an action to take on the genius result card.**Note:** Genius result cards do not always show a summary of the answer.

</td></tr><tr><td>

Show more

</td><td>

Displays more search results.

</td></tr></tbody>
</table>