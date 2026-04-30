---
title: Supported wiki tags
description: Basic tags are supported for Wikitext fields in the system.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Wiki field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Supported wiki tags

Basic tags are supported for Wikitext fields in the system.

<table id="table_dfr_4zk_5q"><thead><tr><th>

Format

</th><th>

Wiki tag

</th></tr></thead><tbody><tr><td>

Headers

</td><td>

= Header 1 =, == Header 2 ==, etc.

</td></tr><tr><td>

Numbered step

</td><td>

\#Step 1

</td></tr><tr><td>

Bullets \(multi-level\)

</td><td>

\*Bullet 1, \*\*Bullet 2

</td></tr><tr><td>

Indentation

</td><td>

:Level 1, ::Level 2

</td></tr><tr><td>

Line break

</td><td>

&lt;br&gt;

</td></tr><tr><td>

Tables

</td><td>

Full table support, including cell spacing, padding, borders, background shading, and width measurements.

 For example:

```
{| class="wikitable"
|-
! Header 1
! Header 2
|-
| row 1, cell 1
| row 1, cell 2
|-
| row 2, cell 1
| row 2, cell 2
|}
```

 **Note:** Sortable tables are not supported \(class="sortable"\).

</td></tr><tr><td>

Code blocks

</td><td>

&lt;pre&gt; Generic block &lt;/pre&gt;

 &lt;javascript&gt; Javascript Syntax &lt;/javascript&gt;

 &lt;xml&gt; XML Syntax &lt;/xml&gt;

</td></tr><tr><td>

Bold

</td><td>

'''text'''

</td></tr><tr><td>

Italics

</td><td>

''text''

</td></tr><tr><td>

Ignore Wiki and HTML formatting

</td><td>

&lt;nowiki&gt; wikitext &lt;/nowiki&gt;

</td></tr><tr><td>

Web link

</td><td>

\[http://community.service-now.com/ &lt;link text&gt;\]

</td></tr><tr><td>

Placed images

</td><td>

\[\[Image:&lt;image name&gt;\]\] For more information on uploading images or files to the database, see [Storing images in the database](https://www.servicenow.com/docs/access?context=c_StoringImagesInTheDatabase&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

HTML

</td><td>

Most common HTML tags are supported

 &lt;b&gt;bold&lt;/b&gt;, &lt;strong&gt;strong&lt;/strong&gt;, &lt;i&gt;italics&lt;/i&gt;, &lt;h1&gt;header1&lt;/h1&gt;, &lt;h2&gt;header2&lt;/h2&gt;, &lt;h3&gt;header3&lt;/h3&gt;, &lt;p&gt;paragraph&lt;/p&gt;, &lt;sub&gt;sub&lt;/sub&gt;, &lt;sup&gt;sup&lt;/sup&gt;, &lt;center&gt;center&lt;/center&gt;

</td></tr></tbody>
</table>