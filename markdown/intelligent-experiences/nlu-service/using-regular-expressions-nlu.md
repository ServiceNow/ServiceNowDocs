---
title: Using regular expressions in entities
description: Learn how to use regular expressions in your NLU entities to establish patterns that help the system locate, match, and manage text.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [NLU entities, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Using regular expressions in entities

Learn how to use regular expressions in your NLU entities to establish patterns that help the system locate, match, and manage text.

Pattern entities use regular expressions \(regex\) to match any pattern of text, such as the format of an email address, a phone number, or an incident or case ID.

**Note:** ServiceNow uses and supports Java regex exclusively and not other vendor options, such as Perl regex.

## Regex examples

For a full example of regex code used in a pattern entity, see [Create a pattern entity](../task/create-pattern-entity.md).

The following four examples provide the format and regex code for different pattern entities.

-   **Knowledge base article**

    ServiceNow Knowledge Base \(KB\) articles use the format KB1234567. The regex code is KB\\d\{7\}, where KB = knowledge base record and d\{7\} = 7 digits.

    ![Create a pattern entity for a KB article.](../images/regex1.png)

-   **Case number**

    Case tasks use the format CS1234567. The regex code is CS\\d\{7\} where CS = case record and d\{7\} = 7 digits.

    ![Create a pattern entity for a case number.](../images/regex2.png)

-   **Email address**

    Email addresses use the format name@servicenow.com. The regex code is \\b\[a-zA-Z0-9&amp;\*/\_.+-\]+@\[a-zA-Z0-9-\]+\\.\[a-zA-Z0-9-.\]+\\b, which supports these formats: name@servicenow.com and name@servicenow.co.in.

    ![Create a pattern entity for email addresses.](../images/regex3.png)

-   **Phone number**

    United States phone numbers use the format 555-123-4567. The regex code is \\d\{10\}\|\(?:\\d\{3\}-\)\{2\}\\d\{4\}\|\\\(\\d\{3\}\\\)\\d\{3\}-?\\d\{4\}, which supports these formats: 5108882062,510-888-2062, and \(510\)888-2062.

    ![Create a pattern entity for a United States phone number.](../images/regex4.png)


## Regex resources

For further information on regular expressions, see the following external links.

-   [Java Regular Expressions](https://www.tutorialspoint.com/java/java_regular_expressions.htm)
-   [Java Regular Expression Tester](https://www.freeformatter.com/java-regex-tester.html#documentation)
-   [Pattern \(Java Platform SE7\)](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html)
-   [Java regex match abbreviations](https://blog.softhints.com/java-regex-extract-abbriviations/)

