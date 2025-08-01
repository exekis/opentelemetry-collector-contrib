[comment]: <> (Code generated by mdatagen. DO NOT EDIT.)

# paging

## Default Metrics

The following metrics are emitted by default. Each of them can be disabled by applying the following configuration:

```yaml
metrics:
  <metric_name>:
    enabled: false
```

### system.paging.faults

The number of page faults.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {faults} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values | Optional |
| ---- | ----------- | ------ | -------- |
| type | Type of fault. | Str: ``major``, ``minor`` | false |

### system.paging.operations

The number of paging operations.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {operations} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values | Optional |
| ---- | ----------- | ------ | -------- |
| direction | Page In or Page Out. | Str: ``page_in``, ``page_out`` | false |
| type | Type of fault. | Str: ``major``, ``minor`` | false |

### system.paging.usage

Swap (unix) or pagefile (windows) usage.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | false |

#### Attributes

| Name | Description | Values | Optional |
| ---- | ----------- | ------ | -------- |
| device | Name of the page file. | Any Str | false |
| state | Breakdown of paging usage by type. | Str: ``cached``, ``free``, ``used`` | false |

## Optional Metrics

The following metrics are not emitted by default. Each of them can be enabled by applying the following configuration:

```yaml
metrics:
  <metric_name>:
    enabled: true
```

### system.paging.utilization

Swap (unix) or pagefile (windows) utilization.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Double |

#### Attributes

| Name | Description | Values | Optional |
| ---- | ----------- | ------ | -------- |
| device | Name of the page file. | Any Str | false |
| state | Breakdown of paging usage by type. | Str: ``cached``, ``free``, ``used`` | false |
