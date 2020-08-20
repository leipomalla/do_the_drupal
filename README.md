Install Drupal with Composer. You can check wheather you have Composer by writing composer -v to command line. I didn't want D9 since yet so i wrote "composer create-project drupal/recommended-project:^8.8@dev -n --no-dev do_the_drupal", do_the_drupal being the name I chose.

Create a database for your project. I followed instructions from digital ocean: 

To begin, log into MySQL:

mysql -u root -p

CREATE DATABASE drupal;

CREATE USER drupaluser@localhost IDENTIFIED BY 'password';

GRANT SELECT,INSERT,UPDATE,DELETE,CREATE,DROP,INDEX,ALTER,CREATE TEMPORARY TABLES,LOCK TABLES ON drupal.* TO drupaluser@localhost;

FLUSH PRIVILEGES;

exit



“If there is an older version of drush installed, and you don’t want to update it, or it is impossible to install drush to the server (as in shared hosting it can be) you can also use the project’s own drush from vendor/…“.
