**Эндпоинт для работы с Организациями, Мероприятиями и членством в них**
<br>
<br>1) **create Organization or Event**
<br>POST /api/community.create
<br>**_parameters in request body:_**
<br>name >>> string
<br>type >>> requirements="org|event"
<br>**_return_**
<br>Object (Organization or Event)
<br>
<br>2) **edit Organization or Event**
<br>PUT /api/communities/{id}
<br>id >>> id of Event or Organization object
<br>**_parameters in request body:_**
<br>{"community_form":{}}
<br>
<br>3) **Get Organization or Event**
<br>GET /api/community.get
<br>**_parameters in request URL:_**
<br>id >>> id of Event or Organization object
<br>type >>> requirements="org|event"
<br>
<br>4) **Get User Organizations or Get User Events**
<br>GET /api/community.getUserCommunities
<br>**_parameters in request URL:_**
<br>user_id >>> requirements="\d+"
<br>type >>> requirements="org|event"
<br>filter >>> nullable=true, requirements="owner"
<br>**_parameters in request body:_**
<br>page >>> requirements="\d+"
<br>
<br>5) **Join Organization by User or Join Event By User**
<br>POST /api/community.join
<br>**_parameters in request body:_**
<br>community_id >>> requirements="\d+"
<br>
<br>6) **Join Event By Organization**
<br>POST /api/community.joinEventByOrganization
<br>**_parameters in request body:_**
<br>event_id >>> requirements="\d+"
<br>organization_id >>> requirements="\d+"
<br>
<br>7) **Leave Organization by User or Leave Event By User**
<br>DELETE /api/community.leave
<br>**_parameters in request URL:_**
<br>community_id >>> requirements="\d+"
<br>
<br>8) **Leave Event By Organization**
<br>DELETE /api/community.leaveEventByOrganization
<br>**_parameters in request body:_**
<br>event_id >>> requirements="\d+"
<br>organization_id >>> requirements="\d+"
<br>
<br>9) **Get Unconfirmed Members (Users)**
<br>GET /api/community.getUnconfirmed
<br>**_parameters in request URL:_**
<br>id >>> id of Event or Organization object, requirements="\d+"
<br>**return**
<br>array(
<br>'members' => Collection of Users,
<br>'organization_members' => Collection of Organizations
<br>)
<br>
<br>10) **Approve User Membership**
<br>PUT /api/community.approve
<br>**_parameters in request body:_**
<br>org_id >>> requirements="\d+"
<br>member_id >>> requirements="\d+"
<br>
<br>11) **Approve Organization Membership**
<br>PUT /api/community.approveOrganization
<br>**_parameters in request body:_**
<br>event_id" >>> requirements="\d+"
<br>organization_id >>> requirements="\d+"
<br>
<br>12) **Reject User Membership**
<br>DELETE /api/community.reject
<br>**_parameters in request body:_**
<br>org_id >>> requirements="\d+"
<br>member_id >>> requirements="\d+"
<br>
<br>13) **Reject Organization Membership**
<br>DELETE /api/community.rejectOrganizationMembership
<br>**_parameters in request body:_**
<br>event_id >>> requirements="\d+"
<br>organization_id >>> requirements="\d+"
<br>
<br>14)  **delete Organization or Event**
<br>DELETE /api/community.delete
<br>**_parameters in request URL:_**
<br>id >>> requirements="\d+"
<br>
<br>15) **get Organization or Event Awards**
<br>GET /api/community.getAwards
<br>
<br>16) **get Expertise Profiles**
<br>GET /api/community.getExpertiseProfiles
<br>
<br>17) **get Expertise Types**
<br>GET /api/community.getExpertiseTypes
<br>
<br>18) **get Ownerships**
<br>GET /api/community.getOwnerships
<br>
<br>19) **get Organization Specializations**
<br>GET /api/community.getOrganizationSpecializations
<br>
<br>20) **get Expert Specializations**
<br>GET /api/community.getExpertSpecializations
<br>
<br>21) **get Organization Types**
<br>GET /api/community.getTypes
<br>
<br>21) **set Event is Ended**
<br>PUT /api/events/{id}
<br>**_parameters in request URL:_**
<br>isEnded >>> requirements="true|false"
<br>
<br>
<br>