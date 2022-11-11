# [FIXED] WhatsApp Cloud API Webserver

This is a template for generating Whatsapp bots which are immediately deployable to Heroku, powered by Meta's Whatsapp Cloud API

# Setup

### Deploy 

1. You can deploy this sample app on Heroku (for testing) by clicking here:

    
    [![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/NullCode1337/PyWhatsapp)


2. Add a name and region for this bot, then click Deploy App button.

    ![Preview](Images/Heroku1.png)


3. Wait for the build to finish

    ![Preview](Images/Heroku2.png)

4. When Heroku has successfully deployed your application, click on **Manage App**

    ![Preview](Images/Heroku3.png)

5. Go to the **Settings > Reveal Config Vars**, and add the following variables:
```text
TOKEN: <your temporary access token or permanent token from Whatsapp/Getting Started>
PHONE: <your phone number ID from Whatsapp/Getting Started>
APP_SECRET: <any random string (no numbers) which you will also add to Meta Webhooks>
```
6. When you have finished, click **Open app**. You'll be sent to a website which says **"Hello, It Works"**

    ![Preview](Images/Heroku7.png)

    ![Preview](Images/Heroku8.png)

7. Now your callback URL will be `https://<app_name>.herokuapp.com/whatsapi`

    ![Preview](Images/Heroku9.png)

8. Open Meta Developers Whatsapp/Configuration panel and click **"Edit"** beside webhooks textbox

![image](https://user-images.githubusercontent.com/70959549/190577740-509bee34-9645-44b7-9042-1a3c12e875d5.png)
![image](https://user-images.githubusercontent.com/70959549/190577966-047e74bc-78c0-488f-b237-bb3ad0f66f9e.png)

9. On the dialog box, for **Callback URL** enter `https://<app_name>.herokuapp.com/whatsapi`

10. For **Verify Token** enter the APP_SECRET you previously set on Heroku. Click Verify and Save.

![image](https://user-images.githubusercontent.com/70959549/190578355-719246d5-e3d6-4f80-a422-3788cc418f72.png)

## References 
1. [WhatsApp Cloud API official documentation](https://developers.facebook.com/docs/whatsapp/cloud-api/)
2. [Heyoo WhatsApp API Python Wrapper](https://github.com/Neurotech-HQ/heyoo)
3. [Create a Facebook App ID App Secret](https://support.appmachine.com/support/solutions/articles/80000978442)

## Credits
1. [Jaxparrow](https://github.com/JAXPARROW/)      [Original Creator]
2. [NullCode1337](https://github.com/NullCode1337) [Revamped project]
