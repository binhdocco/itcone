## CREATED by Binh Justin 12 Oct, 2024 under MIT license

## ABOUT THE PROJECT

Building a website with Drupal10 including:

- Containerization tool
    - Docker and Lando plugin
- Component-driven architecture:
    + Each section will be a component containing list of fields for inputting data (text & image)
    + Components can be re-ordered on edition page
- Multilingual
    + English (default): /
    + Simplified Chinese: /zh-hans
- Metatag supported
- The website has a simple Home page and the demo AboutUs page and Page-not-found page.
- URLs to AboutUs page:
    + EN: /about-us
    + ZH-HANS: /zh-hans/about-us
- CSS+JS:
    + The website focus on building content with Drupal10, reusing existing CSS from https://it-consultis.com/about-us/
    + Due to the different approach, the JS from https://it-consultis.com/about-us/ is not compatible, therefore no JS added to the page.

## PREREQUISITES

- PHP ver 8.1 or above
- Composer

## HOW TO INSTALL

- Git clone from https://github.com/binhdocco/itcone.git
- Go to folder: itcdrupal
- Open command line at the current directory, run:
    composer remove drush/drush

- Copy&Rename the file /.dev/settings.php.sample TO /web/sites/default/settings.php

## If you HAVE Lando installed, from /itcdrupal, run:
    lando start
    lando composer require drush/drush
    lando theme-import
    lando drush cr

## If you DONOT have Lando installed 
- create a database in your machine, and update the database info in /web/sites/default/settings.php
- import sample sql from /.dev/theme_database.sql.gz into your database
- extract /.dev/theme_files.tgz to /web/sites/default/files

## Open the website's url
- If using Lando: http://itcone.local.lndo.site/ 
    
## Admin user: 
- Username: admin
- Password: theAdmin123@