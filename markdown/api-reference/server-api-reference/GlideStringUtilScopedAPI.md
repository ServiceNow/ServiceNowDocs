---
title: GlideStringUtil - Scoped, Global
description: The GlideStringUtil API provides string handling methods.Replaces periods with underscore characters.Removes quotes from a string.Replaces problem characters with escape characters.Replaces illegal characters with their escape codes.Replaces non-printable characters with their printable notation.Replaces query term separators "^" with their escape sequence "^^".Replaces quotes with escape characters by adding a backslash before each quote.Replaces illegal HTML characters into HTML notation.Extracts numeric characters from a string.Validates whether the specified string is a valid base64 string.Validates whether the specified string is in valid sys\_id format.Replaces the new line character, /n, with a break code, &lt;br/&gt;.Replaces carriage returns, line feeds, and tabs with spaces, and then removes leading, trailing, and duplicate spaces.Replaces escape characters with their respective character.Encodes non-ASCII characters, unsafe ASCII characters, and spaces so you can use the returned string on the Internet. Uses UTF-8 encoding. Uses percent \(%\) encoding.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideStringUtil - Scoped, Global

The GlideStringUtil API provides string handling methods.

Access these methods using the static object GlideStringUtil. This class is available in scoped and global scripts.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideStringUtil - dotToUnderBar\(String sourceString\)

Replaces periods with underscore characters.

|Name|Type|Description|
|----|----|-----------|
|sourceString|String|Text to process.|

|Type|Description|
|----|-----------|
|String|Text with periods replaced with underscores.|

```
var filename="../../../../../../etc/passwd";
cleanFilename=GlideStringUtil.dotToUnderBar(filename);
gs.info(cleanFilename);
```

Output:

```
 __/__/__/__/__/__/etc/passwd
```

## GlideStringUtil - escapeAllQuotes\(String sourceString\)

Removes quotes from a string.

|Name|Type|Description|
|----|----|-----------|
|sourceString|String|The string to be processed.|

|Type|Description|
|----|-----------|
|String|The string with quotes removed.|

```
mystring="let's escape some quotes";
escapeQuote=GlideStringUtil.escapeAllQuotes(mystring);
gs.info(escapeQuote);
```

Output:

```
lets escape some quotes
```

## GlideStringUtil - escapeForHomePage\(String sourceString\)

Replaces problem characters with escape characters.

|Name|Type|Description|
|----|----|-----------|
|sourceString|String|Text to process.|

|Type|Description|
|----|-----------|
|String|Text with problem characters replaced with escape characters.|

```
mystring="<test> string \n to escape";
escapedString=GlideStringUtil.escapeForHomePage(mystring);
gs.info(escapedString);
```

Output:

```
%3ctest%3e string \n to escape
```

## GlideStringUtil - escapeHTML\(String htmlString\)

Replaces illegal characters with their escape codes.

Using this method removes illegal characters that might cause the UI to render improperly, or trigger a client side attack such as JavaScript or HTML injection.

|Name|Type|Description|
|----|----|-----------|
|htmlString|String|Text to process.|

|Type|Description|
|----|-----------|
|String|Text with illegal characters replaced with their escape codes.|

```
mydata='"<>&';
mydata=GlideStringUtil.escapeHTML(mydata);
gs.info(mydata);
```

Output:

```
&quot;&lt;&gt;&amp;
```

## GlideStringUtil - escapeNonPrintable\(String sourceString\)

Replaces non-printable characters with their printable notation.

|Name|Type|Description|
|----|----|-----------|
|sourceString|String|Text to process.|

|Type|Description|
|----|-----------|
|String|Text with non-printable characters replaced with printable notation.|

```
mystring="test \x09 non \x00 printable \x07 chars";
escapedString=GlideStringUtil.escapeNonPrintable(mystring);
gs.info(escapedString);
```

Output:

```
test \t non \u0000 printable \u0007 chars
```

## GlideStringUtil - escapeQueryTermSeparator\(String sourceString\)

Replaces query term separators "^" with their escape sequence "^^".

|Name|Type|Description|
|----|----|-----------|
|sourceString|String|Text to process.|

|Type|Description|
|----|-----------|
|String|Text with query term separators replaced with the escape characters.|

```
myquery="test^Test";
escapedQuery=GlideStringUtil.escapeQueryTermSeparator(myquery);
gs.info(escapedQuery);
```

Output:

```
test^^Test
```

## GlideStringUtil - escapeTicks\(String sourceString\)

Replaces quotes with escape characters by adding a backslash before each quote.

|Name|Type|Description|
|----|----|-----------|
|sourceString|String|Text to process.|

|Type|Description|
|----|-----------|
|String|Text with backslashes added before quotes.|

```
mystring="let's try escapeTicks";
escaped=GlideStringUtil.escapeTicks(mystring);
gs.info(escaped); 
```

Output:

```
let\'s try escapeTicks
```

## GlideStringUtil - getHTMLValue\(String sourceString\)

Replaces illegal HTML characters into HTML notation.

Using this method removes illegal characters that might cause the UI to render improperly, or trigger a client side attack such as JavaScript or HTML injection.

