---
{
    "title": "CLEAN TRASH",
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

This statement is used to clean up garbage data in the backend

grammar:

```sql
ADMIN CLEAN TRASH [ON ("BackendHost1:BackendHeartBeatPort1", "BackendHost2:BackendHeartBeatPort2", ...)];
```

illustrate:

1. Use BackendHost:BackendHeartBeatPort to indicate the backend that needs to be cleaned up, and clean up all backends without adding the on limit.

## Examples

1. Clean up the junk data of all be nodes.

        ADMIN CLEAN TRASH;

2. Clean up the junk data of '192.168.0.1:9050' and '192.168.0.2:9050'.

        ADMIN CLEAN TRASH ON ("192.168.0.1:9050","192.168.0.2:9050");

## Keywords