# Caching

Caching is used to speed up and improve *latency* of a system. Also, caching will store data in a new location, other than data source itself, making data retreival faster as compared to initial storage of data.

Ex:

* Clients makes request to the servers which retrieves data from DB. **Cache** can be placed at Client or Server level if same request comes in the future.
* Multiple clients make multiple network requests to the servers. We can redirect requests to the cache instead of DB, or every server can have its own cache.

**Two Cache Systems:** Write Through Cache & Write Back Cache

First type: When some data appears, it’ll be written to both cache and DB. Weak point? Requires a visit to DB every time.

Second type: When some data appears, system will update **only** the cache at first and go back to the client. Now the cache is out of sync with DB. The system will asynchronously update cache with DB(ex. every 5 secs/min etc or when cache gets full). Weak point? If system crashes before DB gets updated with cache, the updated data is lost.

**Stale cache** are cache with old data(that hasn’t been updated yet). Example: if YouTube had caches on the servers, then some comments may not be updated properly.

**Cache Eviction Policy** is a technique by which data gets evicted from the system. Ways: LRU (least-recently used), FIFO, LFU (least-frequently used).

We can use **CDN**(Content Delivery Network) which acts like a cache for our system.

![Key Terminologies](ImageRepo/Caching.png?raw=true)