|Name|Type|Description|
|----|----|-----------|
|sourceString|String|Text to process.|

|Type|Description|
|----|-----------|
|String|Text with illegal characters replaced with HTML notation.|

```
mydata='&';
htmlvalue=GlideStringUtil.getHTMLValue(mydata);
gs.info(htmlvalue);
```

Output:

```
&amp;
```

## GlideStringUtil - getNumeric\(String sourceString\)

Extracts numeric characters from a string.

|Name|Type|Description|
|----|----|-----------|
|sourceString|String|Text to process.|

|Type|Description|
|----|-----------|
|String|Text containing only numeric characters.|

```
mystring='123 test 456 String 789 cleaning';
onlyNumeric=GlideStringUtil.getNumeric(mystring);
gs.info(onlyNumeric); 
```

Output:

```
123456789
```

## GlideStringUtil - isBase64\(String sourceString\)

Validates whether the specified string is a valid base64 string.

|Name|Type|Description|
|----|----|-----------|
|sourceString|String|Text to process.|

<table id="table_yzl_h3v_5cb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified string is in valid base64 format.Possible values:

-   true: Valid base64 formatted string.
-   false: Invalid base64 formatted string.

</td></tr></tbody>
</table>```
//(adding a "*" to corrupt the base64 format)
base64="GethdTYehdtshetB*";
isValid=GlideStringUtil.isBase64(base64);
gs.info(isValid);
```

Output:

```
false
```

## GlideStringUtil - isEligibleSysID\(String sourceString\)

Validates whether the specified string is in valid sys\_id format.

The sys\_id format is a sequence of 32 hexadecimal characters where all the characters are in the range \[0-9, a-f, A-F\].

|Name|Type|Description|
|----|----|-----------|
|sourceString|String|Text to process.|

<table id="table_dgh_2jv_5cb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified string is in valid sys\_id format.Possible values:

-   true: Valid sys\_id formatted string.
-   false: Invalid sys\_id formatted string.

</td></tr></tbody>
</table>```
sysID="62826bf03710200044e0bfc8bcbe5df1";
isElig=GlideStringUtil.isEligibleSysID(sysID);
gs.info(isElig);
```

Output:

```
true
```

## GlideStringUtil - newLinesToBreaks\(String sourceString\)

Replaces the new line character, `/n`, with a break code, `<br/>`.

|Name|Type|Description|
|----|----|-----------|
|sourceString|String|Text to process.|

|Type|Description|
|----|-----------|
|String|Text with new line characters replaced with HTML break code.|

```
mystring="new line break \n, this is after the break";
replaceNewLine=GlideStringUtil.newLinesToBreaks(mystring);
gs.info(replaceNewLine); 
```

Output:

```
new line break <br/>, this is after the break
```

## GlideStringUtil - normalizeWhitespace\(String sourceString\)

Replaces carriage returns, line feeds, and tabs with spaces, and then removes leading, trailing, and duplicate spaces.

|Name|Type|Description|
|----|----|-----------|
|sourceString|String|Text to process.|

|Type|Description|
|----|-----------|
|String|Text with carriage returns, line feeds, and tabs replaced with spaces, and then leading, trailing, and duplicate spaces removed.|

```
mystring="test with \n (new line) and \t (tabulation)";
normalizedString=GlideStringUtil.normalizeWhitespace(mystring);
gs.info(normalizedString);
```

Output:

```
test with (new line) and (tabulation)
```

## GlideStringUtil - unEscapeHTML\(String htmlString\)

Replaces escape characters with their respective character.

This method replaces these escape characters: `&lt; &gt: &nbsp; &amp; &quote;`.

**Note:** In scoped applications call this method as unescapeHTML\(String\). In global applications call this method as unEscapeHTML\(String\).

|Name|Type|Description|
|----|----|-----------|
|htmlString|String|String to process.|

|Type|Description|
|----|-----------|
|String|String with the escape characters replaced.|

This code example shows the method being called in a global application.

```
mydata='&quot;&lt;&gt;&amp;';
unescaped=GlideStringUtil.unEscapeHTML(mydata);
gs.info(unescaped);
```

Output:

```
"<>&
```

This code example shows the method being called in a scoped application.

```
mydata='&quot;&lt;&gt;&amp;';
unescaped=GlideStringUtil.unescapeHTML(mydata);
gs.info(unescaped);
```

Output:

```
"<>&
```

## GlideStringUtil - urlEncode\(String url\)

Encodes non-ASCII characters, unsafe ASCII characters, and spaces so you can use the returned string on the Internet. Uses UTF-8 encoding. Uses percent \(%\) encoding.

**Note:** Only available in global scope.

|Name|Type|Description|
|----|----|-----------|
|url|String|String to encode.|

|Type|Description|
|----|-----------|
|String|String with non-ASCII characters, unsafe ASCII characters, and spaces encoded.|

```
var mystring='Test characters: " < > & &quot; &lt; &gt; &amp;';
escapedString=GlideStringUtil.urlEncode(mystring);
gs.info(escapedString);
```

Output:

```
Test+characters%3A+%22+%3C+%3E+%26+%26quot%3B+%26lt%3B+%26gt%3B+%26amp%3B
```

