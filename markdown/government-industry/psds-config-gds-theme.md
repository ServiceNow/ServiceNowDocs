---
title: Configure the GOV.UK Design System Service Portal theme
description: Use the Branding Editor to give the GDS Service Portal its own look and feel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-gds-theme.html
release: australia
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 3
breadcrumb: [Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the GOV.UK Design System Service Portal theme

Use the Branding Editor to give the GDS Service Portal its own look and feel.

By default, the GOV.UK Design System Service Portal theme looks like:

\[Omitted image "image.psds\_gds\_default\_theme"\] Alt text: GDS Portal Default Theme.

You can customize the default GDS Service Portal theme to suit your needs using the Branding Editor. To access the Branding Editor, navigate to **Service Portal** &gt; **Service Portal Configuration**, then select **Branding Editor**.

From the portal list, select **UK Government Portal**, and use the options on the Quick Setup and Theme Colors tabs to customize the portal.

Branding Editor

\[Omitted image "psds\_gds\_branding\_editor.png"\] Alt text: GDS Portal Branding Editor.

<table id="table_bq1_v4h_2z"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Portal Title

</td><td>

The name of your portal. Changing the name of the portal in the Branding Editor also changes the title on the portal form field in the platform UI.

</td></tr><tr><td>

Logo

</td><td>

The logo that appears in the header for your portal. This image is scaled to a maximum height of 46 px and a maximum width of 200 px.

</td></tr><tr><td>

Logo padding

</td><td>

Where you want the logo to sit in relation to the edge of the header. This information is stored in the CSS variables section on the portal form.

</td></tr><tr><td>

Tag line &amp; background

</td><td>

Fields defined by the JSON schema in the **Quick start config** field on the portal record in the platform UI. The sample Service Portal adds **Tag Line** and **Background** to the Branding Editor using the following schema:

```
[{
	"tagline": {
		"table" : "sp_instance",
		"sys_id" : "34fe3d96cb20020000f8d856634c9cf4",
		"field" : "title"
	},
	"hero_background": {
		"table" : "sp_container",
		"sys_id" : "be98a8d2cb20020000f8d856634c9c63",
		"field" : "background_image"
	}
}]
```

For more information on editing the portal from the portal record page, see [Configure the GOV.UK Design System Service Portal record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gds-portal-record.md).

</td></tr><tr><td>

Tag line

</td><td>

Introduce your users to a portal page with a tag line. This text is stored in an instance of the homepage search widget.

</td></tr><tr><td>

Tag line color

</td><td>

Select a color for the tag line.

</td></tr><tr><td>

Homepage background color

</td><td>

Add a color for your background. You can type in a color name, hex color, decimal \(RGB\), or select from the color palette.

</td></tr><tr><td>

Background image

</td><td>

Upload an image to appear in the background of your homepage. This image is stored in the container for the widget on your homepage.

</td></tr></tbody>
</table>The default theme for the GDS Service Portal employs Gov.UK design system standards, and includes the official Gov.UK color palette \(primary, secondary, background, text colors\). To choose other colors, navigate to the Theme colors tab. The theme preview updates as you make changes. Changes made to the theme colors in the Branding Editor appear in the CSS variables field of the portal form in the platform UI.

## Add a header or footer

To add a header or footer to your portal, you must configure it through the theme of the portal.

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration** &gt; **Portal Tables** &gt; **Themes**.
2.  Select the theme you want to add the header or footer to.
3.  In the header or footer field, select the header or footer you want to use for your portal.

    By default, the toolkit provides a GDS-compliant base system Stock Header or Sample Footer widgets that you may select for reuse.

4.  Optional: Select **Fixed Header** or **Fixed Footer** to lock the header or footer in one place so when users scroll up or down they remain in the same location on the page.
5.  To configure the appearance of the header, in the Service Portal configuration page, open the Branding Editor.
6.  Under the **Theme Colors** tab, use the color selectors in the Navbar section to control the colors in the header.

For information on creating and customizing the header/footer menu, see [Create a portal header menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-header-menu.md).

## Customizing the Portal CSS

Changes made in the Branding Editor or to specific components of the portal \(such as a widget or a page container\) override any customizations made to the theme. If your portal needs more customization than Branding Editor can provide, you can edit the CSS of the existing theme. For information on how to customize the portal theme using CSS, see [Create a portal theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_CustomCSS.md).

**Parent Topic:**[Configure the GOV.UK Design System \(GDS\) Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gds-content-pack-gsp.md)

