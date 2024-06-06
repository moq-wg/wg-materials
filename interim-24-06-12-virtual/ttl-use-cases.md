## Use Case #1 - Cache Expiration
Publisher can hint to a relay or subscriber the maximum amount of time an object can be served out of a cache

* Caches do not have infinte resources.  Communicating a maximum duration helps the cache operate more efficiently.
* A cache can evict items before their maximum duration has passed for its own reasons
* Evicting or expiring an object from a cache should not change what objects are delivered for a subscription.

## Use Case #2 - Don't send what you won't use
Live and interactive applications require a mechanism that prevents delivery of data that is no longer useful

  1. In some applications, each subscriber might have a different useful duration<br>
    _Example_: variable size buffers behind live
  2. In some applications, the publisher always knows when objects are not useful<br>
    _Example_: TBD
  3. In some applications, the arrival of newer groups or objects may change what is useful<br>
    _Example_: Don't deliver object from groups more than 1 behind live head

Objects which arrive at a cache live may be cached and retrieved as VoD or live rewind.  A live subscriber might not
want to receive data older than say, 10 seconds, but the publisher might want that data to reside in a cache for up to 30 
minutes.
     
## Use Case #3 - Policy
Publisher can set a policy on a track indicating an absolute time after which an object must not be served

  1. This can stem from contractual obligations (eg: broadcast rights expire at a set time).

## Questions:

1. What is the appropriate granularity of exiry information?  Are there tracks and/or groups with objects that have different
   properties with respect to caching, delivery or policy?
2. Is it useful to have a flavor of publisher-specified cache expiration that also modifies object status from `Normal` to `Does Not Exist`?
