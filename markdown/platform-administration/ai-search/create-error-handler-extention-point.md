---
title: Create an error handler extension point
description: Create a scripted extension point to handle the embedding generation errors that occur when custom embedding models in the AI Search Retrieval Augmented Generation \(RAG\) application generate semantic vectors.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring bring your own model \(BYOM\), Configuring an external or custom embedding model, AI Search Retrieval Augmented Generation \(RAG\), Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an error handler extension point

Create a scripted extension point to handle the embedding generation errors that occur when custom embedding models in the AI Search Retrieval Augmented Generation \(RAG\) application generate semantic vectors.

## Before you begin

Role required: admin

## About this task

The `BYOMEmbeddingGenerationErrorHandler` script enables you to control the retry logic, handle batch failures, and modify passages when the embedding is generated. These strategies help to improve the performance of your large-scale semantic indexing pipelines.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** field, search and select the **BYOMEmbeddingGenerationErrorHandler** extension point.

3.  From the related links, select **Create implementation**.

4.  On the Script Include form, update the script as required.

    1.  To manage the embedding generation errors in a custom embedding model, define a `process(inputParams)` method in the extension point script. This method must return a structured response that is based on the predefined error categories.

        ```
        var BYOMEmbeddingGenerationErrorHandler = Class.create();
        BYOMEmbeddingGenerationErrorHandler.prototype = {
            initialize: function() {},
        
            process: function(inputParams) {
                var responseStatus = inputParams.responseStatus;
                var responseErrorCode = parseInt(inputParams.responseErrorCode);
                var responseBody = inputParams.responseBody;
                var responseHeaders = inputParams.responseHeaders;
                var responseErrorMessage = inputParams.responseErrorMessage;
                var passages = inputParams.passages;
                var maxTokens = inputParams.maxTokens;
                var additionalParams = {};
        
                var response = BYOMEmbeddingUtil.buildErrorResponse(
                    BYOMEmbeddingUtil.ErrorCodeEnum.UNKNOWN_ERROR,
                    "unknown error",
                    additionalParams
                );
        
        ```

    2.  To categorize errors, use the `BYOMEmbeddingUtil.ErrorCodeEnum` codes.

        ```
        
        BYOMEmbeddingUtil.ErrorCodeEnum = {
            REQUEST_SIZE_TOO_LARGE_ERROR: "RequestSizeTooLargeError",        // Reduce batch size and retry
            RATE_LIMIT_ERROR: "RateLimitError",                              // Retry without reducing batch size
            PASSAGE_SIZE_TOO_LARGE_ERROR: "PassageSizeTooLargeError",        // Retry with reduced passage size
            UNKNOWN_ERROR: "UnknowError",                                     // Ignore this run; retry in next job
            SKIP_BATCH_ERROR: "SkipBatchError",                              // Skip the entire batch, no retry
            UPDATE_PASSAGE_CONTENT_ERROR: "UpdatePassageContentError",       // Retry with updated passage content
            RETRY_SKIP_ON_FAIL_ERROR: "RetrySkipOnFailError"                 // Retry with backoff; skip on failure
        };
        
        ```

    3.  The allowed fields for `buildErrorResponse` include the following types of error codes:

        ```
        
        var allowedFieldsByErrorCode = {
            REQUEST_SIZE_TOO_LARGE_ERROR: ['error_code', 'error_message'],
            RATE_LIMIT_ERROR: ['error_code', 'error_message', 'retry_after_seconds'],
            PASSAGE_SIZE_TOO_LARGE_ERROR: ['error_code', 'error_message', 'passages'],
            UNKNOWN_ERROR: ['error_code', 'error_message'],
            SKIP_BATCH_ERROR: ['error_code', 'error_message'],
            UPDATE_PASSAGE_CONTENT_ERROR: ['error_code', 'error_message', 'passages'],
            RETRY_SKIP_ON_FAIL_ERROR: ['error_code', 'error_message']
        };
        
        ```

    4.  The following table describes the error codes and their corresponding retry strategies:

        |Error Code|Description|Retry Strategy|
        |----------|-----------|--------------|
        |REQUEST\_SIZE\_TOO\_LARGE\_ERROR|Batch too large|Reduces batch size, and retries exponentially.|
        |RATE\_LIMIT\_ERROR|Rate limit reached|Waits for `retry_after_seconds`, and then retries.|
        |PASSAGE\_SIZE\_TOO\_LARGE\_ERROR|Passage too large|Reduces the passage length \(usually half\), and then retries.|
        |UNKNOWN\_ERROR|Unknown issue|Skips a retry this run, and automatically retries in the next scheduled job.|
        |SKIP\_BATCH\_ERROR|Irrecoverable issue with batch|Skips the entire batch without a retry.|
        |UPDATE\_PASSAGE\_CONTENT\_ERROR|Retry with corrected content|Uses the corrected passages from a response and retries.|
        |RETRY\_SKIP\_ON\_FAIL\_ERROR|Retry then skip|Retries by increasing the wait times for a specified number of retry attempts.|

5.  Select **Update**.


**Parent Topic:**[Configuring bring your own model \(BYOM\)](../concept/creating-byom.md)

