---
title: CDM system properties
description: CDM system properties.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, DevOps Config, IT Service Management]
---

# CDM system properties

CDM system properties.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

## CDM system properties

<table id="table_y45_jxj_g5b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cdm.variable\_regex

</td><td>

The regex used to capture variables referenced in a CDI value. With this value, the syntax to use a variable is:

```
@@name@@
```

 Default: @@\(\[^@\].\*?\)@@

</td></tr><tr><td>

sn\_cdm.cdm\_queue\_request\_expiry\_time\_ms

</td><td>

The maximum time for a process to be available for processing before it is marked as expired.

 Default: 900000 ms \(15 min\)

</td></tr><tr><td>

sn\_cdm.cdm\_validation\_timeout\_ms

</td><td>

The maximum time limit for a validation of a snapshot.

Default: 900000 ms \(15 min\)

</td></tr><tr><td>

sn\_cdm.default\_node\_identifier\_keys

</td><td>

The keys used to identify node objects within an array node.

 Default: \(none\)

</td></tr><tr><td>

sn\_cdm.execute\_exporter\_async\_for\_standard\_request

</td><td>

If set to `false`, exporter requests skip the request queue and their output is returned immediately. Changing this setting may decrease system performance if there are many export requests.

 Default: true

</td></tr><tr><td>

sn\_cdm.exception\_enabled

</td><td>

If set to false, the control exception functionality is disabled regardless of other policy settings.

 Default: true

</td></tr><tr><td>

sn\_cdm.node\_name\_allowed\_character\_regex

</td><td>

The regex used to validate the name of a node. Default allowed characters are:

```
0-9, A-Z, a-z, _, -, ., %, $, whitespace, :, #
```

 Default: `[\\w-.% :$#]`

</td></tr><tr><td>

sn\_cdm.app\_name\_allowed\_character\_regex

</td><td>

The regex used to validate the name of an application. Default allowed characters are:

```
0-9, A-Z, a-z, _,-, ., whitespace, |, :, [], (), %, $, #
```

 Default: `[\\w-.%$#() :|[\\]]`

</td></tr><tr><td>

sn\_cdm.snapshot\_name\_allowed\_character\_regex

</td><td>

The regex used to validate the name of a snapshot. Default allowed characters are:

```
0-9, A-Z, a-z, _,-, ., %
```

 Default: `[\\w-.%]`

</td></tr><tr><td>

sn\_cdm.exporter\_name\_allowed\_character\_regex

</td><td>

The regex used to validate the name of an exporter. Default allowed characters are:

```
0-9, A-Z, a-z, _,-, .,%
```

 Default: `[\\w-.%]`

</td></tr><tr><td>

sn\_cdm.exporter\_argument\_name\_allowed\_character\_regex

</td><td>

The regex used to validate the name of an exporter argument. Default allowed characters are:

```
0-9, A-Z, a-z, _
```

 Default: `[\\w]`

</td></tr><tr><td>

sn\_cdm.cdm\_max\_allowed\_open\_changesets

</td><td>

The maximum allowed number of open changesets.

 Default: 10

</td></tr><tr><td>

sn\_cdm.preventative\_duplicate\_node\_name\_check

</td><td>

If set to true, validating for node name duplication will check name usage across all other open changesets as well \(as opposed to limiting the check within the changeset\).

 Default: false

</td></tr><tr><td>

sn\_cdm.max\_allowed\_upload\_file\_size

</td><td>

The maximum payload size for upload of config data via the REST API.

 Default: 5 MB

</td></tr><tr><td>

sn\_cdm.max\_allowed\_cdi\_per\_application

</td><td>

The maximum number of CDIs allowed per application. If the number is exceeded, further upload of config data via the REST APIs is blocked.

 Increasing this limit may significantly decrease performance and break UI functionality. If you change the value, you must recalculate the CDI usage data by running the following command:

 ```
new sn_cdm.CdmApplicationManager().updateCdiCountOfApplications();
```

 Default: 100000

</td></tr><tr><td>

sn\_cdm.max\_allowed\_cdi\_per\_deployable

</td><td>

The maximum number of CDIs allowed per deployable. If the number is exceeded, further upload of config data via the REST APIs is blocked.

 Increasing this limit may significantly decrease performance and break UI functionality. If you change the value, you must recalculate the CDI usage data by running the following command:

 ```
new sn_cdm.CdmApplicationManager().updateCdiCountOfApplications();
```

 Default: 10000

</td></tr><tr><td>

sn\_cdm.max\_nodes\_in\_memory

</td><td>

The maximum number of nodes that can be supported when using the `queryTree` method of `CdmQuery`.

 Default: 10000

</td></tr><tr><td>

sn\_cdm.reserved\_node\_names

</td><td>

Names that cannot be used for nodes.

 Default: vars, collections, deployables, components

</td></tr><tr><td>

sn\_cdm.max\_allowed\_cdi\_per\_shared\_component

</td><td>

The maximum number of CDIs allowed per shared component. If the number is exceeded, further upload of config data via the REST APIs is blocked.

 Increasing this limit may significantly decrease performance and break UI functionality. If you change the value, you must recalculate the CDI usage data by running the following command:

 ```
new sn_cdm.CdmApplicationManager().updateCdiCountOfApplications();
```

 Default: 10000

</td></tr><tr><td>

sn\_cdm.max\_allowed\_cdi\_per\_library

</td><td>

The maximum number of CDIs allowed per shared component library. If the number is exceeded, further upload of config data via the REST APIs is blocked.

 Increasing this limit may significantly decrease performance and break UI functionality. If you change the value, you must recalculate the CDI usage data by running the following command:

 ```
new sn_cdm.CdmApplicationManager().updateCdiCountOfApplications();
```

 Default: 10000

</td></tr><tr><td>

sn\_cdm.attachment.display\_mime\_types

</td><td>

File types for which the content preview is available on the Preview pane.

 You can add additional MIME types to display in the Preview pane. However, the preview is not available for binary file MIME types, such as audio, image, and video.

 Default: `text/yaml,text/css,text/csv,text/html,text/javascript,text/plain,text/richtext,text/x-vcard,text/x-vcalendar,application/xml,application/javascript,application/json`

</td></tr></tbody>
</table>