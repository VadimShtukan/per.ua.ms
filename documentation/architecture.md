# Architecture

## Services Decomposition 

Декомпозизая сервисов была произведена на основе пользовательского сценария - https://github.com/VadimShtukan/per.ua.ms/blob/master/documentation/use_case/create_order.md. В результате были выделены следующие сервисы:
- Сервис пользователей (User service):
    - Информация о пользователях.
    - Генерация токенов для пользователей.
    - Аутентификация пользователей.
    - Привязка пользователей к группам.
    - Вернуть UserId по номеру телефона. 
- Сервис товаров (Product service):
    - Описание и характеристики товаров, изображение.
    - Товарные остатки.
    - Вычисление стоимости товаров от базовой цены (в зависимости от курса доллара)
- Сервис заказов(Order service):
    - Информация о заказе, товары в заказе, общая сумма заказа.
    - Информация о доставке заказе.
    - Статусы заказов.
    - История изменения заказов.
    - напоминание пользователей о неоплаченных заказах. Автоматическая отмена неоплаченных заказов. 
- Сервис корзины (Cart Service):
    - Подсчет суммы заказа в корзине.
    - Хранение корзин покупателей.
    - Анализ не закрытых корзин и информирование об этом покупателей.
- Сервис для отправки уведомлений - почта, СМС, Telegram, Viber (Notification service).
    - Формирование текста уведомления.
    - Принятие решения по способу доставки сообщений.
    - Контроль доставки сообщений.
- Сервис скидок (Discount Service):
    - Подсчет скидки для покупателя.
    - Начисление/списание скидок.
- Сервис оплат (Payment Service)
    - взаимодействие с провайдерами приема оплат.
    - контроль оплат и Информирование Order сервиса об успешной оплате.
- Сервис(ы) формирования чеков (Bills Service)
    - Формирование нефиксальных чеков.
    - Формирование фиксальных чеков через РРО.
    - Формирование Z отчетов в налоговую.
- Сервис(ы) для взаимодействия с серверами служб доставки(Delivery Service)
    - создание декларация
    - напоминание о незабранных посылках
    

## Диаграммы бизнес процессов
![Image description](https://github.com/VadimShtukan/per.ua.ms/blob/master/documentation/img/create_order_1.png)  
![Image description](https://github.com/VadimShtukan/per.ua.ms/blob/master/documentation/img/create_order_2.png)    
![Image description](https://github.com/VadimShtukan/per.ua.ms/blob/master/documentation/img/create_order_3.png)    
![Image description](https://github.com/VadimShtukan/per.ua.ms/blob/master/documentation/img/create_order_activity_1.png)    
![Image description](https://github.com/VadimShtukan/per.ua.ms/blob/master/documentation/img/order_flow_activity_1_2.png)    
![Image description](https://github.com/VadimShtukan/per.ua.ms/blob/master/documentation/img/order_flow_activity_3.png)

## Межсервисное взаимодействия    
![Image description](https://github.com/VadimShtukan/per.ua.ms/blob/master/documentation/img/services.png)    





 
