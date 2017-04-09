# checkMyInventory
Check my Inventory 

## Setup 

Account linking, Login to the app using google OAuth. 

## How it works 
- Apps <> API <> [OAuth, Service, Db(user)]

- Google OAuth Documentation - https://developers.google.com/identity/protocols/OAuth2

- https://console.developers.google.com
    - Create Project 
        - Name Project
    - Gmail API
        - Enable
        - Credentials 
            - Create Credentials
                - OAuth client ID
                - Configure consent screen
                - Input info
                - Save
                - Web application
                - Fill urls from ADA after creating skill
                - Create
        - Save the Oauth key and secret
- Create AWS Lambda & ADA Skill
- Account Linking AWS
    - Authorization URL
        - https://accounts.google.com/o/oauth2/v2/auth?access_type=offline&response_type=code&approval_prompt=force
    - Client ID - from Google Oauth
    - Domains (optional)
    - Scope - Gmail API 
        - Refrence link - https://developers.google.com/gmail/api/v1/reference/users/drafts/list
        - Add Scopes 
            - https://mail.google.com/
            - https://www.googleapis.com/auth/gmail.modify
            - https://www.googleapis.com/auth/gmail.readonly
    - Google API Console    
        - Credentials
        - Skill
            - Input Redirect URL from AWS to Google API Console
    - Access Token URI 
        - https://www.googleapis.com/oauth2/v4/token
    - Client Secret
        - Input from Gmail OAuth
    - Save & Next
    