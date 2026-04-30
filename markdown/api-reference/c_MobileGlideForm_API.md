---
title: Mobile GlideForm \(g\_form\) - Client
description: The Mobile GlideForm \(g\_form\) API provides methods to work with forms on the mobile platform.Adds a decorative icon next to a field.Gets the form label text.Determines if a field is present on the form.Removes a decorative icon from next to a field.Sets the form label text.
locale: en-US
release: xanadu
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# Mobile GlideForm \(g\_form\)- Client

The Mobile GlideForm \(g\_form\) API provides methods to work with forms on the mobile platform.

Use these methods in any script that targets a mobile device.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## MobileGlideForm \(g\_form\) - addDecoration\(String fieldName, String icon, String text\)

Adds a decorative icon next to a field.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The field name.|
|icon|String|The font icon to show next to the field.|
|text|String|The text title for the icon \(used for screen readers\).|

|Type|Description|
|----|-----------|
|void| |

This example adds a VIP icon next to the caller.

```
function onChange(control, oldValue, newValue, isLoading) {
      // if the caller_id field is not present, then we can't add an icon anywhere
      if (!g_form.hasField('caller_id'))
          return;
      
      if (!newValue)
         return;
      
      g_form.getReference('caller_id', function(ref) {
      g_form.removeDecoration('caller_id', 'icon-star', 'VIP');
      
      if (ref.getValue('vip') == 'true')
           g_form.addDecoration('caller_id', 'icon-star', 'VIP');			
      });
      }
```

## MobileGlideForm \(g\_form\) - getLabel\(String fieldName\)

Gets the form label text.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The field name.|

|Type|Description|
|----|-----------|
|String|The label text.|

```
if (g_user.hasRole('itil')) {
      var oldLabel = g_form.getLabel('comments');
      g_form.setLabel('comments', oldLabel + ' (Customer visible)');
      }
```

## MobileGlideForm \(g\_form\) - hasField\(String fieldName\)

Determines if a field is present on the form.

Present means that it can be shown, not that it is visible.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The field to look for.|

|Type|Description|
|----|-----------|
|Boolean|True if the field is present on the form; false, if it is not. On the form means that the field is part of g\_form. It could still be hidden, read-only, mandatory, or invalid.|

This example makes the assigned\_to field mandatory if the assignment\_group field is on the form.

```
if (g_form.hasField('assignment_group'))
      g_form.setMandatory('assigned_to', true);
    
```

## MobileGlideForm \(g\_form\) - removeDecoration\(String fieldName, String icon, String text\)

Removes a decorative icon from next to a field.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The field name.|
|icon|String|The icon to remove.|
|text|String|The text title for the icon.|

|Type|Description|
|----|-----------|
|void| |

```
function onChange(control, oldValue, newValue, isLoading) {
      // if the caller_id field is not present, then we can't add an icon anywhere
      if (!g_form.hasField('caller_id'))
           return;
      
      if (!newValue)
           return;
      
      g_form.getReference('caller_id', function(ref) {
           g_form.removeDecoration('caller_id', 'icon-star', 'VIP');
      
           if (ref.getValue('vip') == 'true')
                g_form.addDecoration('caller_id', 'icon-star', 'VIP');			
      });
      }
```

## MobileGlideForm \(g\_form\) - setLabel\(String fieldName, String label\)

Sets the form label text.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The field name.|
|label|String|The field label text.|

|Type|Description|
|----|-----------|
|void| |

This example changes the comments label.

```
if (g_user.hasRole('itil')) {
      var oldLabel = g_form.getLabel('comments');
      g_form.setLabel('comments', oldLabel + ' (Customer visible)');
      }
```

