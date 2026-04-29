---
title: Controls in Virtual Agent API
description: Virtual Agent API provides you various controls to manage the responses in your conversation.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Use, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Controls in Virtual Agent API

Virtual Agent API provides you various controls to manage the responses in your conversation.

The available controls in Virtual Agent API are:

## Output Text

```
{
  "uiType": "OutputText",
  "group": "DefaultText",
  "value": "**bold**\n*italic*\n***bold italic***\n[Google](https://empcygiraffe6.service-now.com/va_link.do?token=77ee77ef77eSZGFlMTc3OWU5NzY2MTExMDUyNjFiMzQ3MTE1M2FmYjTvt6zvt5Qx77es77etWE1nS0ZLOElhU1FQYzhIajh2dmNmZz09WHdPTDYzV3ZpUWF1MGJwRlB0ZktUY29wVWt1UGVueUNIS1FkRHRyUW9idHlmVFZlRWJOODZyRjZYN0VQamxnWUV5WkhZSDRJaWFGWmJRZU1CaXZLYWhudnkwbDdvNFZsMlMzUUw4Q3VRTUJWMHhvTWlRLXZOQnh5M0hveVBuellNVmJCbGlka0RqNTAzVFVUQml0MTZzSnlUTVJoakdZektldXdoYXlM77eu77ev&target_url=https%3A%2F%2Fwww.google.co.in)\n\n- ***ul1***\n- ***ul2***\n\n\n1. ol1\n2. ol2\n\n",
  "maskType": "NONE | SECURE"
}
```

|Field|Description|
|-----|-----------|
|value|Contains the output text value.|
|maskType|'NONE' indicates normal text and 'SECURE' indicates secure output text.|

## Output Html

```
{
  "uiType": "OutputHtml",
  "group": "DefaultOutputHtml",
  "style": "inline",
  "height": 0,
  "width": 0,
  "value": "<html>     <body>     <table>   <tr>     <th>Company</th>     <th>Contact</th>     <th>Country</th>   </tr>   <tr>     <td><a href=\"https://www.google.co.in\">Alfreds Futterkiste</a></td>     <td>Maria Anders</td>     <td>Germany</td>   </tr>   <tr>     <td>Centro comercial Moctezuma</td>     <td>Francisco Chang</td>     <td>Mexico</td>   </tr>   <tr>     <td><a href=\"https://www.google.co.in\">Ernest Handel</a></td>     <td>Roland Mendel</td>     <td>Austria</td>   </tr>   <tr>     <td>Island Trading</td>     <td>Helen Bennett</td>     <td>UK</td>   </tr>   <tr>     <td>Laughing Bacchus Winecellars</td>     <td>Yoshi Tannamuri</td>     <td><a href=\"https://www.google.co.in\">Canada</a></td>   </tr>   <tr>     <td>Magazzini Alimentari Riuniti</td>     <td>Giovanni Rovelli</td>     <td>Italy</td>   </tr> </table>     </body> </html> ",
  "imageUrl": "https://empcygiraffe6.service-now.com//api/now/v1/cs/media/zKFqUx0NJyVaFRJqzeRhFgeMsMo9211mCvrMgKzrRpTWqFJDrXLOadoYGC5CQnwr",
  "imageHeight": 217,
  "imageWidth": 501,
  "links": [
    {
      "link": "https://www.google.co.in",
      "label": "Alfreds Futterkiste"
    },
    {
       "link": "https://www.google.co.in",
       "label": "Ernest Handel"
    },
    {
       "link": "https://www.google.co.in",
       "label": "Canada"
    }
  ]
}
```

|Field|Description|
|-----|-----------|
|value|Contains the html value.|
|imageUrl|Contains the image of html if 'Html to image conversion required' is enabled on sys\_cs\_provider.|
|imageHeight|Contains the image height if 'Html to image conversion required' is enabled on sys\_cs\_provider.|
|imageWidth|Contains the image width if 'Html to image conversion required' is enabled on sys\_cs\_provider.|
|links|Contains links in the given html if 'Html to image conversion required' is enabled on sys\_cs\_provider.|

## Output Image

```
{
  "uiType": "OutputImage",
  "group": "DefaultOutputImage",
  "value": "https://adaptivecards.io/content/cats/1.png",
  "altText": "Image alt text"
 }
```

|Field|Description|
|-----|-----------|
|value|Contains the image url.|
|altText|Contains the alt text for the image \(not mandatory\).|

