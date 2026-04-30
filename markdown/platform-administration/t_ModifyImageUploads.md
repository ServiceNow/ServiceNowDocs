---
title: Disable user access to the image library for HTML area
description: By default, users can use and upload images to the image library from an HTML field. You can disable access to the image library from HTML fields. This is only applicable to HTML area and not TinyMCE.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Extended functions in HTML field editor, Configure the HTML toolbar, Configure a field editor for the HTML field, Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Disable user access to the image library for HTML area

By default, users can use and upload images to the image library from an HTML field. You can disable access to the image library from HTML fields. This is only applicable to HTML area and not TinyMCE.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **UI Pages**.

2.  Select **html\_insert\_image\_dialog**.

3.  Locate the following lines of code in the **HTML** field and comment them out.

    ```
    <g:evaluate var="jvar_use_dbimage">
    	var imageGR = new GlideRecord('db_image');
    	 if(imageGR.isValid())
    		imageGR.canRead();						  
    </g:evaluate>
    ```

    and

    ```
    <j:if test= "${jvar_write_dbimage}">
        <j:set var = "jvar_default_insert_image_type" value = "dbimage" />
        <g:ui_select_option text = "${gs.getMessage('Image Library')}" value = "dbimage" selected = "${jvar_default_insert_image_type}" />
    </j:if>
    ```

4.  Select **Update**.


## What to do next

To remove the **Upload from URL** option in the HTML editor, add a new property named **glide.ui.html.image.allow\_url** and set the **Value** to **false**.

**Parent Topic:**[Extended functions in HTML field editor](../../../use/using-forms/reference/r_ExtendedFunctions.md)

**Related topics**  


[Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#)

