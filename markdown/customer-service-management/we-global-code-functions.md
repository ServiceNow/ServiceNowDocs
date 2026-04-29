---
title: Functions available in Web Embeddables global and component code
description: ServiceNow Embeddables API enables you to integrate ServiceNow components into your external websites. These functions provide essential functionality for initialization, authentication, component management, and event handling.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Web Embeddables reference, Reference, Customer Service Management]
---

# Functions available in Web Embeddables global and component code

ServiceNow Embeddables API enables you to integrate ServiceNow components into your external websites. These functions provide essential functionality for initialization, authentication, component management, and event handling.

## Global code

The embed script includes the following methods as part of the global code. The following details help you understand how they work.

-   **Init method**
    -   **Purpose**: Initializes the embeddables framework with configuration settings.
    -   **Usage pattern**:

        ```
        await init({
        	theme: 'fad87d2ca304121029a4d1aed31e610f', //sys_id of theme,
        	baseURL: 'https://demo.servicenow.com',
        	authCallback: getTokenCallBack, // Authentication callback function 
               locale: 'ja', // Language/locale for components
               interceptSessionTimeout: true, // Handle session timeouts (default: true)
        	// cacheComponents: [ //Pre-cache component for performance  "sn-embedx-case-form", "sn-embedx-case-list", "sn-embedx-case-view" ]
        });
        ```

    -   **Parameters**:
        -   `authCallback` \(Function\): Returns authentication token for the current user.
        -   `baseURL` \(String\): Base URL of the ServiceNow instance.
        -   `locale` \(String, optional\): Language/locale setting \(for example, ‘en’, ‘es’\) that updates the user’s language preference in ServiceNow for authenticated user.
        -   `theme` \(String\): The sys\_id of theme to apply.
        -   `interceptSessionTimeout` \(Boolean, optional\): Enable session timeout handling. By default, it is set to `true`.
        -   `cacheComponents` \(Array, optional\): List of component tag names to pre-cache.
    -   **Key behaviors**:
        -   Must be called before any other embeddables functions.
        -   Loads necessary resources and establishes a connection.
        -   Optionally sets up interceptors for session management.
        -   Updates the user’s language preference for the authenticated user if locale is provided.
        -   Pre-caches specified components for improved performance.
-   **login\(\)**
    -   **Purpose**: Authenticates the user with the ServiceNow instance.
    -   **Usage Pattern**:

        ```
        await login();
        
        ```

    -   **Key behaviors**:
        -   Calls the authCallback function provided during initialization.
        -   Authenticates with the returned token - Dispatches **SN\_EMBEDDABLES\_LOGIN\_SUCCESS** event on success.
    -   **Prerequisites:** `init()` must be called first with a valid authCallback - authCallback function must return a valid authentication token.
-   **logout\(\)**
    -   **Purpose**: Logs out the user from ServiceNow session.
    -   **Usage pattern**:

        ```
        await logout();
        ```

    -   **Key behaviors**: Dispatches **SN\_EMBEDDABLES\_LOGOUT\_SUCCESS** event on success.
    -   **Prerequisite**: `init()` must be called first with valid baseURL - User must be logged in.

## Component code

The embed script includes the following methods as part of the component code. The following details help you understand how they work.

-   **getEmbeddables**
    -   **Purpose**: Loads and initializes specified embeddable components.
    -   **Usage pattern**:

        ```
        // Load components by providing array of component tag names
        getEmbeddables(["sn-embedx-case-view", "sn-embedx-case-form"]);
        ```

    -   **Parameters**: `components` \(Array\): Array of component tag names to load
-   **setProperties\(componentElement, properties\)**
    -   **Purpose**: Sets properties on embeddable component instances.
    -   **Usage pattern**:

        ```
        const caseViewComponent = document.querySelector('sn-embedx-case-view');
        setProperties(snEmbedxCaseView,{
        		table:sn_customerservice_case,
        		sysId:221a69cd3b411300b5c42479b3efc480,
        		playbookExperience:playbookExperience,
        		selectedPlaybookContextId:85d9f349ff766210e9d3ffffffffffce,
        		selectedStageContextId:9da56770ff7a2210e9d3ffffffffffd9,
        		selectedActivityContextId:5d8bf1805d8bf8205d8b54d05d8be070 });
        ```

    -   **Parameters**: `componentElm` \(HTMLElement\): The component DOM element - properties \(Object\): Key-value pairs of properties to set.
-   **setEvents \(componentElement, eventHandlers\)**
    -   **Purpose**: Attaches event listeners to embeddable components.
    -   **Usage pattern**:

        ```
        const caseViewComponent = document.querySelector('sn-embedx-case-view');
        const eventHandlers = {'
        'SN_EMBEDX_CASE_VIEW#COMPONENT_READY': (e) => { 
        console.log('Component is ready and usable'); }, 
        'SN_EMBEDX_CASE_VIEW#COMPONENT_ERROR': (e) => { const 
        { errorMessage, errorType } = e.detail.payload;
        console.log('Component error:', errorMessage, errorType); },
        };
        setEvents(caseViewComponent, eventHandlers); 
        ```

    -   **Parameters**: `componentElm` \(HTML Element\): The component DOM element - eventHandlers \(Object\): Key-value pairs where keys are event names and values are handler functions.

## Key considerations

Here are some key considerations to help you implement this effectively:

-   Ensure to call init\(\) first. It sets up the foundation for all other functions.
-   Use event handlers for the component life-cycle. It also monitor component readiness and errors.
-   Cache frequently used components. Use cacheComponents in init\(\) for better performance.
-   Implement