## Output Link

```
{
  "uiType": "OutputLink",
  "group": "DefaultOutputLink",
  "label": "ServiceNow",
  "header": "The world works with ServiceNow",
  "type": "link",
  "value": {
    "action": "https://empcygiraffe6.service-now.com/va_link.do?token=<token>&target_url=https%3A%2F%2Fwww.servicenow.com",
    "target": "_blank"
  }
}
```

|Field|Description|
|-----|-----------|
|header|Link Header|
|label|Link label|
|value-&gt;action|Link url|

## Multi Link

```
{
  "uiType": "GroupedPartsOutputControl",
  "group": "DefaultGroupedPartsOutputControl",
  "groupPartType": "Link",
  "header": "Multilink Header",
  "values": [
    {
      "action": "https://empcygiraffe6.service-now.com/va_link.do?token=<token>&target_url=https%3A%2F%2Fwww.link1.com",
      "description": "a short desc",
      "label": "link 1 label",
      "context": "KB",
      "target": "_blank"
    },
    {
      "action": "https://empcygiraffe6.service-now.com/va_link.do?token=<token>&target_url=https%3A%2F%2Fwww.link2.com",
      "description": "a short desc",
      "label": "link 2 label",
      "context": "ITSM",
      "target": "_blank"
    }
  ]
}
```

|Field|Description|
|-----|-----------|
|header|MultiLink control header|
|values|Links array|

**Link structure in links array:**

|Field|Description|
|-----|-----------|
|label|Link label|
|action|Link url|
|description|Link Description|
|context|Context or Taxonomy|

## Output Card

```
{
  "uiType": "OutputCard",
  "group": "DefaultOutputCard",
  "templateName": "<card-template>",
  "data": "<card-data-json>",
}
```

<table id="table_oxm_4jv_d3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

templateName

</td><td>

Card type or Card name

</td></tr><tr><td>

data

</td><td>

json representing card data.**Note:** The data field will be of type string. You need to parse it to use the data.

</td></tr></tbody>
</table>**Large Image With Text**

```
{
  "uiType": "OutputCard",
  "group": "DefaultOutputCard",
  "templateName": "Large image with text",
  "data": "{\"image\":\"https://adaptivecards.io/content/cats/1.png\",\"description\":\"Large image description\", \"dataNowSmartLink\":\"W9F4Ld8z\",\"title\":\"Large image\",\"imageAlt\":\"large image alt text\",\"url\":\"\",\"target\":\"_blank\"}",
  "smartLinksMetadata": {
    "W9F4Ld8z": {
      "type": "standard",
      "source": "",
      "target": "_blank"
    }
  }
}
```

**Small Image With Text**

```
{
  "uiType": "OutputCard",
  "group": "DefaultOutputCard",
  "templateName": "Small image with text",
  "data": "{\"image\":\"https://adaptivecards.io/content/cats/1.png\",\"description\":\"Small image with text description\",\"dataNowSmartLink\":\"i6CL61tN\",\"title\":\"Small image with text\",\"imageAlt\":\"small image alt text\",\"url\":\"\",\"target\":\"_blank\"}",
  "smartLinksMetadata": {
     "i6CL61tN": {
       "type": "standard",
       "source": "",
       "target": "_blank"
     }
  }
}
```

**Youtube**

```
{
  "uiType": "OutputCard",
  "group": "DefaultOutputCard",
  "templateName": "Youtube Video Card",
  "data": "{\"link\":\"https://empcygiraffe6.service-now.com/va_link.do?token=<token>&target_url=servicenow.com\",\"description\":\"The world works with ServiceNow\",\"id\":\"IWsGk-Kh5ko\",\"title\":\"ServiceNow\",\"url\":\"\",\"target\":\"_blank\"}"
}
```

**Record**

```
{
  "uiType": "OutputCard",
  "group": "DefaultOutputCard",
  "templateName": "Card",
  "data": "{\"sys_id\":\"0c5f3cece1b12010f877971dea0b1449\",\"subtitle\":\"INC0008001\",\"dataNowSmartLink\":\"VLzQTN88\",\"title\":\"Incident\",\"fields\":[{\"fieldLabel\":\"Number\",\"fieldValue\":\"INC0008001\"},{\"fieldLabel\":\"Short description\",\"fieldValue\":\"ATF:TEST2\"},{\"fieldLabel\":\"Caller\",\"fieldValue\":\"survey user\"}],\"table_name\":\"incident\",\"url\":\"https://empcygiraffe6.service-now.com/va_link.do?token=<token>target_url=https%3A%2F%2Fempcygiraffe6.service-now.com%2Fsp%3Fsys_id%3D0c5f3cece1b12010f877971dea0b1449%26id%3Dticket%26table%3Dincident\",\"target\":\"_blank\"}",
  "smartLinksMetadata": {
    "VLzQTN88": {
      "type": "standard",
      "source": "https://empcygiraffe6.service-now.com/sp?sys_id=0c5f3cece1b12010f877971dea0b1449&id=ticket&table=incident",
      "target": "_blank"
    }
  }
}
```

