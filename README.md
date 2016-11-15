Starter pack
============

This script offer a workflow to manage Wordpress installation and setup very easily. Through a user prompt in the command line you can:

* Install the latest version of Wordpress with Composer.
* Setup WP core in a custom directory (site up and running in http://localhost/yoursite).
* Move wp-config.php from WP core  directory (https://wordpress.stackexchange.com/questions/58391/is-moving-wp-config-outside-the-web-root-really-beneficial).
* Create DB in your local system (if it doesn't exist).
* Custom wp-content directory, outside WP folder (the script does the needed modifications to wp-config.php file).
* WP-SYNC plugin to manage your DB through different enviroments.

In 5 minutes, you will have a fresh Wordpress installation, with a lot of security and performance tweaks, plugins and more.

It manages Wordpress installation with Composer. Set up is done with WP-CLI and BASH scripting. At the end, cames Grunt to edit and move some files/folders.


## System requeriments:

Before getting started, make sure you have installed, up and running:

- PHP 5.3.2+
- Composer: https://getcomposer.org/.
- WP CLI: https://wp-cli.org/
- Node.js: https://nodejs.org/en/
- Grunt: http://gruntjs.com/



## Getting started

__1. In terminal, go to the project folder and type (as root, or using sudo):__

```bash
# WP_SUBDIR=wp; composer install;
# chmod +x wpconfigure.sh; wpconfigure.sh
```

## References

1. https://github.com/micahblu/wp-launchpad
2. http://roots.io/using-composer-with-wordpress/
3. https://deliciousbrains.com/how-why-install-wordpress-core-subdirectory/
