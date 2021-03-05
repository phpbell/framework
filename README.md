# Bell

Framework em PHP funcional com views em PHP puro e models com [Medoo](https://medoo.in)

## Instalação

```bash
composer install Bell/Bell
```

## Hello world

index.php

```php
<?php
require 'vendor/autoload.php';
$cfg=[
    'db'=>[
        // required
        'database_type' => 'mysql',
        'database_name' => 'teste',
        'server' => 'localhost',
        'username' => 'root',
        'password' => ''
    ],
    'root'=>'/var/www/html/exemplo',
    'showErrors'=>true,
    'url'=>'http://public.local',
    'localhost'=>'http://localhost/pb'
];
$bell=new Bell\Bell($cfg);
$bell->view('home','world');
?>
```

view/home.php

```php
<?php
return function($str){
    print 'hello '.$str;
};
