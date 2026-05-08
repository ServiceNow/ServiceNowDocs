---
title: Message - Global
description: The Message Server API allows you to retrieve localized messages from the Message \[sys\_ui\_message\] table for an entry with code equal to the code parameter, key equal to the message parameter, and language equal to the language of the session \(or fallback language\).Retrieves a localized message from the Message \[sys\_ui\_message\] table while allowing for disambiguation and dynamic content insertion.Retrieves a localized message within the Message \[sys\_ui\_message\] in the specified language, regardless of the current user's session language.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Message- Global

The Message Server API allows you to retrieve localized messages from the Message \[sys\_ui\_message\] table for an entry with code equal to the code parameter, key equal to the message parameter, and language equal to the language of the session \(or fallback language\).

The Message API supports internationalization \(i18n\) by dynamically fetching messages based on the user's session language or a specified language parameter. This API offers three main features:

-   Disambiguation: Uses a compound key of `code` and `message` to distinguish between identical strings used in different contexts \(for example, "open" as a verb vs. noun\).
-   Named parameters: Allows for dynamic interpolation of values into message templates using named placeholders.
-   Language control: `getMessageLang` lets you specify a target language, useful for scenarios like mail merges or multilingual notifications 2 3.

The Message API is provided with the standard base system within the `sn_i18n` namespace and does not require any plugins or special roles to access it. Before calling any methods within this class, ensure appropriate Message \[sys\_ui\_message\] records exist and are populated with matching `key`, `code`, and `language` fields.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Message - getMessage\(String code, String message, Map args\)

Retrieves a localized message from the Message \[sys\_ui\_message\] table while allowing for disambiguation and dynamic content insertion.

Values from the **args** parameter are interpolated into the matching template literals in the string.

<table id="table_ikk_fn1_ggc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

code

</td><td>

String

</td><td>

Required. A string up to 255 characters used as an identifier. **code** can be used to disambiguate messages with similar text but different meanings or contexts. The recommended value is the name of the application scope. If further disambiguation is required, it may be augmented. For example, "open" could mean a status or an action, therefore the **code** parameter helps clarify which meaning to use. If two messages are required with the same string but different casing, the script is as follows:

```
sn_i18n.Message.getMessage("scopeName-open-capitalized", "Open");
sn_i18n.Message.getMessage("scopeName-open", "open");
```

</td></tr><tr><td>

message

</td><td>

String

</td><td>

Required. The message in English. Corresponds to the `key` ﬁeld in the Message \[sys\_ui\_message\] table. This message is used if no localized version is found for the target language.

</td></tr><tr><td>

args

</td><td>

JSON

</td><td>

Optional. A map of named parameters used to dynamically insert values into the message. The keys match the Named Parameters in the message. The values can be string literals or variables/constants that are in scope. For example, if your message is `"Hello, {name}!"`, you can pass `{name: "John"}` to render `"Hello, John!”`.

</td></tr></tbody>
</table><table id="table_jkk_fn1_ggc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Returns a value from the Message \[sys\_ui\_message\] table where:

-   The code parameter matches the code ﬁeld.
-   The first 255 characters of the message parameter match the key field.
-   The session language matches the language field.

 If no match is found, any fallback languages are checked for a match \(see Set a fallback language\). If a match is still not found, the message value \(2nd parameter\) is returned.

 Named Parameters are replaced with the specified values in the map passed in the args parameter.

</td></tr></tbody>
</table>The following example calls the getMessage\(\) method to retrieve an existing record in the Message \[sys\_ui\_message\] table in French, which is the user session language. The following code block contains the message's contents.

```
<?xml version="1.0" encoding="UTF-8"?>
<xml>
	<sys_ui_message>
		<code>exampleCode</code>
		<key>User {username} has been added as {role}</key>
		<language>fr</language>
		<message>L'utilisateur {username} a été ajouté en tant que {role}</message>
	</sys_ui_message>
</xml>
```

The example runs the API script with a session language of French:

```
//defines a user object using the name and role properties
var user = {
name: "Fred Luddy",
role: "maint"
}

//retrieves a localized message where code: "exampleCode" is the disambiguation key, message: User {username} has been added as {role}" is the default message template, and args: username: user.name, role: user.role } is a map of named parameters that will replace {username} and {role} in the message.
gs.info(sn_i18n.Message.getMessage("exampleCode","User {username} has been added as {role}",{username: user.name, role: user.role}));
```

The output contains the message in French:

```
//English: User Fred Luddy has been added as maint
L'utilisateur Fred Luddy a été ajouté en tant que maint
```

### Basic usage without named parameters

```
// Retrieves a localized message using only code and default message
var message = sn_i18n.Message.getMessage("status.open", "Open");
gs.info(message); // Output depends on user's session language
```

This example augments the **code** parameter with `"satus.open"` to disambiguate the message, and the **message** parameter, **"Open"**, as the fallback if no translation is found.

### Basic usage with named parameters

