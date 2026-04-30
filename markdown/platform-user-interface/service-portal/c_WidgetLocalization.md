---
title: Internationalize a widget
description: Use the $\{\} or gs.getMessage\(\) syntax in the HTML Template, Client Script, or Server Script fields of a widget to tag strings for translation so you can localize your Service Portal content.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Internationalize a widget

Use the `${}` or `gs.getMessage()` syntax in the **HTML Template**, **Client Script**, or **Server Script** fields of a widget to tag strings for translation so you can localize your Service Portal content.

The `${}` or `gs.getMessage()` searches in the messages table \[sys\_ui\_message\] in the platform to see what the translation would be.

Use the HTML template to internationalize strings in a widget. Type the following in an HTML template.

```
<div>
  <p>${This message will be internationalized.}</p>
  <p>However, this will NOT be.</p>
</div>
```

Writing text as `${message}` is the equivalent of writing `${gs.getMessage("message")}` in other parts of the system, but written as a more legible shorthand.

**Note:** In some cases, the translation might have quotes or double quotes on it. That could lead to JavaScript errors if you are using the $\{\} syntax in the client script. The safest way to fetch a translated message is to do it in the server script. Then, assign the value to a client-side Angular binding.

## Translating strings in the client script

```
function() {
  var c =this;
  c.message="${This message will be internationalized}";
}
```

HTML template:

```
<div>
  <!-- The output of this text will be internationalized. -->
  <p>{{c.message}}</p>
</div>
```

## Translating strings in the server script

Use the server script to translate schema options and other values during server-side runtime.

Server script

```
function() {  
  data.message=gs.getMessage("this message contains 'quotes'");
  //You can also translate schema options using the server script
  //For example, data.message=gs.getMessage(options.title);
}
```

HTML template

```
<div>  
  <p>{{c.data.message}}</p>
</div>
```

**Parent Topic:**[Developing custom widgets](widget-dev-guide.md)

