# couchbase-query-executor

A library for filterable and sortable lists in SpringData with CouchBase using N1QL query. You can read more about this lib in [this blogpost](http://leaks.wanari.com/2016/10/24/couchbase-can-make-filterable-list-springdata/?utm_source=github&utm_medium=20161024&utm_campaign=suxy).

This is an updated version of [TeamWanari/couchbase-query-executor](https://github.com/TeamWanari/couchbase-query-executor).
Read more about installation and usage there.

## Updated features

- Fixes some issues with Couchbase 4.6.1

- Additional filters

|**Filter**|**Description**|**Example use**|
|---|---|---|
|null|Selects when field exists and is null|`JsonObject.create().put("fieldName" + CouchbaseQueryExecutor.NULL_FILTER, JsonObject.empty());`|
|not null|Selects when field exists and is not null|`JsonObject.create().put("fieldName" + CouchbaseQueryExecutor.NOT_NULL_FILTER, JsonObject.empty());`|
|missing|Selects when field does not exist|`JsonObject.create().put("fieldName" + CouchbaseQueryExecutor.MISSING_FILTER, JsonObject.empty());`|
|null or missing|Selects when field is not null or does not exist|`JsonObject.create().put("fieldName" + CouchbaseQueryExecutor.NULL_OR_MISSING_FILTER, JsonObject.empty());`|


