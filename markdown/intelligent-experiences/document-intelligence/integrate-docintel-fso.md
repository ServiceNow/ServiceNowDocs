---
title: Integrate with Financial Services Operations
description: Document Intelligence provides document extraction capabilities to Financial Services Operations \(FSO\).
locale: en-US
release: australia
product: Document Intelligence
classification: document-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate, Document Intelligence, Enable AI experiences]
---

# Integrate with Financial Services Operations

Document Intelligence provides document extraction capabilities to Financial Services Operations \(FSO\).

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](docintel-nowassist-landing.md).

Document Intelligence integration with FSO enables machine learning \(ML\) to assist in quickly automating document processing and accurately extracting information from documents. Admins can further integrate Document Intelligence with the FSO Document Processor to enable users to extract and store fields from a document.

For more information, see Document Intelligence for FSO.

## How Document Intelligence works with FSO

Document Intelligence works within the Document Processor as follows:

-   Creating a Document Type \(sn\_doc\_processor\_type\) creates a record on DocIntel Use Case \(sys\_di\_task\_definition\)
-   Creating a Document Attribute \(sn\_doc\_processor\_attribute\) creates a DocIntel field \(sys\_di\_key\) record
-   Updating the Document Attribute record updates the field record

Creating a Document Verification Task \(sn\_doc\_processor\_verification\_task\) creates a DocIntel Document Task \(sys\_di\_task\) if it meets the following requirements:

-   Document Verification task has "ocr\_processing\_needed" checked
-   Document Verification task has a document attached
-   Document Verification task is in state "Submitted"

After the DocIntel document task is complete, the values should be extracted to the Extracted Fields \(sn\_doc\_processor\_extracted\_value\) table.

## Enable Document Intelligence for FSO

Ensure all the necessary applications and plugins are installed and activated to enable Document Intelligence in the FSO Document Processor.

See Enable Document Intelligence for FSO.

**Parent Topic:**[Integrating Document Intelligence with other applications](integrating-docintel.md)

