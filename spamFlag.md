**Система спам меток для Постов, Сообщений и Обьявлений**


1) Создание спам-метки
**POST /api/spamFlag.create**
_Принимает два параметра в теле запроса_
**_id_** Айдишник сущности для спам метки
**_type_** Тип сущности для спам метки, возможные значения: advert_spam_flag|post_spam_flag|message_spam_flag

2) Удалить спам метку по **ID** спам-метки
**DELETE /api/spamFlag.delete?id=:ID**


3) Получить спам-метку по **ID**
**GET /api/spamFlag.get?id=:ID**


4) Получить все спам метки текущего юзера 
**GET /api/spamFlag.getByCurrentUser**
