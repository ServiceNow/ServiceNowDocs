---
title: Color variable support for card view buttons
description: Learn how to use color variables to change theming in your mobile card view buttons.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/mobile/color-var-cardview-button.html
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Color theme considerations, Configure theming, Next Experience theming, Configuring the Mobile Platform, Mobile Platform]
---

# Color variable support for card view buttons

Learn how to use color variables to change theming in your mobile card view buttons.

<table id="table_w1s_df2_zvb"><tbody><tr><td>

Use color variables in **Card template element attributes** to control color values for icon buttons on your mobile cards.

 The following color variables are available to use:

-   **BackgroundColorVariable**
-   **BorderColorVariable**
-   **TextColorVariable**

 For more information on these attributes, see [Card template element attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mca-attributes.md).

</td><td>

\[Omitted image "color-var-example-6.png"\] Alt text: Color variable used in a card view template element

</td></tr></tbody>
</table>## Button style guide

<table id="table_rwx_4ny_mxb"><thead><tr><th>

Color

</th><th>

Example

</th><th>

Variables

</th></tr></thead><tbody><tr><td>

Primary

</td><td>

\[Omitted image "button-primary.png"\] Alt text: Primary button example

</td><td>

-   **Background**

Mobile variable: `Primary`

Web variable: `now-color--primary-1`

-   **Text**

Mobile variable: `Text Actionable`

Web variable: `now-color_text--primary-actionable`


</td></tr><tr><td>

Secondary

</td><td>

\[Omitted image "button-secondary.png"\] Alt text: Secondary button example

</td><td>

-   **Background**

Mobile variable: `Background Primary`

Web variable: `now-color_background--primary`

-   **Text**

Mobile variable: `Primary`

Web variable: `now-color--primary-1`

-   **Border \(2px\)**

Mobile variable: `Primary`

Web variable: `now-color--primary-1`


</td></tr><tr><td>

Positive

</td><td>

\[Omitted image "button-positive.png"\] Alt text: Positive button example

</td><td>

-   **Background**

Mobile variable: `Positive`

Web variable: `now-color_alert--positive-3`

-   **Text**

Mobile variable: `Text Actionable`

Web variable: `now-color_text--primary-actionable`


</td></tr><tr><td>

Destructive

</td><td>

\[Omitted image "button-destructive.png"\] Alt text: Destructive button example

</td><td>

-   **Background**

Mobile variable: `Destructive`

Web variable: `now-color_alert--critical-3`

-   **Text**

Mobile variable: `Text Actionable`

Web variable: `now-color_text--primary-actionable`


</td></tr><tr><td>

Bare

</td><td>

\[Omitted image "button-bare.png"\] Alt text: Bare button example

</td><td>

-   **Background**

Mobile variable: `Primary`/`Positive`/`Destructive`

Web variable: `now-color--primary-1`/

`now-color_alert--positive-3`/

`now-color_alert--critical-3`

-   **Text**

Mobile variable: `Text Actionable`

Web variable: `now-color_text--primary-actionable`


 **Note:** This button can be configured with primary, positive, or destructive color.

</td></tr><tr><td>

Disabled

</td><td>

\[Omitted image "button-disabled.png"\] Alt text: Disabled button example

</td><td>

Use this style when the action is unavailable while offline.

 Can be used with all styles- primary, secondary, text/icon.

</td></tr></tbody>
</table>