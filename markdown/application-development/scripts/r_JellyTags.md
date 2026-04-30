---
title: Jelly tags
description: Use Jelly to turn XML into HTML.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Creating custom UI Pages and UI macros, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Jelly tags

Use Jelly to turn XML into HTML.

Watch these introductory videos to learn about using Jelly in the ServiceNow AI Platform.

-   [Introducing Jelly Scripting - Part 1 \(Video\)](https://www.youtube.com/watch?v=_MhWugMQegs&list=PLCOmiTb5WX3ouggdJ4ty2dVUSrki9uYr1&index=1%7C)
-   [Introducing Jelly Scripting - Part 2 \(Video\)](https://www.youtube.com/watch?v=Td7t_tiehzY&list=PLCOmiTb5WX3ouggdJ4ty2dVUSrki9uYr1&index=2%7C)
-   [Introducing Jelly Scripting - Part 3 \(Video\)](https://www.youtube.com/watch?v=gPy5xkks0tA&list=PLCOmiTb5WX3ouggdJ4ty2dVUSrki9uYr1&index=3%7C)

## Jelly Tags

-   **if**
    -   Description: The `if` tag is just what it looks like, an `if` tag. This is like an `if` statement in any programming language, but keep in mind that there is no `elseif` tag and no `else` tag. If you want to create that kind of structure, try the `choose`/`when`/`otherwise` syntax.
    -   Parameters: `test` - The condition to evaluate in order to determine if the block will execute.
    -   Example:

        ```
        <g:evaluate var="jvar_now_GR" object="true">
           var now_GR = new GlideRecord("incident");
           now_GR.addQuery("active", true);
           now_GR.query();
           now_GR;
        </g:evaluate>
         
        <j:if test="${!jvar_now_GR.hasNext()}">
           We did not find any active incidents.
        </j:if>
        <j:if test="${jvar_now_GR.next()}">
           We found ${jvar_now_GR.getRowCount()} active incidents.
        </j:if>
        
        ```

-   **while**
    -   Description: The `while` tag does a while loop.
    -   Parameters: `test` - The condition to evaluate in order to determine if the statement will loop through. This should be an expression enclosed in `${}` or `$[]`that evaluates to true or false.
    -   Example:

        ```
        <g:evaluate var="jvar_now_GR" object="true">
           var now_GR = new GlideRecord("incident");
           now_GR.addQuery("active", true);
           now_GR.query();
           now_GR;
        </g:evaluate>
         
        <j:while test="${jvar_now_GR.next()}">
          <a href="incident.do?sys_id=${jvar_now_GR.getValue('sys_id')}">${jvar_now_GR.getValue('number')}</a>
        </j:while>
        ```

-   **set**
    -   Description: The `set` tag sets a variable.
    -   Parameters:
        -   `var` - The variable to set. Often the system prefixes these variables with `jvar_` for consistency.
        -   `value` - The value to set `var` to. This is often an expression enclosed in `${}` or `$[]`.
        -   `defaultValue` - If the value results to null or empty, this value is put into the `var`.
    -   Example:

        ```
        <j:set var="jvar_incident_number" value="${jvar_now_GR.getValue('number')}"/>
        ```

-   **set\_if**
    -   Description: The `set_if` tag sets a variable based on a test. This tag is similar to the `ternary` operator in other programming languages \(`var = <test> ? <if_true> : <if_false>`\).
    -   Parameters:
        -   `var` - The variable to set. Often the system prefixes these variables with `jvar_` for consistency.
        -   `test` - The condition to evaluate in order to determine if the statement will evaluate the true value or the false value. This should be an expression enclosed in `${}` or `$[]` that evaluates to true or false.
        -   `true` - The value to set the variable to if `test` evaluates to `true`. This parameter is optional, so if the field is blank, and if test evaluates to true, the variable is left blank.
        -   `false` - The value to set the variable to if `test` evaluates to false. This parameter is optional, so if the field is blank, and if test evaluates to false, the variable will be left blank.
-   **choose**
    -   Description: The `choose` tag starts a choose block of code. This is similar to the `if-elseif-else` kind of syntax in most programming languages. With a `choose` tag, you can use `when` and `otherwise` tags to specify other blocks of code.
    -   Parameters: None
    -   Example:

        ```
        <j:choose>
           <j:when test="${jvar_now_GR.getRowCount() ${AMP}lt; 1}">We found multiple records!</j:when>
           <j:when test="${jvar_now_GR.next()}">We found record ${jvar_now_GR.getValue('number')}</j:when>
           <j:otherwise>Sorry, we could not find the record you specified.</j:otherwise>
        </j:choose>
        ```

-   **when**
    -   Description: The `when` tag is used within a choose block to indicate a condition. This tag is similar to an `if` or an `elseif` in that it specifies a condition, executes the inner content, and then implies a break at the end to leave the `if-elseif` construct.
    -   Parameters: `test` - The condition to evaluate in order to determine if the statement will loop through. This should be an expression enclosed in `${}` or `$[]` that evaluates to true or false.
    -   Example:

        ```
        <j:choose>
           <j:when test="${jvar_now_GR.getRowCount() ${AMP}lt; 1}">We found multiple records!</j:when>
           <j:when test="${jvar_now_GR.next()}">We found record ${jvar_now_GR.getValue('number')}</j:when>
           <j:otherwise>Sorry, we could not find the record you specified.</j:otherwise>
        </j:choose>
        ```

-   **otherwise**
    -   Description: The `otherwise` tag is used within a `choose`/`when`/`otherwise` block, and is like the `else` or `default` case.
    -   Parameters: None
    -   Example:

        ```
        <j:choose>
           <j:when test="${jvar_now_GR.getRowCount() ${AMP}lt; 1}">We found multiple records!</j:when>
           <j:when test="${jvar_now_GR.next()}">We found record ${jvar_now_GR.getValue('number')}</j:when>
           <j:otherwise>Sorry, we could not find the record you specified.</j:otherwise>
        </j:choose>
        ```


## Glide Tags

-   **evaluate**
    -   Description: The `evaluate` tag evaluates JavaScript code \(server side\), and makes variables visible to future code. Unlike other tags, the `evaluate` tag evaluates the content that is inside the tag as server side JavaScript.

        The context is the same as that of script includes in the system. Other script includes, global business rules, GlideRecord, GlideSystem, and Jelly variables \(prefixed with jelly. if the parameter `jelly="true"` is set\) are available.

    -   Parameters:
        -   `var` - The name of the variable that will be set to the result of the script.
        -   `object` - If set to `true`, the result of the expression is treated as an object instead of a primitive variable \(string or integer variable values\).
        -   `jelly` - If set to `true`, allows Jelly context variables to be referenced in the script.
        -   `expression` - This is an expression to be executed for the value to put in `var`. The expression can be either of two places. First, it can be an attribute on the `evaluate` tag itself. Otherwise, the content between the beginning tag and ending tag is the expression. The last line of the expression is the actual value passed into `var`.
    -   Example:

        ```
        <g:evaluate var="jvar_now_GR" object="true">
          var now_GR = new GlideRecord("incident");
          now_GR.addQuery("active", "true");
          now_GR.query();
          now_GR; // this is the variable put into the variable jvar_now_GR
        </g:evaluate>
        ```

        ```
        <g:evaluate var="jvar_now_GR" object="true" expression="
          var now_GR = new GlideRecord('incident');
          now_GR.addQuery('active', 'true');
          now_GR.query();
          now_GR; // this is the variable put into the variable jvar_now_GR" />
        ```

-   **messages**
    -   Description: The `messages` tag helps with translation. When gs.getMessage\(\) is called anywhere on a page, there are two possible places where the translation is found. First, the page checks a local cache of translations. Second, the page makes an AJAX call to the server to find the translation. What `g:messages` does is allow pages to cache certain messages.
    -   Parameters: None
    -   Example:

        ```
        <g:messages>
          Yes
          No
          Cancel
        </g:messages>
        ```

-   **breakpoint**
    -   Description: When the `breakpoint` tag is called, it prints a list of all the variables in Jelly at the current moment, with their respective values. If a variable is specified, it prints the requested variable and its value. The output is placed in the system log.
    -   Parameters: `var` - \(Optional\) The variable to log the value for. If `var` is not specified, then all variables are dumped into the log.
    -   Example:

        ```
        <g:breakpoint />
        ```

        ```
        <g:breakpoint var="sysparm_view"/>
        ```

-   **no\_escape**
    -   Description: The system, by default, uses escaped output as a security measure. Output placed inside of `no_escape` tags is not escaped before output. Be careful when using these tags, because if user input is displayed here it can open a security vulnerability on the page.
    -   Parameters: None
    -   Example \(phase 1\) – Disables automatic output escaping of all contained $\{\} expressions:

        ```
        <g:no_escape>
         ${jvar_raw_html_data}
        </g:no_escape>
        ```

    -   Example \(phase 2\) – Use `NOESC` to disable escaping for the specified string. This implies the expression must evaluate to a string.

        ```
        <g:no_escape>$[NOESC:jvar_expr]</g:no_escape>
        ```

        For information on phase 1 and phase 2 evaluation, refer to the Jelly introduction videos listed at the beginning of this section.

-   **macro\_invoke**
    -   Description: The `macro_invoke` tag calls a UI macro that you have specified in the database. You may also call a UI macro by specifying it in the tag name. For example, if you had a UI macro named my\_macro, you could call that macro with the tag `<g:my_macro/>`. For information, see [UI macros](https://www.servicenow.com/docs/access?context=c_UIMacros&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).
    -   Parameters:
        -   `macro` - The name of the UI macro to execute. If your tag name is `g:macro_invoke`, then the macro attribute specifies the name of the macro. If the tag name includes the name of the macro, then there is no need to include a macro attribute.
        -   Other attributes - For each attribute you specify, a variable with that name will be available in the context of the UI macro, prefixed with `jvar_`.
    -   Example:

        ```
        <!-- Will invoke the contents of the UI macro named "sample_macro", which will have the variable jvar_message available within it-->
        <g:macro_invoke macro="sample_macro" message="This is a sample macro variable." />
        ```

        ```
        <!-- Will invoke the contents of the UI macro named "sample_macro", which will have the variable jvar_message available within it-->
        <g:sample_macro message="This is a sample macro variable." />
        ```

-   **if\_polaris**
    -   Description: The `if_polaris` tag checks if Next Experience is enabled for the current page. It must include at least one of the child tags `<g:then />` or `g:else />`.
    -   Parameters: None
    -   Example:

        ```
        <g:if_polaris>
            <g:then><g:inline template="polaris_nav"/></g:then>
            <g:else><g:inline template="classic_nav"/></g:else>
        </g:if_polaris>
        
        <g:if_polaris>
            <g:then><a href="…">Click here to see what’s new!</a></g:then>
        </g:if_polaris>
        
        <g:if_polaris>
            <g:else>Core UI only code here!</g:else>
        </g:if_polaris>
        
        ```

-   **then**
    -   Description: The `then` tag is used within an `if_polaris` block to set the page content when Next Experience is enabled.
    -   Parameters: None
    -   Example:

        ```
        <g:if_polaris>
            <g:then><g:inline template="polaris_nav"/></g:then>
            <g:else><g:inline template="classic_nav"/></g:else>
        </g:if_polaris>
        
        <g:if_polaris>
            <g:then><a href="…">Click here to see what’s new!</a></g:then>
        </g:if_polaris>
        
        <g:if_polaris>
            <g:else>Core UI only code here!</g:else>
        </g:if_polaris>
        
        ```

-   **else**
    -   Description: The `else` tag is used within an `if_polaris` block to set the page content when Next Experience isn't enabled.
    -   Parameters: None
    -   Example:

        ```
        <g:if_polaris>
            <g:then><g:inline template="polaris_nav"/></g:then>
            <g:else><g:inline template="classic_nav"/></g:else>
        </g:if_polaris>
        
        <g:if_polaris>
            <g:then><a href="…">Click here to see what’s new!</a></g:then>
        </g:if_polaris>
        
        <g:if_polaris>
            <g:else>Core UI only code here!</g:else>
        </g:if_polaris>
        
        ```


-   **[Jelly escaping types](../../server-scripting/reference/r_JellyEscapingTypes.md#)**  
You use different methods when escaping characters in JavaScript and HTML. JavaScript uses the backslash character, and HTML uses the ampersand character.
-   **[Extensions to Jelly syntax](../concept/c_ExtensionsToJellySyntax.md#)**  
Apache's Jelly syntax is used to render forms, lists, UI pages, and many other things rendered in ServiceNow.

**Parent Topic:**[Creating custom UI Pages and UI macros](../concept/create-custom-ui-pages.md)

