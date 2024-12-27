# MongoDB Aggregation Pipeline Bug
This repository demonstrates a common error in MongoDB aggregation pipelines where applying the `$limit` stage before the `$sort` stage leads to incorrect results when trying to retrieve the top N documents.

## Bug Description
The provided code snippet attempts to find the top 10 most frequent values in a field within a collection. However, due to the order of the `$limit` and `$sort` stages, the results are inaccurate. The `$limit` stage restricts the number of documents before sorting, resulting in a top 10 based on the unsorted data.