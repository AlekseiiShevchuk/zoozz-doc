**Эндпоинт для работы с Организациями, Мероприятиями и членством в них**

1) **create Organization or Event**
POST /api/community.create
**_parameters in request body:_**
name >>> string
type >>> requirements="org|event"
**_return_**
Object (Organization or Event)

2) **edit Organization or Event**
PUT /api/communities/{id}
id >>> id of Event or Organization object
**_parameters in request body:_**
{"community_form":{}}

3) **Get Organization or Event**
GET /api/community.get
**_parameters in request URL:_**
id >>> id of Event or Organization object
type >>> requirements="org|event"

4) **Get User Organizations or Get User Events**
GET /api/community.getUserCommunities
**_parameters in request URL:_**
user_id >>> requirements="\d+"
type >>> requirements="org|event"
filter >>> nullable=true, requirements="owner"
**_parameters in request body:_**
page >>> requirements="\d+"