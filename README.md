# Demo 3Scale as API user

## Register account on developer portal
Register your email at developer portal https://anugraha.3scale.net - Sign in - Sign up
All entries must be filled.

Review API documentation at DOCUMENTATION tab.

## Register for Finto API plan
Register Finto API
- APPLICATIONS -> Create new applications -> select finto
- Plan: basic
- Name: finto-client
- Description: finto-client
- Create Application

Note down your unique user key (eg. bb629d06ad6bf40c736a735a315836cba).

## Try out calling allowed API using your key
Go to DOCUMENTATION tab
- GET /vocabularies
- LANG: en
- USER_KEY: #user-key
- Try it out!
  
You should be able to see response.

## Try out calling protected API using your key
Go to DOCUMENTATION tab
- GET /types
- LANG: en
- USER_KEY: #user-key
- Try it out!
  
You should see Limit exceeded response.

## Upgrade plan to premium
Go to APPLICATIONS tab
- finto-client
- basic > review/changes
- Review your existing basic plan
  - GET_vocabularies 60 hit / minute
- Select premium plan
  - GET_vocabularies 6000 hit / minute
  - GET_types 6000 hit / minute
- Request Plan Change
  
You will need approval from admin.

## Try out calling protected API after plan upgraded to premium
After upgrade request is approved, try to call GET /types API again. You should be able to get correct response.

## Review your usage statistic
Go to STATISTICS tab. You should be able to see your usage statistic.