```
// Retrieves a localized message with named parameters
var message = sn_i18n.Message.getMessage(
 "scopeName” + "_greeting_personal",
 "Hello, {name}! You have {count} new messages.",
 { name: "John", count: 5 }
);
gs.info(message);
```

Output:

```
"Hello, John! You have 5 new messages." (localized if available)
```

This example augments the **code** parameter with `"greeting_personal"` to distinguish this greeting from others, and **message** is a template with placeholders. **args** \(`{name: "John", count: 5}`\) fills in the placeholders.

## Message - getMessageLang\(String code, String message, Map args, String language\)

Retrieves a localized message within the Message \[sys\_ui\_message\] in the specified language, regardless of the current user's session language.

Values from the **args** parameter are interpolated into the matching template literals in the string.

getMessageLang\(\) is useful for:

-   Overriding session language: Useful for sending notifications, emails, or reports in a specific language.
-   Multilingual support: Ideal for applications that serve users across different regions.
-   Testing translations: Helps developers preview how messages appear in other languages without switching user settings.

<table id="table_ikk_fn1_ggc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

code

</td><td>

String

</td><td>

Required. A string up to 255 characters used as an identifier. **code** can be used to disambiguate messages with similar text but different meanings or contexts. The recommended value is the name of the application scope. If further disambiguation is required, it may be augmented. For example, "open" could mean a status or an action, therefore the **code** parameter helps clarify which meaning to use. If two messages are required with the same string but different casing, the script is as follows:

```
sn_i18n.Message.getMessage("scopeName-open-capitalized", "Open");
sn_i18n.Message.getMessage("scopeName-open", "open");
```

</td></tr><tr><td>

message

</td><td>

String

</td><td>

Required. The message in English. Corresponds to the `key` ﬁeld in the Message \[sys\_ui\_message\] table. This message is used if no localized version is found for the target language.

</td></tr><tr><td>

args

</td><td>

JSON

</td><td>

Optional. A map of named parameters used to dynamically insert values into the message. The keys match the Named Parameters in the message. The values can be string literals or variables/constants that are in scope. For example, if your message is `"Hello, {name}!"`, you can pass `{name: "John"}` to render `"Hello, John!”`.

</td></tr><tr><td>

language

</td><td>

String

</td><td>

Required. Language to return the message in.Format: [BCP-47 language code](https://appmakers.dev/bcp-47-language-codes-list/)

Default: Session language

</td></tr></tbody>
</table><table id="table_jkk_fn1_ggc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Returns a value from the Message \[sys\_ui\_message\] table where:

-   The code parameter matches the code ﬁeld.
-   The first 255 characters of the message parameter match the key field.
-   The session language matches the language field.

 If no match is found, any fallback languages are checked for a match \(see Set a fallback language\). If a match is still not found, the message value \(2nd parameter\) is returned.

 Named Parameters are replaced with the specified values in the map passed in the args parameter.

</td></tr></tbody>
</table>The following example calls the getMessageLang\(\) method to translate an existing record in the Message \[sys\_ui\_message\] table into Japanese. The following code block contains the message's contents.

```
<?xml version="1.0" encoding="UTF-8"?>
<xml>
	<sys_ui_message>
		<code>exampleCode</code>
		<key>User {username} has been added as {role}</key>
		<language>ja</language>
		<message> {username} が {role} として追加されました。</message>
	</sys_ui_message>
</xml>
```

The example runs the API script with a session language other than Japanese:

```
var user = {
    name: "Fred Luddy",
    role: "maint"
}
gs.info(sn_i18n.Message.getMessageLang("exampleCode","User {username} has been added as {role}",{username: user.name, role: user.role}, "ja"));
```

The output contains the message in Japanese:

```
Fred Luddy が maint として追加されました
```

The following examples use named parameters \(\{username\}, \{role\}\) for dynamic content, specifies a target language using ISO language codes \("fr", "ja", "es"\), and ensures fallback to the default message if no translation is found.

French notification:

```
var user = {
  name: "Fred Luddy",
  role: "maint"
};

var message = sn_i18n.Message.getMessageLang(
  "user.added",
  "User ${username} has been added as ${role}",
  { username: user.name, role: user.role },
  "fr" // French
);

gs.info(message); // Output: "L'utilisateur Fred Luddy a été ajouté en tant que maint" (if translation exists)
```

Japanese notification:

```
var user = {
  name: "Hanako Yamada",
  role: "admin"
};

var message = sn_i18n.Message.getMessageLang(
  "user.added",
  "User ${username} has been added as ${role}",
  { username: user.name, role: user.role },
  "ja" // Japanese
);

gs.info(message); // Output: "ユーザー Hanako Yamada が admin として追加されました" (if translation exists)
```

Spanish notification:

```
var user = {
  name: "Carlos Ruiz",
  role: "editor"
};

var message = sn_i18n.Message.getMessageLang(
  "user.added",
  "User ${username} has been added as ${role}",
  { username: user.name, role: user.role },
  "es" // Spanish
);

gs.info(message); // Output: "El usuario Carlos Ruiz ha sido añadido como editor" (if translation exists)
```

