# API Platform Tutorial
[API Platform](https://symfonycasts.com/screencast/api-platform)

## Setup
1. **Download Composer dependencies**
    ```
    composer install
    composer require    
    ```
    You may alternatively need to run `php composer.phar install`, depending
    on how you installed Composer.

2. **Start the built-in web server**
    
    ```
    symfony server:
    
    symfony serve
    ```
    (If this is your first time using this command, you may see an
    error that you need to run `symfony server:ca:install` first).

3. **Install API Platform**
    ```
    composer require api 
    ```

4. Check Documentation
    ```
    http://127.0.0.1:8000/api
    ```
   
## Concept of API-Platform 
Instead of thinking about routes, controllers and responses, API Platform wants you to think about creating 
API resources - like CheeseListing - and then exposing that resource in a variety of different formats, 
like JSON-LD, normal JSON, XML or exposing it through a GraphQL interface.

## Database Entities
1. Change **.env**
    ```
    DATABASE_URL=mysql://root:@127.0.0.1:3306/cheese_wiz
    ```
   
2. Install **maker** bundle and create *CheeseListing* entity and add some fields
    ```
    composer require maker --dev
    php bin/consolse make:entity
    ```
    Create database: 
    ```
    php bin/console doctrine:database:create
    ```
    
3. Install **migrations**, create migration and migrate
    ```
    composer require migrations
    php bin/console make:migration
    php bin/console doctrine:migrations:migrate
    ```
   
## Swagger-UI / Open-API
[Tutorial](https://symfonycasts.com/screencast/api-platform/swagger#play):  
**Swagger UI** is Interface and reads/displays Json file in **Open-API** format.
**Swagger Codegen** to create SDK for API in various languages.


Check **API**
```angular2 
http://127.0.0.1:8000/api
```

testing and checking: add 2 cheeses and send  request:
```angular2 
http://127.0.0.1:8000/api/cheese_listings/2.jsonld
```

Set to OpenApi 3 version:
```angular2 
http://127.0.0.1:8000/api?spec_version=3
http://127.0.0.1:8000/api/docs.json
http://127.0.0.1:8000/api/docs.json?spec_version=3
```

## JSON-LD / RDF

## ...
