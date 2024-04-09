## RUNNING WORDPRESS WEBSITE WITH DOCKER

In this guide you can find information how to run copy of your WordPress website with Docker.

1. Create new project folder
2. Copy Dockerfile, docker-compose.yml, and .env files into the new folder
3. Create "src" folder, and copy all files from your website root folder
4. Change MySQL settings in wp-config.php in accordance with variables in .env file
5. Add these lines to wp-config.php:

```
define( 'WP_HOME', 'http://localhost:3000' );
define( 'WP_SITEURL', 'http://localhost:3000' );
```

6. Run "docker-compose build" and "docker-compose up"
7. Open PHPMyAdmin and import data from your SQL dump to "wordpress_db" table
8. In PHPMyAdmin change password for WordPress admin in "wp24_users" table
9. Open your website on localhost:3000 and login to WordPress admin
