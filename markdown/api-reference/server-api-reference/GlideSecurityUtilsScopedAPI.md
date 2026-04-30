---
title: GlideSecurityUtils - Scoped, Global
description: The GlideSecurityUtils API provides methods to work with URLs.Removes suspicious encoding to prevent reflected or DOM based cross site scripting.Removes the domain address from the URL, which leaves the page name and parameters.Add escape characters to a script.Check the specified URL against the system defined allow list.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSecurityUtils - Scoped, Global

The GlideSecurityUtils API provides methods to work with URLs.

Access these methods using the static object GlideSecurityUtils. This class is available in scoped and global scripts.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideSecurityUtils - cleanURL\(String url\)

Removes suspicious encoding to prevent reflected or DOM based cross site scripting.

|Name|Type|Description|
|----|----|-----------|
|url|String|The URL to be checked.|

|Type|Description|
|----|-----------|
|String|The URL stripped of problem elements.|

```
myurl='javascript%3Aalert(1)';
var clean=GlideSecurityUtils.cleanURL(myurl);
gs.info(clean);
```

Output: null

## GlideSecurityUtils - enforceRelativeURL\(String url\)

Removes the domain address from the URL, which leaves the page name and parameters.

|Name|Type|Description|
|----|----|-----------|
|url|String|The URL to be turned into a relative URL.|

|Type|Description|
|----|-----------|
|String|A relative URL.|

```
myurl='http://evildomain.com/test.do';
relativeURL=GlideSecurityUtils.enforceRelativeURL(myurl);
gs.info(relativeURL);
```

Output: test.do

## GlideSecurityUtils - escapeScript\(String script\)

Add escape characters to a script.

Adding escape characters to a script helps prevent cross-site scripting.

|Name|Type|Description|
|----|----|-----------|
|script|String|The script to have escape characters added.|

|Type|Description|
|----|-----------|
|String|The script with escape characters added.|

```
theScript="<script> alert(1)</script>";
var escapedScript=GlideSecurityUtils.escapeScript(theScript);
gs.info(escapedScript);
```

Output: `&lt;script&gt; alert(1)&lt;/script&gt;`

## GlideSecurityUtils - isURLWhiteListed\(String url\)

Check the specified URL against the system defined allow list.

|Name|Type|Description|
|----|----|-----------|
|url|String|The URL to be checked against the URL allow list.|

|Type|Description|
|----|-----------|
|Boolean|Returns true if the specified URL is in the allow list.|

```
myURL="http://evil.com/badscript.do";
isWhitelisted=GlideSecurityUtils.isURLWhiteListed(myURL);
gs.info(isWhitelisted);
```

Output: false

