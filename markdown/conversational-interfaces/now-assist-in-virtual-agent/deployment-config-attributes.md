---
title: Now Assist deployment configuration properties
description: Manage the behavior of suggestions that users see when typing in the input box.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/now-assist-in-virtual-agent/deployment-config-attributes.html
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: reference
last_updated: "2026-06-03"
reading_time_minutes: 1
breadcrumb: [Now Assist in Virtual Agent reference, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Now Assist deployment configuration properties

Manage the behavior of suggestions that users see when typing in the input box.

|Property|Description|Deployment configuration|Domain|
|--------|-----------|------------------------|------|
|contextual\_suggestions\_enabled|Now Assist panel users see page contextual suggestions in the autosuggest zero query when this property is set to `true`. Prerequisite: autosuggest zero query should be enabled using **homepage\_zero\_query\_ autosuggestions\_enabled**.|Now Assist panel – Platform \(default\)|global|
|contextual\_suggestions\_enabled|Now Assist panel users see page contextual suggestions in the autosuggest zero query when this property is set to `true`. Prerequisite: autosuggest zero query should be enabled using **homepage\_zero\_query\_ autosuggestions\_enabled**.|UI Builder Now Assist|global|
|contextual\_suggestions\_enabled|Now Assist panel users see page contextual suggestions in the autosuggest zero query when this property is set to `true`. Prerequisite: autosuggest zero query should be enabled using **homepage\_zero\_query\_ autosuggestions\_enabled**.|AIA assistant|global|
|homepage\_typeahead\_autosuggestions\_enabled|Users see autosuggestions when they type the first character, onwards, in the input box. The default value is `true`. When the value is set to `false`, users don’t see autosuggestions.|DC test assistant|global|
|homepage\_ typeahead\_ autosuggestions\_enabled|Users see autosuggestions when they type the first character, onwards, in the input box. The default value is `true`. When the value is set to `false`, users don’t see autosuggestions.|Now Assist in Virtual Agent \(default\)|global|
|homepage\_ typeahead\_ autosuggestions\_enabled|Users see autosuggestions when they type the first character, onwards, in the input box. The default value is `true`. When the value is set to `false`, users don’t see autosuggestions.|Now Assist panel – Platform \(default\)|global|
|homepage\_zero\_query\_ autosuggestions\_enabled|Homepage zero query autosuggestions are shown to users. The default value is `true`. When the value is set to `false`, homepage zero query autosuggestions are not shown to users.|Now Assist in Virtual Agent \(default\)|global|
|homepage\_ zero\_query\_ autosuggestions\_enabled|Homepage zero query autosuggestions are shown to users. The default value is `true`. When the value is set to `false`, homepage zero query autosuggestions are not shown to users.|Now Assist panel – Platform \(default\)|global|
|homepage\_zero\_query\_autosuggestions\_enabled|Homepage zero query autosuggestions are shown to users. The default value is `true`. When the value is set to `false`, homepage zero query autosuggestions are not shown to users.|DC test assistant|global|

