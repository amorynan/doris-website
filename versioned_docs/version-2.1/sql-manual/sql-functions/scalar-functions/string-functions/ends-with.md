---
{
    "title": "ENDS_WITH",
    "language": "en"
}
---

<!-- 
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
-->

## Description

Returns true if the string ends with the specified suffix, otherwise returns false. Special cases:

- If either of the two parameters is NULL, returns NULL.

## Syntax

```sql
ENDS_WITH ( <str> , <suffix> )
```

## Parameters

| Parameter | Description |
|-----------|--------------|
| `str`     | Specifies the original string to be judged |
| `suffix`  | Specifies the ending string to be judged |

## Return value

true or false, type is `BOOLEAN`. Special cases:

- If either of the two parameters is NULL, returns NULL.

## Example

```sql
SELECT ENDS_WITH("Hello doris", "doris"),ENDS_WITH("Hello doris", "Hello")
```

```text
+-----------------------------------+-----------------------------------+
| ends_with('Hello doris', 'doris') | ends_with('Hello doris', 'Hello') |
+-----------------------------------+-----------------------------------+
|                                 1 |                                 0 |
+-----------------------------------+-----------------------------------+
```