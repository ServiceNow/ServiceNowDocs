---
title: Configuring resource path for your custom embedding model
description: The bring your own model \(BYOM\) configuration uses the shared alias from Generative AI Controller to connect the LLM with your custom embedding model. To avoid configuration issues, ensure the connection URL is set separately and any additional paths are correctly set in the resource path.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-11-10"
reading_time_minutes: 1
breadcrumb: [Configuring an external or custom embedding model, AI Search Retrieval Augmented Generation \(RAG\), Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Configuring resource path for your custom embedding model

The bring your own model \(BYOM\) configuration uses the shared alias from Generative AI Controller to connect the LLM with your custom embedding model. To avoid configuration issues, ensure the connection URL is set separately and any additional paths are correctly set in the resource path.

Review the guidelines for configuring the resource path for custom embedding models in a BYOM setup.

## Configuration syntax

The `resource_path` should include any additional URL paths beyond the base URL specified in the Connection URL. The general syntax is:

```
/<API Version>/<specific-path-to-resource>
```

-   **Base URL vs Resource Path**
    -   The Connection URL in the alias contains only the base URL. For example, https://example.com.

        **Note:** Do not add any additional path, such as \(`/api/v1/model`\) in the connection URL, as it may break the LLM configuration.

    -   Specify any additional paths in the resource\_path value.

## Example Configuration

For a Google Gemini model, the configuration consists:

-   Connection URL:

    ```
    https://us-central1-aiplatform.googleapis.com
    ```

-   resource\_path:

    ```
    /v1/projects/sn-63151000.63151000-byom-poc-x6jx/locations/us-central1/publishers/google/models/gemini-embedding-001:predict
    ```


Parameters and Variables of resource path includes:

-   **API Version**

    Specify the version of the API you are using, for example, `/v1`\).

-   **Specific Path to Resource**

    Include the detailed path to the specific resource or model endpoint.


