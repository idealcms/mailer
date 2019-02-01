# Ideal CMS Mailer v.5.0
Максимально простой отправщик писем на PHP (с поддержкой отправки через SMTP)

Является компонентом Ideal CMS, но может работать и отдельно.

Письма отправляются только в UTF-8, на все входящие параметры
(тема письма, содержание письма) должны быть тоже в UTF-8
 
Пример использования:
 
    $mail = new Ideal\Mailer();
    $mail->setSubj('Это тема письма'); // устанавливаем тему письма
    $mail->setHtmlBody($htmlText); // письмо отправляем в html-формате
    // Прикрепляем файл /var/tmp/bla-bla.jpg под именем picture.jpg
    $mail->fileAttach('/var/tmp/bla-bla.jpg', 'image/jpg', 'picture.jpg');
    // Отправляем письмо с ящика my@email.com на ящики other@email.com, second@email.com
    $mail->sent('my@emai.com', 'other@email.com, second@email.com');
