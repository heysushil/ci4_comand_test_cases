# Comands and their change cases:

## Ci4 instalation command

    composer create-project codeigniter4/appstarter project-root

## If you don’t need or want phpunit installed, and all of its composer dependencies:

    composer create-project codeigniter4/appstarter --no-dev

## Upgrading: after any major modification update composer

    composer update

## Latest dev changes

    php builds development

>> The command above will update composer.json to point to the develop branch of the working repository, and update the corresponding paths in config and XML files. To revert these changes run:

## Translations Installation: use to change project language partail change not full

This is one of the greate way to change project langauge learn more here [Translations Installation](https://codeigniter4.github.io/CodeIgniter4/outgoing/localization.html)

    composer require codeigniter4/translations

## You can check the current environment by spark env command:

    php spark env

## Remove index.php form url

Create `.htaccess` file on root directory and add this code on it

    RewriteEngine On
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteCond %{REQUEST_FILENAME} !-d
    RewriteRule ^(.*)$ index.php/$1 [L]

## Virtual Hosting: 

We recommend using “virtual hosting” to run your apps. You can set up different aliases for each of the apps you work on,

Make sure that the virtual hosting module is enabled (uncommented) in the main configuration file, e.g., `apache2/conf/httpd.conf`:

    LoadModule vhost_alias_module modules/mod_vhost_alias.so

## Run on different port:

    php spark serve --port 8081