## Multipart Output

```
{
  "uiType": "MultiPartOutput",
  "group": "DefaultMultiPartOutput",
  "navigationBtnLabel": "Click for more",
  "content": {
    "uiType": "OutputText",
    "value": "multipart text output",
    "maskType": "NONE"
  }
}
```

<table id="table_rvm_bmv_d3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

navigationBtnLabel

</td><td>

Navigation Button label

</td></tr><tr><td>

content

</td><td>

Represents the control defined with multipart.**Note:**

-   Content can be OutputText or OutputImage or OutputHtml or OutputLink or OutputCard.
-   You must send 'click\_for\_more' as response to move to the next part.

</td></tr></tbody>
</table>## InputText

```
{
  "uiType": "InputText",
  "group": "DefaultText",
  "required": true,
  "nluTextEnabled": false,
  "entityType": "Text",
  "label": "enter something",
  "maskType": "NONE"
}
```

<table id="table_wj5_nmv_d3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

Input text label

</td></tr><tr><td>

required

</td><td>

True or false that indicates whether the control can be skipped or not.

</td></tr><tr><td>

maskType

</td><td>

NONE or SECURE.-   NONE indicates normal input.
-   SECURE indicates secure input.

</td></tr><tr><td>

entityType

</td><td>

The input is text or email or IP address.

</td></tr><tr><td>

nluTextEnabled

</td><td>

Whether nlu is enabled at this node or not.

</td></tr></tbody>
</table>## Boolean

```
{
  "uiType": "Boolean",
  "group": "DefaultPicker",
  "required": true,
  "nluTextEnabled": false,
  "entityType": "Boolean",
  "label": "select yes/no",
  "options": [
    {
       "label": "Yes",
       "value": "yes",
       "renderStyle": "data"
    },
    {
       "label": "No",
       "value": "no",
       "renderStyle": "data"
    }
  ]
}
```

<table id="table_g2w_fnv_d3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

Boolean control prompt

</td></tr><tr><td>

required

</td><td>

True or false that indicates whether the control can be skipped or not.

</td></tr><tr><td>

maskType

</td><td>

NONE or SECURE.-   NONE indicates normal input.
-   SECURE indicates secure input.

</td></tr><tr><td>

entityType

</td><td>

Boolean

</td></tr><tr><td>

nluTextEnabled

</td><td>

Whether NLU is enabled at this node or not.

</td></tr><tr><td>

options

</td><td>

Boolean options

</td></tr></tbody>
</table>**Option structure in options array:**

|Field|Description|
|-----|-----------|
|label|Option label|
|value|Option value|
|renderStyle|Data or button|

## Picker

```
{
  "uiType": "Picker",
  "group": "DefaultPicker",
  "required": true,
  "nluTextEnabled": false,
  "label": "Select an option",
  "itemType": "List",
  "style": "list",
  "multiSelect": false,
  "options": [
    {
      "label": "option 1",
      "value": "option 1",
      "renderStyle": "data",
      "enabled": false
    },
    {
      "label": "option 2",
      "value": "option 2",
      "renderStyle": "data",
      "enabled": false
    },
    {
      "label": "option 3",
      "value": "option 3",
      "renderStyle": "data",
      "enabled": false
    }
  ],
  "scriptedData": {
    "cardData": "{\"title\":\"Choice - Large image with text\",\"description\":\"Choice - Large image with text description\",\"image\":\"https://adaptivecards.io/content/cats/1.png\",\"imageAlt\":\"alt text\"}",
    "cardName": "Large image with text",
    "cardTemplate": "",
    "renderStyle": "card"
  }
}
```

<table id="table_cgz_d4v_d3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

Picker control prompt

</td></tr><tr><td>

style

</td><td>

List or carousel. Carousel indicates carousel control.

</td></tr><tr><td>

