# [FIXED] WhatsApp Cloud API Webserver

This is a template for generating Whatsapp bots which are immediately deployable to Heroku, powered by Meta's Whatsapp Cloud API

# Setup

### Deploy 

1. You can deploy this sample app on Heroku (for testing) by clicking here:

    
    [![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/NullCode1337/whatsapi-flask-webhook)


2. Add a name and region for this bot, then click Deploy App button.

    ![Preview](Images/Heroku1.png)


3. Wait for the build to finish

    ![Preview](Images/Heroku2.png)

4. When Heroku has successfully deployed your application, click on **Manage App**

    ![Preview](Images/Heroku3.png)

5. Go to the **Settings > Reveal Config Vars**, and add the following variables:
```text
TOKEN: <your temporary access token or permanent token from Meta Whatsapp dashboard>
PHONE: <your phone number ID from Meta Whatsapp Dashboard>
APP_SECRET: <any random string (no numbers) which you will also add to Meta Webhooks>
```
6. When you have finished, click **Open app**. You'll be sent to a website which says **"Hello, It Works"**

    ![Preview](Images/Heroku7.png)

    ![Preview](Images/Heroku8.png)

7. Now your callback URL will be `https://<app_name>.herokuapp.com/whatsapi`

    ![Preview](Images/Heroku9.png)

8. Open Meta Developers Whatsapp/Configuration panel and click **"Edit"** beside webhooks textbox

9. On the dialog box, for **Callback URL** enter `https://<app_name>.herokuapp.com/whatsapi`

10. For **Verify Token** enter the APP_SECRET you previously set on Heroku. Click Verify and Save.

![image](https://user-images.githubusercontent.com/70959549/190555985-55da4237-f932-4789-98a8-036a3aa650cf.png)

## References 
1. [WhatsApp Cloud API official documentation](https://developers.facebook.com/docs/whatsapp/cloud-api/)
2. [Heyoo WhatsApp API Python Wrapper](https://github.com/Neurotech-HQ/heyoo)
3. [Create a Facebook App ID App Secret](https://support.appmachine.com/support/solutions/articles/80000978442)

## Credits
1. [Jaxparrow](https://github.com/JAXPARROW/)      [Original Creator]
2. [NullCode1337](https://github.com/NullCode1337) [Revamped project]
