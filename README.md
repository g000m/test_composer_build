Avalara Composer Demonstration
============

This script provides a workflow to manage Wordpress installation and setup. Through a user prompt in the command line you can:
* Install a specific version of Wordpress with Composer.
* Setup WP core in a custom directory (site up and running in http://localhost/yoursite).
* Move wp-config.php from WP core directory (https://wordpress.stackexchange.com/questions/58391/is-moving-wp-config-outside-the-web-root-really-beneficial).
* Create DB in your local system (if it doesn't exist).
* Custom wp-content directory, outside WP folder (the script does the needed modifications to wp-config.php file).

In just a few minutes, you will have a fresh Wordpress installation.

At the moment, this just installs a bare WordPress file set. We are working to include actions to download and restore a database and the uploaded files. 

## System requirements:

Before getting started, make sure you have installed, up and running:

- PHP 5.6.+
- Composer: https://getcomposer.org/.
- WP CLI: https://wp-cli.org/
- Node.js: https://nodejs.org/en/
- Grunt: http://gruntjs.com/

## Setting up a github access key

As some of the code in this sample is pulled from our github private repositories, you'll need to configure your system to use your Github key when you run the script. 

__To set up a Github key__
1. Log in to Github and visit https://github.com/settings/tokens. 
2. Click __Generate new token__. 
3. Type a description for the token.
4. Check the __repo__ box at the top of the scopes list.  
5. Click __Generate token__

Use the new token value as an option in the following composer command. Use your Github user name and the token value below. 

```bash
$ composer config -g http-basic.github.com {GitHubUserName} {NewToken}
```

This creates an `auth.json` file in the `.composer` subdirectory of your user folder. Composer will use the values here to authenticate whenever it connects to Github.  

## Do it

__1. Open a terminal, navigate to your project folder and type:__

```bash
$ composer install
```

Wait a few minutes as it downloads the code and dependencies and places them in the folders defined in the file. 

If you make changes to any of the settings in the composer file, you can update the installation by typing:

```bash
$ composer update
```

## References

1. http://roots.io/using-composer-with-wordpress/
2. https://deliciousbrains.com/how-why-install-wordpress-core-subdirectory/
