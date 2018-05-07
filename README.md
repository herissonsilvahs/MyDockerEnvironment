Workspace with docker compose, including:
    - php 7.2
    - apache2
    - mysql 5.7.22

- Reading htaccess file
- Laravel projects tested and working

Usage:
    Setup configurations in docker-compose.yml

    WebSites projects is insert in html folder

    Folder apache2-php-7.2 is local to apache and php configuration files

    When to up in the first time, is required use option --build in compose command:
        $ docker-compose up --build
