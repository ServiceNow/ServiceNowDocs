---
title: LSOFParser - Global
description: The LSOFParser script include provides methods to parse the output of the lsof command: lsof -i4TCP -n -P -F pcnfT.Generates the specified error message.Initializes the file descriptor process.Initializes the parser process.Sets the current command.Closes the file descriptor process.Closes the parser process.Sets the current file descriptor.Sets the current address.Sets the current PID.Sets the current state.Parses the specified lsof output.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# LSOFParser- Global

The LSOFParser script include provides methods to parse the output of the `lsof` command: `lsof -i4TCP -n -P -F pcnfT`.

Use this script include with a discovery script when you need to parse `lsof` output.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## LSOFParser - error\(String msg\)

Generates the specified error message.

|Name|Type|Description|
|----|----|-----------|
|msg|String|The error message|

|Type|Description|
|----|-----------|
|void| |

## LSOFParser - initFileDescriptor\(\)

Initializes the file descriptor process.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## LSOFParser - initProcess\(\)

Initializes the parser process.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## LSOFParser - on\_c\(String line\)

Sets the current command.

|Name|Type|Description|
|----|----|-----------|
|line|String|The command|

|Type|Description|
|----|-----------|
|void| |

## LSOFParser - on\_endFileDescriptor\(\)

Closes the file descriptor process.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## LSOFParser - on\_endProcess\(\)

Closes the parser process.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## LSOFParser - on\_f\(String line\)

Sets the current file descriptor.

|Name|Type|Description|
|----|----|-----------|
|line|String|The file descriptor|

|Type|Description|
|----|-----------|
|void| |

## LSOFParser - on\_n\(String line\)

Sets the current address.

|Name|Type|Description|
|----|----|-----------|
|line|String|The address|

|Type|Description|
|----|-----------|
|void| |

## LSOFParser - on\_p\(String line\)

Sets the current PID.

|Name|Type|Description|
|----|----|-----------|
|line|String|The PID|

|Type|Description|
|----|-----------|
|void| |

## LSOFParser - on\_T\(String line\)

Sets the current state.

|Name|Type|Description|
|----|----|-----------|
|line|String|The state|

|Type|Description|
|----|-----------|
|void| |

## LSOFParser - parse\(String lsofOutput\)

Parses the specified `lsof` output.

Results are available in connections and listeners arrays, and errors are recorded in errorString\(\) and isValid\(\).

|Name|Type|Description|
|----|----|-----------|
|lsofOutput|String|The `lsof` output|

|Type|Description|
|----|-----------|
|void| |

