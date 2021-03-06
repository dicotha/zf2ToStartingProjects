Skeleton Zend FrameWork 2 by Waldir Bertuqui
=======================

Introduction
------------
This repository is a simple way to start my projects in Zend Framework 2

Has:
 - Zend Developer Tools
 - Doctrine
 - ZFtools CLI
 - Bootstrap 4
 

Installation using git
---------------------------
Clone this repository, open the git bash if you use Windows or open your Command line of your preference.

Navigate to the folder root, execute the command line below

```sh
composer install

```
Before that, go to folder 
```sh
vendor\zendframework\zend-developer-tools\config
```
copy the file zenddevelopertools.local.php.dist and send the copy to folder :
```sh
config\autoload
```
Rename the file to "zdt.local.php"

In this same folder create a file with the name doctrine.local.php and put this code below inside
```sh
<?php
return array(
    'doctrine' => array(
        'connection' => array(
            'orm_default' => array(
                'driverClass' =>'Doctrine\DBAL\Driver\PDOMySql\Driver',
                'params' => array(
                    'host'     => 'localhost',
                    'port'     => '',
                    'user'     => 'root',
                    'password' => '',
                    'dbname'   => 'sis3',
                )))));
```

Go to your mysql and create a db called sis3

Still in the folder root execute this command to validate your db

```sh
./vendor/bin/doctrine-module orm:validate-schema

```
Before the steps above, go to the folder public and run this command in bash:
```sh
$ php -S localhost:8080
```

Thanks 


Waldir Bertuqui Neto
