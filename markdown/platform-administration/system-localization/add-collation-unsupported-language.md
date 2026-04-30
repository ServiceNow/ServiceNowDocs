---
title: Add collation information for an unsupported language
description: Add collation information for an unsupported language to enable sorting columns in lists according to the language.
locale: en-US
release: zurich
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Translating to an unsupported language, System Localization, Translation and localization, Configure core features, Administer]
---

# Add collation information for an unsupported language

Add collation information for an unsupported language to enable sorting columns in lists according to the language.

## Before you begin

Add a record for a language not provided by an internationalization \(I18N\) plugin to associate new translations with and translate content into that language. For more information, see [Translating to an unsupported language](self-localize.md).

Role required: admin

## About this task

Collation information must come from the underlying Relational Database Management System \(RDBMS\) used by the instance: MariaDB, RaptorDB, or Oracle. To determine which RDBMS an instance uses, navigate to **All** &gt; **System Diagnostics** &gt; **Database** &gt; **Information**. Refer to the documentation provided by the RDBMS to determine if the database includes a collation for a given language and the name of the collation.

## Procedure

1.  In the navigation filter, enter `sys_db_collation_info.list`.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Language|The [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) code for the language.|
    |Collation Name|The name of the collation provided by the Relational Database Management System \(RDBMS\).|
    |Application|The application scope.|
    |Database|The Relational Database Management System \(RDBMS\) to which the collation applies: MariaDB, RaptorDB, or Oracle.|

4.  Select **Submit**.


## Result

When sorting columns according to the session language is enabled, users can sort columns according to the collation of the unsupported language. For more information, see [Sorting according to the session language](sorting-session-language.md#).

