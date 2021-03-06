---
title: How to clear the cache
---

There are three ways to remove objects from the Varnish cache:

1. Clear the cache by a particular url.
1. Clearing the entire cache.
1. Fine tuned control of the cache with Varnish ban expressions.

### Clear a particular URL

You can remove particular URLs from the cache by entering the URL and clicking **Purge**.
This form accepts wildcards in the form of `*`, so entering `/images*` will purge all URLs starting with `/images`. You can also clear the cache for a specific URL, for example `https://www.example.com/assets/css/styles.css`.

### Empty the entire cache

This will remove **everything** from the cache. Use this if the cache is completely out of date and it needs to be refreshed.

NOTE: This may cause increased load on your origin server and also slow down your website for users until we are able to refill the cache.

### Varnish ban expressions

You can think of bans as a way to purge or filter out object that are already in the cache. Keep in mind that this method does not ban future requests from being stored in the cache.

Support for bans are built into Varnish so to learn how to use bans, see the [Varnish Cache documentation](https://www.varnish-cache.org/docs/trunk/users-guide/purging.html#bans).
