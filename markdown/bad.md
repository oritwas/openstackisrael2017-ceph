## The bad


## Performance


### Latency

Note: Explain how block device latency isn’t exactly RBD’s strong
suit, and what we can do to mitigate that (such as `disk_cache_mode =
network=writeback`).


### Lots of objects in a single container/bucket

Note: If number of objects in a bucket index shard exceeds 100K  there is a drop in performance


### Indexless bucket

Note: Buckets without a bucket index, no bucket listing and no Geo replication support


### offline bucket resharding

Note: User can change bucket index shards number, currently only when the bucket is offline.


### dynamic bucket resharding

Note: From Luminous we will  increase the number of bucket index shards automatically


## Swift compatibility

Note: Explain shortcomings vs. the current Swift API.


### EXT4 as  a backend for Ceph

Note: Due to limitation of the xattrs size it can store, users can only run with osd max object name len = 256 and
osd max object namespace len = 64.
