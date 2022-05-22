# HTTP API with Symfony 5

Make simple CRUD operations with HTTP Protocols.

> GUI available [here](https://gitlab.com/k.serbouty/http-gui).
---

## Features

- Coverage of CRUD operations.
- JSON format.

## API

### Parameters

| Parameter   | Type   |
|-------------|--------|
| name        | string |
| description | string |
| quantity    | int    |
| price       | int    |

### Endpoints

| HTTP   | Endpoints             |
|--------|-----------------------|
| POST   | /api/json/create      |
| POST   | /api/query/create     |
| GET    | /api/json/get         |
| GET    | /api/json/get/{id}    |
| PATCH  | /api/json/update/{id} |
| PUT    | /api/json/update/{id} |
| DELETE | /api/json/delete/{id} |


## Requirements

- Composer
- PHP >=7.2.5

### Installation

Install dependencies
```
composer install
```

Configure database (.env or .env.local) with your credentials
```
DATABASE_URL="mysql://db_name:db_password@127.0.0.1:3306/db_name?serverVersion=8.0"
```

Create database
```
php bin/console doctrine:database:create
```

Update database schema
```
php bin/console doctrine:migrations:migrate
```

Create products

```
php bin/console doctrine:fixtures:load
```

Run

```
php -S localhost:8000 -t public
```

You can now run the [GUI](https://gitlab.com/k.serbouty/http-gui) too and interact with your products.

## Authors

Karim Serbouty

## License

Source code is licensed under the [MIT license](./LICENSE.md).