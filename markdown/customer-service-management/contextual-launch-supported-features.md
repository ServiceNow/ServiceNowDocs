---
title: Feature context parameters supported in Engagement Messenger
description: Features for contextual launch capability enable you to set the default launch screen in Engagement Messenger.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Customer Service Management reference, Customer Service Management]
---

# Feature context parameters supported in Engagement Messenger

Features for contextual launch capability enable you to set the default launch screen in Engagement Messenger.

<table id="table_mxg_gyz_m4b"><thead><tr><th>

Feature

</th><th>

Embed code

</th><th>

Feature parameter description

</th></tr></thead><tbody><tr><td>

CHAT

</td><td>

```
{ 
	feature: "CHAT", 
	params: { 
		"topic_id": "*&lt;sys\_id&gt;*",
		"language": "*&lt;language\_name&gt;*",
		”sysparm_*&lt;param\_name&gt;*": "*&lt;param\_value&gt;*" 
	} 
}

```

</td><td>

-   **&lt;sys\_id&gt;**

Identifies the Virtual Agent topic to be included in the chat.

-   **&lt;language\_name&gt;**

Default chat language. For example, for French, specify `fr`

-   **&lt;param\_name&gt;:&lt;param\_value&gt;**

Any additional parameters to be passed to the Virtual Agent topic. The name of the parameter should start with `sysparm`. For example, `sys_param_product_name`.


</td></tr><tr><td>

WORK\_ORDER

</td><td>

```
{ 
	feature: "WORK_ORDER", 
	params: { 
		"table": "wm_order",
		"sys_id": "*&lt;sys\_id&gt;*"
		}
}

```

</td><td>

-   **&lt;sys\_id&gt;**

System identifier \(sys\_id\) of a work order.


</td></tr><tr><td>

CASE

</td><td>

```
{ 
	feature: "CASE", 
	params: { 
		"table": "sn_customerservice_case",
		"sys_id": "*&lt;sys\_id&gt;*"
		
	} 
}
```

</td><td>

-   **&lt;sys\_id&gt;**

System identifier \(sys\_id\) of a case.


</td></tr><tr><td>

NEW\_CASE

</td><td>

```
{ 
	feature: "NEW_CASE", 
	params: { 
		} 
}
```

</td><td>

None

</td></tr><tr><td>

CASE\_LIST

</td><td>

```
{ 
	feature: "CASE_LIST", 
	params: { 
		} 
}
```

</td><td>

None

</td></tr><tr><td>

VIEW\_ARTICLE

</td><td>

```
{ 
	feature: "VIEW_ARTICLE", 
	params: { 
		"sys_kb_id": "*&lt;sys\_id&gt;*"
	} 
}
```

</td><td>

-   **&lt;sys\_id&gt;**

System identifier \(sys\_id\) of a knowledge article.


</td></tr><tr><td>

SEARCH

</td><td>

```
{ 
	feature: "SEARCH", 
	params: { 
		"q": "*&lt;search\_term&gt;*"
	} 
}
```

</td><td>

-   **&lt;search\_term&gt;**

Term to be searched for in a search results query.


</td></tr><tr><td>

CASE\_SEARCH

</td><td>

```
{ 
	feature: "CASE_SEARCH", 
	params: { 
		"q": "*&lt;search\_term&gt;*"
	} 
}
```

</td><td>

-   **&lt;search\_term&gt;**

Term to be searched for in a case results query.


</td></tr><tr><td>

CATALOG\_ITEM

</td><td>

```
{ 
	feature: "CATALOG_ITEM", 
	params: { 
		"sys_id": "*&lt;sys\_id&gt;*"
	} 
}

```

</td><td>

-   **&lt;sys\_id&gt;**

System identifier \(sys\_id\) of a catalog item.


</td></tr><tr><td>

NEW\_APPOINTMENT

</td><td>

```
{ 
	feature: "NEW_APPOINTMENT", 
	params: { 
		} 
}
```

</td><td>

None

</td></tr><tr><td>

NEW\_WORK\_ORDER

</td><td>

```
{ 
	feature: "NEW_WORK_ORDER", 
	params: { 
		} 
}
```

</td><td>

None

</td></tr><tr><td>

HOME

</td><td>

```
{ 
	feature: "HOME", 
	params: { 
	} 
}
```

</td><td>

None

</td></tr></tbody>
</table>**Related topics**  


[Launch a feature in Engagement Messenger using custom code](../task/contextual-launch-using-script-engagement-messenger.md)

