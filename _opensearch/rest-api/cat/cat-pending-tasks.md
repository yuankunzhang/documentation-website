---
layout: default
title: cat pending tasks
parent: CAT
grand_parent: REST API reference
nav_order: 45
has_children: false
---

# cat pending tasks
Introduced 1.0
{: .label .label-purple }

The cat pending tasks operation lists the progress of all pending tasks, including task priority and time in queue.

## Example

```
GET _cat/pending_tasks?v
```

## Path and HTTP methods

```
GET _cat/pending_tasks
```

## URL parameters

All cat nodes URL parameters are optional.

In addition to the [common URL parameters]({{site.url}}{{site.baseurl}}/opensearch/rest-api/cat/index#common-url-parameters), you can specify the following parameters:

Parameter | Type | Description
:--- | :--- | :---
local | Boolean | Whether to return information from the local node only instead of from the master node. Default is false.
master_timeout | Time | The amount of time to wait for a connection to the master node. Default is 30 seconds.
time | Time | Specify the units for time. For example, `5d` or `7h`. For more information, see [Supported units]({{site.url}}{{site.baseurl}}/opensearch/units/).


## Response

```json
insertOrder | timeInQueue | priority | source
  1786      |    1.8s     |  URGENT  | shard-started
```
