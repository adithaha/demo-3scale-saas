# Demo 3Scale as API user

## Register account on developer portal
Register your email at developer portal https://anugraha.3scale.net

Review API documentation at Documentation tab

## Register for Finto API plan
Register Finto API
- Applications -> Create new applications -> select finto
- Plan: basic
- Name: finto-client
- Description: finto-client
- Create Application

Note down your unique user key (eg. bb629d06ad6bf40c736a735a315836cba)

## Try out calling API using your key
Go to Documentation tab
- GET /vocabularies
- LANG: en
- USER_KEY: #user-key
- Try it out!
  
You should be able to see response

## Try out calling protected API using your key
Go to Documentation tab
- GET /types
- LANG: en
- USER_KEY: #user-key
- Try it out!
  
You should see Limit exceeded response

## Upgrade plan to premium
Go to Applications tab
- finto-client
- basic > review/changes
- Review your existing basic plan
  - GET_vocabularies 60 hit / minute
- Select premium plan
  - GET_vocabularies 6000 hit / minute
  - GET_types 6000 hit / minute
- Request Plan Change
  
You will need approval from admin

## Try out calling protected API after plan upgraded to premium
After upgrade request is approved, try to call GET /types API again. You should be able to get correct response.
