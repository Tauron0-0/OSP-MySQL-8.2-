OSP модуль MySQL-8.2 не работает

Ошибка на сайте:
Fatal error: Uncaught mysqli_sql_exception: Access denied for user 'mysql'@'localhost' (using password: YES) in C:\OSPanel\home\STALCRAFT_X_SPARTA.local\php\index.php:71 Stack trace: #0 C:\OSPanel\home\STALCRAFT_X_SPARTA.local\php\index.php(71): mysqli->__construct('localhost', 'mysql', Object(SensitiveParameterValue), 'sparta') #1 {main} thrown in C:\OSPanel\home\STALCRAFT_X_SPARTA.local\php\index.php on line 71

Код:
    <?php
    $mysql = new mysqli("localhost", "mysql", "mysql", "sparta");
 
    if ($mysql->connect_error) {
        die("Conecrt Eror I losh". $mysql->connect_error);
    }
    ?>

На скриншоте отображаеться панель OSP

При открытии консоли разраба OSP пишет что MySQL-8.2 выключен

При попытке ручного запуска выбивает ошибку:
C:\OSPanel>mysql -u root -p
Enter password: ****
ERROR 2005 (HY000): Unknown MySQL server host 'MySQL-8.2' (11001) 
![image](https://github.com/user-attachments/assets/bf0df5c6-b148-4611-8313-14bbbf04f4a4)
