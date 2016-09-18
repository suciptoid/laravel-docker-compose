# Laravel docker-compose
Run laravel on docker container

# Stack
- Apache2 + PHP
- Mariadb

# Using
- Assuming you're have `docker` and `docker-compose` installed on your machine
- Put `docker-compose.yml` into your laravel project
- Run `docker-compose up` to run your laravel app
- Or run with `-d` option to make it's run in the background `docker-compose up -d`

# Access Container
- Run `docke-compose run web bash` to connect web container and promt bash shell
- Run command, eg: database migration

# Example
```
# On local machine
$ docker-compose run web bash

# On Docker container
root@f8dda0701634:/# cd /var/www/laravel
root@f8dda0701634:/var/www/laravel# ./artisan migrate --seed

Migration table created successfully.
Migrated: 2014_10_12_000000_create_users_table
Migrated: 2014_10_12_100000_create_password_resets_table
Migrated: 2015_01_20_084450_create_roles_table
Migrated: 2015_01_20_084525_create_role_user_table
Migrated: 2015_01_24_080208_create_permissions_table
Migrated: 2015_01_24_080433_create_permission_role_table
Migrated: 2015_12_04_003040_add_special_role_column
Migrated: 2016_08_24_150712_create_projects_table
Migrated: 2016_08_25_171213_create_applications_table
Seeded: UserSeeder
Seeded: ProjectSeeder
```
