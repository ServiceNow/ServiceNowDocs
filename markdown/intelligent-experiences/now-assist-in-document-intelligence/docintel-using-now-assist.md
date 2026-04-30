---
title: Using Now Assist in Document Intelligence
description: If you have an agent role, you can use the Now Assist in Document Intelligence workspace to analyze and extract information from your documents with generative AI.
locale: en-US
release: yokohama
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: concept
last_updated: "2025-04-24"
reading_time_minutes: 1
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Now Assist in Document Intelligence, Enable AI experiences]
---

# Using Now Assist in Document Intelligence

If you have an agent role, you can use the Now Assist in Document Intelligence workspace to analyze and extract information from your documents with generative AI.

The following diagram shows how the Now Assist in Document Intelligence skills are set up and used to process documents.

![Diagram showing the document processing flow in Now Assist in Document Intelligence.](../image/mmasset0020964-using-nadi-horizontal.png "Now Assist in Document Intelligence document processing workflow")

In this workflow:

-   A workflow integration creates a document task as part of its flow.
-   A document is uploaded for processing in a document task.
-   Now Assist processes the document and makes predictions based on the fields defined in the use case.
-   If the use case is not set to full automation, the task is sent to a live agent for review.
-   The agent provides input to validate or correct the values predicted by Now Assist.
-   The task is completed and the integrated workflow proceeds as defined.

-   **[Extract document data with Now Assist in Document Intelligence](../task/extract-document-data-with-now-assist-document-intelligence.md)**  
Use the Document Intelligence workspace to review the information that was extracted from a document by Now Assist in Document Intelligence. You can also flag fields for follow-up and identify missing information in the document.
-   **[Review document Q&amp;As with Now Assist in Document Intelligence](../task/review-document-qnas-with-now-assist-document-intelligence.md)**  
Use the Document Intelligence workspace to review the question and answer \(Q&amp;A\) predictions provided by Now Assist in Document Intelligence.

**Parent Topic:**[Now Assist in Document Intelligence](docintel-nowassist-landing.md)

