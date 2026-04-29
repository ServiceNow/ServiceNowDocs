---
title: Exploring HTML sanitizer
description: Remove unwanted code and protect against security concerns such as cross-site scripting attacks by sanitizing HTML markup in HTML fields and translated HTML fields.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [HTML sanitizer]
---

# Exploring HTML sanitizer

Remove unwanted code and protect against security concerns such as cross-site scripting attacks by sanitizing HTML markup in HTML fields and translated HTML fields.

Use HTML sanitization to ensure HTML content within your instance doesn’t contain potentially harmful content. HTML sanitization works by removing HTML tags that could be used to compromise your instance, such as `<script>`, `<link>`, or `<embed>` tags that can be used to run unwanted scripts on your instance or direct your users to unwanted content. Safe tags that control the formatting of your content are preserved. As an administrator, you're able to customize what content is removed or preserved. You’re also able to control whether sanitization applies to all content, or just fields you specify.

The HTML sanitizer works by checking the built-in inclusion list for markup that you always want to preserve. The sanitizer provides the HTMLSanitizerConfig script include that administrators can use to modify the built-in inclusion list. Items can also be added to the exclusion list to remove HTML markup. Contents of the exclusion list override the inclusion list.

The following types of items can be added to the inclusion and exclusion lists:

-   Global attributes
-   Any HTML elements

**Note:** By default, URL attributes like `href` and `src` support only these protocols:

-   `http`
-   `https`
-   `mailto`
-   `data`

For example:

```
<a href="https://community.servicenow.com/community">ServiceNow Community</a>
```

**Note:** To learn more about the **glide.html.sanitize\_all\_fields** property that controls use of the HTML sanitizer, see [Enable HTML Sanitizer \[Updated in Security Center 1.3\]](../../security-center/reference/sc-html-sanitizer.md) in Instance Security Hardening Settings.

## Configure urlAttributes and the protocols

You can configure urlAttributes and their protocols in the **HTMLSanitizer** script include. For example:

```
HTML_WHITELIST : {
urlAttributes: { "protocols" : [ "file", "notes" ] },
                -  -
                -  -
        }
```

Because `notes` is in the inclusion list in this example, this URL isn’t sanitized:

```
<a title=“Lotus” href=“Notes://ABC/X575C90019DE33/ABC594DCB76D86EB4925653E0011C4C1/ZZ90B7E2D33964749257EEA003456FD”>Lotus</a></p> 
```

## Default Inclusion List

**Note:** The Default Inclusion List is a system list and is not accessible by users in the Instance.

```
BUILTIN_HTML_WHITELIST :{
 
    globalAttributes:{ attribute:["id","class","lang","title","style"],
 
                                 attributeValuePattern:{}},
 
    label:{ attribute:["for"]},
 
    font:{ attribute:["color","face","size"]},
 
    a:{ attribute:["href","nohref","name","shape"]},
 
    img:{ attribute:["src","name","alt","border","hspace","vspace","align","height","width"},
 
    table:{ attribute:["border","cellpadding","cellspacing","bgcolor","background","align","no resize","height","width","summary","frame","rules"]},
 
    th:{ attribute:["background","bgcolor","abbr","axis","headers","scope","nowrap","height","width","align","valign","char off","char","colspan","rowspan"]},
 
    td:{ attribute:["background","bgcolor","abbr","axis","headers","scope","nowrap","height","width","align","valign","char off","char","colspan","rowspan"]},
 
    tr:{ attribute:["background","height","width","align","valign","char off","char"]},
 
    thead:{attribute:["align","valign","char off","char"]}, 
 
    tbody:{attribute:["align","valign","char off","char"]}, 
 
    tfoot:{attribute:["align","valign","char off","char"]}, 
 
    colgroup:{attribute:["align","valign","char off","char","span","width"]}, 
 
    col:{attribute:["align","valign","char off","char","span","width"]},
 
    p:{attribute:["align"]},
 
    style:{attributeValuePattern:{"type":"text/css"}}
 
    canvas:{ attribute:["height","width"]},
 
    details:{ attribute:["open"]},
 
    summary:{ attribute:["open","valign","char off","char"]},
 
    button:{ attribute:["disabled","accesskey","type"]},
 
    form:{},
 
    input:{ attribute:["size","maxlength","checked","alt","src","type","disabled","readonly","accesskey","border","usemap"]},
 
    select:{ attribute:["disabled","multiple","size"]},
 
    textarea:{ attribute:["rows","cols","disabled","readonly","accesskey"]},
 
    option:{ attribute:["disabled","label","selected"]},
 
    div:{ attribute:["align"]},
 
    ol:{ attribute:["start","type","square"]},
 
    ul:{ attribute:["type","square","itemscope","itemtype","itemref"]},
 
    li:{ attribute:["value","fb__id","itemprop"]},
 
    span:{ attribute:["color","size","data-mce-bogus","itemprop","face"]},
 
    br:{ attribute:["clear"]},
 
    h3:{ attribute:["itemprop"]},
 
    html:{ attribute:["xmlns","lang","xml:lang"]},
 
    link:{ attribute:["rel","type","href","charset"]},
 
    meta:{ attribute:["name","content","scheme","charset","http-equiv"]},
 
    pre:{ attribute:["xml:space"]},
 
    noscript:{},    h1:{},    h2:{},      h4:{},    h5:{},    h6:{},   
 
    i:{},    b:{},    u:{},    strong:{},    em:{},    small:{},    big:{},   
 
    pre:{},    code:{},    cite:{},    samp:{},    sub:{},    sup:{},    
 
    strike:{},   center:{},  blockquote:{},    hr:{},      map:{},
 
    dd:{},    dt:{},    dl:{},  fieldset:{},    legend:{}, figure:{},  tt:{},
 
    body:{},   caption:{},   head:{},   title:{},  shape:{},},
```

## Using variables and templates in HTML fields

HTML/Translated HTML fields undergo HTML sanitization by default. This process sanitizes the input HTML to protect it from cross-site scripting \(XSS\) and related security attacks. Storing templates or variables such as $\{description\} or \{\{description\}\} or similar and replacing them with a true description post sanitization will reduce the effectiveness of the sanitization process. This is due to the sanitization being called solely on the placeholder template and not the HTML content. Storing only HTML content in the HTML/Translated HTML fields helps ensure an effective sanitization process.

