user
====

create user
-----------
uri:
  POST v1.0/users/

params::

   {
      user: {
         id: user_id,
         password: pass,
         email: mail,
         phone: phone
      }
   }

returns::
   
   status: 201

   {
       "user": {
           "id": "u1000",
           "email": "jqsmith",
           "phone": "john.smith@example.org",
           "enabled": false
       }
   }

get user list
-------------
uri:
  GET v1.0/users/

params::

   None

returns::

   status: 200
   {
       "users": [
           {
               "id": "u1000",
               "name": "jqsmith",
               "email": "john.smith@example.org",
               "enabled": true
           },
           {
               "id": "u1001",
               "name": "jqsmith",
               "email": "john.smith@example.org",
               "enabled": true
           }
       ],
   }

get user detailed information
-----------------------------
uri:
  GET v1.0/users/{user_id}

params::

   None

returns::

   status: 200
   {
      user: {
         id: name,
         description: desc,
         address: addr,
         ...
      }
   }

modify user
-----------
uri:
  PUT v1.0/users/id

params::

   status: 200
   {
      user: {
         id: name,
         description: desc,
         address: addr,
         ...
      }
   }

return::

   {
      user: {
         id: name,
         description: desc,
         address: addr,
         ...,
         enabled
      }
   }

delete user
-----------

uri:
  DELETE v1.0/users/{user_id}

params::

   None

return::

   status: 204
   None

session
=======

create session
--------------

uri:
  POST v1.0/sessions/

params::

   {
      user: {
         id: user_id,
         password: pass
      }
   }

return::

   status: 201
   {
      session: {
         session_id: session_id,
         userid: userid,
      }
   }

get session
-----------

uri:
  GET v1.0/sessions/

params::

   status: 200
   {
      session: {
         session_id: session_id,
         userid: userid
      }
   }

return::

  None
  
delete session
--------------

uri:
  DELETE v1.0/sessions/session_id

params::

   None

return::

   status: 204
