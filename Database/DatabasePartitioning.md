# Database Partitioning
Any application or website that sees significant growth will eventually need to scale in order to accommodate increases in traffic. For data-driven applications and websites, it’s critical that scaling is done in a way that ensures the security and integrity of their data. It can be difficult to predict how popular a website or application will become or how long it will maintain that popularity, which is why some organizations choose a database architecture that allows them to scale their databases dynamically.

### What are the types?
There are two types of partitioning:
1. Horizontal
2. Vertical

### What is horizontal partitioning?
It's the practice of separating one table’s rows into multiple different tables, known as partitions. Each partition has the same schema and columns, but also entirely different rows. Likewise, the data held in each is unique and independent of the data held in other partitions.

### What is vertical partitioning?
In a vertically-partitioned table, entire columns are separated out and put into new, distinct tables. The data held within one vertical partition is independent from the data in all the others, and each holds both distinct rows and columns.

![](https://assets.digitalocean.com/articles/understanding_sharding/DB_image_1_cropped.png)
*src:* https://assets.digitalocean.com/articles/understanding_sharding/DB_image_1_cropped.png