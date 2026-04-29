---
title: Multi-language translation
description: Implement multi-language translation for end-user interfaces. Enable languages and compile translation files.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Multi-language translation

Implement multi-language translation for end-user interfaces. Enable languages and compile translation files.

CPQ can be set up to display configuration experiences in a user's preferred language. This article describes how to implement translations in CPQ.

## Foundation and scope

CPQ multi-language capability is available on end-user user interfaces \(buyside\). The administration platform displays English only.

CPQ supports all left-to-right languages, including those with multi-byte character sets \(e.g., Japanese, Korean\).

**Note:** Right-to-left languages such as Arabic and Hebrew are not currently supported. If your implementation expects to require translation into a right-to-left language, please log a Support case and we will follow up with you.

The base language for all CPQ environments is English. As a result, translations of custom strings must be furnished with the corresponding English key. Example: If the administrator enables French and Finnish on an environment, they will need to provide English-to-French and English-to-Finnish translations.

When multi-language is enabled in CPQ, the app will attempt to serve a configuration experience according to the end-user's browser locale setting. If the language defined in the browser locale matches an enabled language in CPQ, the application will attempt to serve the strings in the requested language. However, if a string is not defined for the requested language, the application will display the corresponding English equivalent.

## Terms used in this article

Static strings: Text CPQ displays to the user that is defined by the application. Examples include default button labels, basic error messages, text in confirmation boxes, and hovertext for set controls. Static strings are currently provided in English \[en\], Finnish \[fi\], French \[fr\], German \[de\], Italian \[it\], and Spanish \[es\]. CPQ will translate static strings into additional languages as needed.

Custom strings: Field labels, field option labels, product name and description, layout tier headings, custom messages and similar strings defined by an administrator are "custom".

Base language: the foundational language in a CPQ environment. Choosing your base language is an important decision, as \(1.\) all configuration elements—including fields, field options, layout elements, and custom message text—must be defined in the base language; and \(2.\) all translations of custom strings key off of the base language. A CPQ environment can only have one base language. All environments in your dev stack need to have the same base language, to enable environment-to-environment migration.

Enabled languages: in addition to the base language, these are the languages you want to support for your end-users coming to CPQ.

## Implementation

1.  Log a Support case that describes the languages you intend to translate configuration experiences into. Request that CPQ Support enable these languages on all relevant CPQ environments in your development stack. After the new languages are enabled, continue with step 2.
2.  To understand how multi-language translation works in CPQ, we recommend that you try a small-scale proof-of-concept before embarking on a wholesale translation effort.

    -   Select a picklist field displayed on the end-user layout. Example: In Blueprint1, we will translate Paint Color \[paintColor\]. paintColor has label "Paint Color" and options "Blue", "Yellow", "Green".
    -   For the purposes of this experiment, assume we enabled Spanish \[es\] in step \#1. You can customize this experiment for one of the languages you enabled in step \#1. In a CSV file, define Spanish \[es\] translations for the field label and the picklist field options:![CSVfile](../images/cpq-spanish-translation-csv.png)
    The graphic above is a sample translation upload file. You can find another example on the Matrix Loader page.

    ![Matrix loader](../images/cpq-matrix-loader-translations.png)

3.  Save the CSV file and upload via Matrix Loader.

    **Note:** If using a program like Microsoft Excel, you must export in UTF-8 format to support characters with diacritic marks, such as accent, cedilla, circumflex, diaeresis/umlaut, etc.

4.  Deploy the blueprint.

To test the buyside user interface, we recommend using the Chrome browser with the [https://chromewebstore.google.com/detail/locale-switcher/kngfjpghaokedippaapkfihdlmmlafcc?hl=en-US](https://chromewebstore.google.com/detail/locale-switcher/kngfjpghaokedippaapkfihdlmmlafcc?hl=en-US) extension installed. This extension allows you to quickly switch the browser locale to test localization. Set Locale Switcher to Spanish \[es\] and open the Blueprint1 configuration. The paintColor field label and contents should be displayed using the custom translated strings in \#2.

The following graphic shows the English version of the picklist on the buyside UI:

![Paint color](../images/cpq-picklist-buyside-ui-english.png)

The following graphic shows the Spanish version of the picklist on the buyside UI:

![Select color](../images/cpq-picklist-buyside-ui-spanish.png)

The following experiment demonstrates how various custom strings, including those defined in field options and layouts, are translated, uploaded, and deployed to accomplish an English-to-Spanish translation.

1.  Compile a list of custom strings that require translation.
2.  Export the following CSV files from CPQ administration:
    -   Field Options: every field option label requires translation. In the Field Option CSV file, these are the strings defined in the name column
    -   Picklist extensions: for each picklist extension that has Extended Information defined, export the Extension Data CSV file. A translation should be provided for every string in columns B and greater.
    -   Product Pickers: strings defined in Determination-type Bulk Actions should be translated into the target language.
    -   Rules:
        -   When action\_type = message, action\_value requires translation
        -   When action\_type = determination and the action affects a text field, many use cases require translation of the string in action\_value
    -   Layout: Translations are needed for:
        -   Tier headings
        -   Columnset headings
        -   Field labels
        -   Help content
        -   Product list column headings
3.  Build your translation file. The file should be one of the following formats:
    -   CSV: [SampleTranslationUploadFormat\_en\_to\_es.csv](https://drive.google.com/file/d/14Gyu0JonI0b9XiE6X9YqkDZqnKfBVOK5/view?usp=sharing)
    -   XLIFF: [SampleTranslationUploadFormat\_en\_to\_fr.xlf](https://drive.google.com/file/d/1z1bfkhiS3mMuK38ywujTFSPha98CNuCq/view?usp=drive_link)
4.  For each string identified in step 1, add an entry to your translation file.
5.  Upload your file in the Matrix Loader.
6.  Deploy the corresponding blueprints.

## Downloading translated strings

To download the translated strings that are saved in a CPQ environment, open CPQ administration in a browser tab. In another browser tab, open the following URL:

`https://{{baseUrl}}/a/translations/v1/translations?fileType={{fileType}}&codes={{codes}`

where \{fileType\} is either `csv` or `xml`, and \{codes\} is a comma-delimited list of the translated strings to retrieve. Use 2-letter language codes such as. 'en' and 'fr'. For example, `&codes=en, fr,de`

**Note:** Some characters in the rendered translated string may include diacritic marks \(accents, etc.\), and if the wrong character set is used these will appear as a replacement symbol for unknown character \(square with a question mark\). To avoid this problem, export CSV files using the UTF-8 format.