required

</td><td>

True or false that indicates whether the control can be skipped or not.

</td></tr><tr><td>

maskType

</td><td>

NONE or SECURE.-   NONE indicates normal input.
-   SECURE indicates secure input.

</td></tr><tr><td>

entityType

</td><td>

Boolean

</td></tr><tr><td>

nluTextEnabled

</td><td>

Whether NLU is enabled at this node or not.

</td></tr><tr><td>

options

</td><td>

Boolean options

</td></tr><tr><td>

scriptedData

</td><td>

Represents a card to be displayed along with picker.

</td></tr></tbody>
</table>**Option structure in options array:**

|Field|Description|
|-----|-----------|
|label|Option label|
|value|Option value|
|renderStyle|data or button|

**scriptedData structure:**

|Field|Description|
|-----|-----------|
|cardName|Template name|
|cardData|Card data as json string.|

## Carousel

```
{
  "uiType": "Picker",
  "group": "DefaultPicker",
  "required": true,
  "nluTextEnabled": false,
  "label": "select an image",
  "itemType": "Picture",
  "style": "carousel",
  "multiSelect": false,
  "options": [
    {
       "label": "name1",
       "description": "a description of value_1 item",
       "attachment": "https://adaptivecards.io/content/cats/1.png",
       "value": "value_1",
       "renderStyle": "data",
       "enabled": false
    },
    {
       "label": "name2",
       "description": "a description of value_2 item",
       "attachment": "https://adaptivecards.io/content/cats/1.png",
       "value": "value_2",
       "renderStyle": "data",
       "enabled": false
    },
    {
       "label": "name3",
       "description": "a description of value_3 item",
       "attachment": "https://adaptivecards.io/content/cats/1.png",
       "value": "value_3",
       "renderStyle": "data",
       "enabled": false
    }
  ],
  "scriptedData": null
}
```

<table id="table_rq3_gpv_d3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

Picker control prompt

</td></tr><tr><td>

style

</td><td>

List or Carousel. Carousel indicates carousel control.

</td></tr><tr><td>

required

</td><td>

True or false that indicates whether the control can be skipped or not.

</td></tr><tr><td>

maskType

</td><td>

NONE or SECURE.-   NONE indicates normal input.
-   SECURE indicates secure input.

</td></tr><tr><td>

entityType

</td><td>

Boolean

</td></tr><tr><td>

nluTextEnabled

</td><td>

Whether NLU is enabled at this node or not.

</td></tr><tr><td>

options

</td><td>

Boolean options

</td></tr></tbody>
</table>**Option structure in options array:**

|Field|Description|
|-----|-----------|
|label|Option label|
|value|Option value|
|description|description for the option|
|attachment|Picture or image for the option|

## Date

```
{
  "uiType": "Date",
  "group": "DefaultDate",
  "required": true,
  "nluTextEnabled": false,
  "entityType": "Date",
  "label": "test date"
}
```

|Field|Description|
|-----|-----------|
|label|Date control prompt|
|required|True or false that indicates whether the control can be skipped or not.|
|entityType|Date|
|nluTextEnabled|Whether NLU is enabled at this node or not.|

## Time

```
{
  "uiType": "Time",
  "group": "DefaultDate",
  "required": true,
  "nluTextEnabled": false,
  "entityType": "Time",
  "label": "Select time"
}
```

|Field|Description|
|-----|-----------|
|label|Time control prompt|
|required|True or false that indicates whether the control can be skipped or not.|
|entityType|Time|
|nluTextEnabled|Whether NLU is enabled at this node or not.|

## DateTime

```
{
  "uiType": "DateTime",
  "group": "DefaultDate",
  "required": true,
  "nluTextEnabled": false,
  "entityType": "Time",
  "label": "Select time"
}
```

|Field|Description|
|-----|-----------|
|label|Date and Time control prompt|
|required|True or false that indicates whether the control can be skipped or not.|
|entityType|Time|
|nluTextEnabled|Whether NLU is enabled at this node or not.|

## StartConversation

```
{
  "uiType": "ActionMsg",
  "actionType": "StartConversation",
  "conversationId": "e0494b2187332550326d0d05dabb350d"
}
```

|Field|Description|
|-----|-----------|
|uiType|ActionMsg|
|actionType|StartConversation|

Indicates that the conversation has started in Virtual Agent API.

**Parent Topic:**[Using Virtual Agent API](use-virtual-agent-api.md)

