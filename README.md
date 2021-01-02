# PHP Login Register

PHP dilinde yazılmış simple login register sistemi.
Simple login register system written PHP.


# Database

CREATE TABLE IF NOT EXISTS `users` (
 `id` int(11) NOT NULL AUTO_INCREMENT,
 `username` varchar(50) NOT NULL,
 `email` varchar(50) NOT NULL,
 `password` varchar(50) NOT NULL,
 `create_datetime` datetime NOT NULL,
 PRIMARY KEY (`id`)
);

# Note

Eğer farklı bir sayfaya kullanıcı girişi session kontrolü yaptırmak isterseniz aşağıdaki kodu yeni eklediğiniz sayfanın en üstüne eklemeniz yeterlidir.
If you want to have a user login session control on a different page, simply add the following code to the top of the page you just added.

<?php
require('db.php');
include("auth_session.php");
?>
