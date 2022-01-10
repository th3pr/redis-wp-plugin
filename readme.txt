== Installation ==

For detailed installation instructions, please read the [standard installation procedure for WordPress plugins](http://codex.wordpress.org/Managing_Plugins#Installing_Plugins).

1. Make sure [Redis is installed and running](http://redis.io/topics/quickstart).
2. Install and activate plugin.
3. Enable the object cache under _Settings -> Redis_, or in Multisite setups under _Network Admin -> Settings -> Redis_.
4. If necessary, adjust [connection parameters](http://wordpress.org/extend/plugins/redis-cache/other_notes/).

If your server doesn't support the [WordPress Filesystem API](https://codex.wordpress.org/Filesystem_API), you have to manually copy the `object-cache.php` file from the `/plugins/redis-cache/includes/` directory to the `/wp-content/` directory.


== Connection Parameters ==

By default the object cache drop-in will connect to Redis over TCP at `127.0.0.1:6379` and select database `0`.

To adjust the connection parameters, client, timeouts and intervals, please see the [connection parameters wiki page](https://github.com/rhubarbgroup/redis-cache/wiki/Connection-Parameters).


== Configuration Options ==

The plugin comes with quite a few configuration options, such as key prefixes, a maximum time-to-live for keys, ignored group and many more.
