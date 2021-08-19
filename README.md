Cloudflare CLI Add-On
=====================

Requires [Cloudflare](https://wordpress.org/plugins/cloudflare/) 3.4+.

Provides a command line interface to the [WordPress Cloudflare plugin](https://www.cloudflare.com/integrations/wordpress/), for performing cache purge actions. 

Quick links: [Using](#using) | [Installing](#installing)

## Using

~~~
wp cloudflare cache_purge
~~~

Clears all cached files to force Cloudflare to fetch a fresh version of those files from your web server.

**EXAMPLES**

    # Flush Cloudflare cache after new code deployment.
    $ wp cloudflare cache_purge
    Success: Entire site cache on Cloudflare purged.

## Installing

This package depends on the `\CF\WordPress\Hooks` class from the [Cloudflare for WordPress](https://wordpress.org/plugins/cloudflare/) plugin. Make sure it is installed and active.

### Via WP-CLI

```bash
wp package install https://github.com/sterner-stuff/cloudflare-cli
```

### Using Composer

```bash
composer config repositories.cloudflare-cli '{ "type": "vcs", "url": "git@github.com:sterner-stuff/cloudflare-cli.git" }'
composer require sterner-stuff/cloudflare-cli
```

