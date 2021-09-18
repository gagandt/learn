# Sharding
Sharding is a database architecture pattern related to horizontal partitioning[^1]. Ideally, it exemplifies a shared-nothing architecture.

> Sharding involves breaking up one’s data into two or more smaller chunks, called **logical shards**. The logical shards are then distributed across separate database nodes, referred to as **physical shards**, which can hold multiple logical shards. Despite this, the data held within all the shards collectively represent an entire logical dataset.

### What is shared-nothing architecture?
This means that the shards are autonomous; they don’t share any of the same data or computing resources.

### Benefits?
1. The main appeal of sharding a database is that it can help to facilitate horizontal scaling, also known as *scaling out*.
2. Another reason why some might choose a sharded database architecture is to speed up query response times.
3. Sharding can also help to make an application more reliable by mitigating the impact of outages. If your application or website relies on an unsharded database, an outage has the potential to make the entire application unavailable. With a sharded database, though, an outage is likely to affect only a single shard.

### Disadvantages?
1. The first difficulty that people encounter with sharding is the sheer complexity of properly implementing a sharded database architecture. If done incorrectly, there’s a significant risk that the sharding process can lead to lost data or corrupted tables. Even when done correctly, though, sharding is likely to have a major impact on your team’s workflows. Rather than accessing and managing one’s data from a single entry point, users must manage data across multiple shard locations, which could potentially be disruptive to some teams.
2. Shards eventually become unbalanced.
3. Once a database has been sharded, it can be very difficult to return it to its unsharded architecture. Rebuilding the original unsharded architecture would require merging the new partitioned data with the old backups or, alternatively, transforming the partitioned DB back into a single DB, both of which would be costly and time consuming endeavors.
4. Sharding isn’t natively supported by every database engine.

#### References
1. https://www.digitalocean.com/community/tutorials/understanding-database-sharding

[^1]: https://github.com/gagandt/learn/blob/main/Database/DatabasePartitioning.md#what-is-horizontal-partitioning