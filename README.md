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
 
3. Install **migrations**, create migration and migrate
    ```
    composer require migrations
    ```
   
   

## ...
