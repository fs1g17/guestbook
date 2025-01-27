# Guestbook

This project is a guestbook built with PHP Syfony, following the [The fast track](https://symfony.com/doc/6.4/the-fast-track/en/index.html).

## Running

### Prerequisits

- Git
- PHP
- Composer
- NodeJS
- Docker & Docker Compose
- Symfony CLI

Ensure the requirements are met with `symfony book:check-requirements`.

### Run

Start local server:
`symfony server:start -d`

Kill local server:
`symfony local:server:stop`

Start the postgresql database docker container
`docker compose up -d`

## Notes

### Project initialisation

Create project:
`symfony new guestbook --webapp --docker --cloud`

- `--webapp`: contains useful packages for building webapps
- `--docker`: enables Docker so that Symfony will automatically add Docker services based on teh required packages
- `--cloud`: automatically generates a sensible Platform.sh configuration

### Debugging

Get logs:
`symfony server:log`

Get env vars:
`symfony var:export`

### Development

Generate a controller:
`symfony console make:controller ControllerName`

Generate entity class:
`symfony console make:entity EntityName`

Generate migration:
`symfony console make:migration`

Run migration:
`symfony console doctrine:migrations:migrate`

Add EasyAdmin:
`symfony composer req "easycorp/easyadmin-bundle:4.x-dev"`

Create admin dashboard:
`symfony console make:admin:dashboard`

Generate CRUD:
`symfony console make:admin:crud`
