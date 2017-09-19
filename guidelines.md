TransferRules Project Guideline by #team-differential
===================


DESCRIPTION
----------
Set of COMPULSORY rules, guidelines and naming conventions to ensure uniformity in the codebase we are building .

Please adhere to these guidelines oo . Na beg we take beg una


GENERAL
----------
Tables, records should not be done via PHPMyAdmin , mysql via terminal or any other mysql client . Any changes to the database should be done via a migration to ensure that everyone is using the same database 
  use snake case example : ( user_credentials ) .

2. migrations
----------
When naming your migrations , The following format is to be used

create_{tablename}_table.php  ( tablenames must be plural) e.g : (create_users_table) 

For example , say I want to make a migration to create the users table , i would name it like this :
```php
$ php artisan make:migration create_users_table
```
3. models
----------
When naming models , the following format must be used ;

For single words , start with a capital letter and ensure it is the Singular version of tablename e.g : (User) for a table named users 

For example , say I want to make a model for the users table , i would name it like this :
```php
$ php artisan make:model User
```
4. controllers
----------
When naming controllers , the following format must be used ;

Use Pascal case or StudlyCaps ( means that the first letter of every word is capitalized ) and then append controller to it e.g: (LoginController)

For example , say I want to make a login controller  , i would name it like this :
```php
$ php artisan make:controller LoginController
```
5. seeders
----------



When naming your seeders , the following format must be used ;

Use Pascal case or StudlyCaps ( means that the first letter of every word is capitalized ) . The seeder must start with the table name . For example, if we want to create a seeder to populate the users table , we would have  : UsersTableSeeder .

```php
$ php artisan make:seeder UsersTableSeeder
```

6. variables
----------

Use lower case for single words whilst multiple words should be seperated by an underscore (snake_cased) example: $wallet_status and $wallet



When naming your variables , the following format must be used ;

Use lower case for single words whilst multiple words should be seperated by underscore (snake_cased) example: $wallet_status and $wallet

```php
$  $wallet_status ="FLEX MODE"; $wallet="LOADED";

```

7. constants
----------

Class constants MUST be declared in all upper case with underscore separators example : ( SAMPLE_CONSTANT )





```php
$  const WHAT_DO_YOU_WANNA_DO ="FLEX"; 

```


8. functions/methods
----------

Use Camel case for multiple words and lower case for single words e.g : function updateWallet(); and function update (); 





```php
$  public function updateWalletOnce();
$  public function spendTheMoney();

```

9. folders
----------

Folders containing files should correspond with the files they contain . e.g The Models folder will contain models, the  Controllers folder will contain controllers . Also ensure you  maintain the folder structure .

10. column names
----------

Column names should be explanatory . For example : ( user_email ) explains to us that the column is meant for emails . Arbitrary column names are not allowed. Also use snake case for multiple words i.e everything would be in lower letters and an underscore should be used to seperate multiple words .

11. API endpoints
----------

API endpoints should be explanatory and easy to guess e.g https://domain.com/v2/user/{id}/wallet, https://domain.com/v1/user/{id}/transactions

12. assets ( images, stylesheets )
----------

All public assets should go into the public folder and be organized .

13. primary keys
----------

primary keys should be named "id" in their table .

14. foreign keys
----------

foreign keys should be prepended by their table name in snake case . Example : a table called users would have a column called transaction_id which references the id in the transactions table .














REFERENCES
-------------
In compiling these guidelines , resources were consulted in order to esnure we follow the community accepted best practices .

> 

> - The official [Laravel](https://laravel.com/docs)   </a> documentation 
> - [http://www.laravelbestpractices.com](http://www.laravelbestpractices.com/)











