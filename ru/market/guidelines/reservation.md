# Бронирование столов


## Флоу интеграции

### Подключение и настройка

1. Клиент нажимает **Подключить** в маркете Poster → открывается страница приложения внутри админки Poster. \
☝️ При подключении приложения, постер автоматом включит триал брони на месяц. Потому что бронирование доступно только на тарифе Pro.

2. На странице отображаем: Название, адрес заведения, телефон владельца. Данные в эти поля подтягиваем из Poster, но их можно отредактировать. 
В одном аккаунте Poster может быть несколько заведений, тогда нужно выводить несколько полей для ввода.

3. Ввели данные → клиенту создается аккаунт в вашей системе

4. Показали страницу на которой клиент настраивает базовые настройки бронирования. 
Чтобы управлять более сложными настройками, нужно перейти в вашу админку.


### Бронирование

1. Гость заведения в бронирует столик через приложение или другим способом

2. Вы отправляете бронь в Poster. Обязательные параметры: 
 - номер телефона
 - имя гостя
 - время когда гость придет
 - сколько времени гость будет в заведении



## Какие методы API использовать

1. Чтобы отобразить ваш интерфейс в админ-панели Poster используйте [Manage Platform](/docs/v3/manage/index). 
Этот же метод вернет вам всю информацию по клиенту: токен для запросов к API, контакты владельца

2. Получайте все заведения в аккаунте методом [access.getSpots](/docs/v3/web/access/getSpots)

3. Создавайте брони методом [incomingOrders.createReservation](/docs/v3/web/incomingOrders/createReservation)


☝️ Сейчас API Poster не позволяет отменять брони. В будущем мы добавим метод API для отмены, но пока интеграции делаются без отмены брони. 