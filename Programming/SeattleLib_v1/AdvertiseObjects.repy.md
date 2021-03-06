# AdvertiseObjects.repy

Provides two objects which makes advertising more efficient. Can be used as an alternative to [wiki:Advertise.repy].

LookupCache caches lookup results to increase performance in programs which calls lookup services frequently.

AdvertisePipe stores a list of (key, value) tuples and advertises them concurrently in a single thread. 

# Functions

LookupCache
```
lookup(self, key, maxvals=100, lookuptype=['central','opendht','DOR'], concurrentevents=2, graceperiod=10, timeout=60)
```
   Exactly the same as [advertise.repy](advertise.repy.md).
   Note:

   * self refers to its own cache.

AdvertisePipe
```
add(self, key, value)
```
   Adds a (key, value) pair to the advertise pipe.
   Note:

   * self refers to its own cache.
   * Each value added is given an unique handle, which is used in remove.

```
remove(self, handle)
```
   Removes a (key, value) pair from the advertise pipe.
   Note:

   * handle is an unique identifier for each value in the advertise pipe.
   * self refers to its own cache

# Usage

no examples?

# Includes
[advertise.repy](advertise.repy.md)
