---
title: Create error handler extension point
description: Create a scripted extension point to handle embedding generation errors that occur when custom embedding models generate semantic vectors. Using extension point enables you to create a primary ticket type as per the extension point definition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/ai-search/create-error-handler-extention-point.html
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring an external or custom embedding model, Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create error handler extension point

Create a scripted extension point to handle embedding generation errors that occur when custom embedding models generate semantic vectors. Using extension point enables you to create a primary ticket type as per the extension point definition.

## Before you begin

Role required: admin

## About this task

The `BYOMEmbeddingGenerationErrorHandler` script enables you to control retry logic, batch failure handling, and passage modification during embedding generation. These flexible strategies improve the robustness of large-scale semantic indexing pipelines.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** field, search and select the **BYOMEmbeddingGenerationErrorHandler** extension point.

3.  From Related Links, select **Create implementation**.

4.  On the Script Include form, update the script as required.

    1.  To handle the embedding generation errors by a custom embedding model, defines a process\(inputParams\) method in the extension point script. This method must return a structured response based on predefined error categories:

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

    2.  To categorize errors, use the following `BYOMEmbeddingUtil.ErrorCodeEnum` codes:

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

    3.  Allowed Fields for `buildErrorResponse` includes:

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

    4.  Retry Behavior by Error Code includes:

        |Error Code|Description|Retry Strategy|
        |----------|-----------|--------------|
        |REQUEST\_SIZE\_TOO\_LARGE\_ERROR|Batch too large|Reduces batch size, retries exponentially.|
        |RATE\_LIMIT\_ERROR|Rate limit reached|Waits for `retry_after_seconds`, then retries.|
        |PASSAGE\_SIZE\_TOO\_LARGE\_ERROR|Passage too large|Reduces passage length \(usually half\), then retries.|
        |UNKNOWN\_ERROR|Unknown issue|Skips retry this run, automatically retried in the next scheduled job.|
        |SKIP\_BATCH\_ERROR|Irrecoverable issue with batch|Skips entire batch without retry.|
        |UPDATE\_PASSAGE\_CONTENT\_ERROR|Retry with corrected content|Uses corrected passages from response and retries.|
        |RETRY\_SKIP\_ON\_FAIL\_ERROR|Retry then skip|Retries with exponential back off, marks as failed after max retries.|

5.  Select **Update**.


