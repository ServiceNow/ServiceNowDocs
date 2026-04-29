---
title: Configure portal branding
description: Use Branding Editor to give your portal its own look and feel.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Defining portal styles, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configure portal branding

Use Branding Editor to give your portal its own look and feel.

To access the Branding Editor, navigate to **Service Portal** &gt; **Service Portal Configuration**, then click **Branding Editor**.

Select the portal you want to customize the theme for from the portal list. Then use the options on the Quick Setup and Theme Colors tabs to customize your portal.

![Branding Editor](../image/BrandEditor.png "Branding Editor")

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

Where you want the logo to sit in location to the edge of the header. This information is stored in the CSS variables section on the portal form.

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

Add a color for your background. You can type in a color name, hex color, decimal \(RGB\), or select from the color palate.

</td></tr><tr><td>

Background image

</td><td>

Upload an image to appear in the background of your homepage. This image is stored in the container for the widget on your homepage.

</td></tr></tbody>
</table>For any colors on the theme tab, you can use the standard color name, hex code, decimal \(RGB\) code, or select the color from the color palate. All the color definitions are stored in the CSS variables field of the portal form. The theme preview updates in real time as you make changes.

|Field|Description|
|-----|-----------|
|Navbar|Use the fields in this section to customize the colors for the header menu.|
|Brand|Use the fields in this section to customize the page colors. For example, the page background or the widget background.|
|Text|Use the fields in this section to customize the color of the text on a page.|

Changes made to the theme colors in the Branding Editor appear in the CSS variables field of the portal form in the platform UI.

**Parent Topic:**[Defining portal styles](portal-css.md)

