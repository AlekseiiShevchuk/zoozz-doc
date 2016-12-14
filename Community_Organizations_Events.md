**Эндпоинт для работы с Организациями, Мероприятиями и членством в них**

1) **create Organization or Event**<br>
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

5) **Join Organization by User or Join Event By User**
POST /api/community.join
**_parameters in request body:_**
community_id >>> requirements="\d+"

6) **Join Event By Organization**
POST /api/community.joinEventByOrganization
**_parameters in request body:_**
event_id >>> requirements="\d+"
organization_id >>> requirements="\d+"

7) **Leave Organization by User or Leave Event By User**
DELETE /api/community.leave
**_parameters in request URL:_**
community_id >>> requirements="\d+"

8) **Leave Event By Organization**
DELETE /api/community.leaveEventByOrganization
**_parameters in request body:_**
event_id >>> requirements="\d+"
organization_id >>> requirements="\d+"

9) **Get Unconfirmed Members (Users)**
GET /api/community.getUnconfirmed
**_parameters in request URL:_**
id >>> id of Event or Organization object, requirements="\d+"
**return**
array(
'members' => Collection of Users,
'organization_members' => Collection of Organizations
)

10) **Approve User Membership**
PUT /api/community.approve
**_parameters in request body:_**
org_id >>> requirements="\d+"
member_id >>> requirements="\d+"

11) **Approve Organization Membership**
PUT /api/community.approveOrganization
**_parameters in request body:_**
event_id" >>> requirements="\d+"
organization_id >>> requirements="\d+"

12) **Reject User Membership**
DELETE /api/community.reject
**_parameters in request body:_**
org_id >>> requirements="\d+"
member_id >>> requirements="\d+"

13) **Reject Organization Membership**
DELETE /api/community.rejectOrganizationMembership
**_parameters in request body:_**
event_id >>> requirements="\d+"
organization_id >>> requirements="\d+"

14)  **delete Organization or Event**
DELETE /api/community.delete
**_parameters in request URL:_**
id >>> requirements="\d+"

15) **get Organization or Event Awards**
GET /api/community.getAwards

16) **get Expertise Profiles**
GET /api/community.getExpertiseProfiles

17) **get Expertise Types**
GET /api/community.getExpertiseTypes

18) **get Ownerships**
GET /api/community.getOwnerships

19) **get Organization Specializations**
GET /api/community.getOrganizationSpecializations

20) **get Expert Specializations**
GET /api/community.getExpertSpecializations

21) **get Organization Types**
GET /api/community.getTypes

21) **set Event is Ended**
PUT /api/events/{id}
**_parameters in request URL:_**
isEnded >>> requirements="true|false"


