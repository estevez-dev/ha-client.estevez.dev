# [Help pages](/help) - Connection

- [Quick start](#quick-start)
- [Advanced](#advanced)
  - [SSL Certificates](#ssl-certificates)
  - [Login with long-lived token](#login-with-long-lived-token)

If this documentation was not useful enough for you, feel free to ask any question in [HA Client on Descord](https://discord.gg/u9vq7QE)

{% include in_post.html %}

## Quick start
When first launching the app you will be presented with Quick start screen asking you to provide your Home Assistant url and [device name](/help/mobile_app_integration#device-name) for [Mobile App integration](/help/mobile_app_integration).

![image](/help/images/connection010.png)

You can just copy your Home Assistant url from browser and use it in the app:

![image](/help/images/connection011.png)

The easy and secure way to aceess you Home Assistant from anywhere (not only from your local network at home) is [Remote UI](https://www.nabucasa.com/config/remote/). If you alredy had it set up, just open your Home Assistant UI in browser, go to **Configuration** - **Home Assistant Cloud**, find **Remote Control** section and copy the url from **Your instance is available at**.

![image](/help/images/connection001.png)

![image](/help/images/connection002.png)

Now you need to login. And this process will be almost automatic thanks to [Home Assistant Authentication API](https://developers.home-assistant.io/docs/en/auth_api.html). You'll see a login form loaded directly from your Home Assistant instance:

![image](/help/images/connection006.png)

That's it! You are ready to go.

[Back to top](#help-pages---connection)

{% include in_post.html %}

## Advanced
### SSL Certificates
The main requirement is that your SSL Certificate should not be self-signed. Most certificates from providers like Let’s Encrypt will work. There is [known issue](https://github.com/estevez-dev/ha_client_pub/issues/24) with RapidSSL certificate, but this problem is common not only for HA Client.

Using of self-signed certificate is not possible for now and this is a restriction of Flutter’s WebSocket implementation.

[Back to top](#help-pages---connection)

### Login with long-lived token
It is possible to generate long-lived token manually and set the app to use it instead of logging in with a simple OAuth way.
To make HA Client use your generated long-lived token you need:
1. Go to your Home Assistant web interface and open your profile settings (just click on your user picture in the bottom part of main menu)

  ![image](/help/images/connection007.png)
 
2. Scroll down to **Long-lived access tokens** section and click **Create token**

  ![image](/help/images/connection008.png)

3. Give it a name `HA Client` as it will be used only for HA Client app (it is recommended to use different access tokens for different apps and services)
4. Click **Ok** and copy newly generated access token somewhere in a safe place or directly to **HA Client**:
  
  ![image](/help/images/connection009.png)

  ![image](/help/images/connection012.png)

[Back to top](#help-pages---connection)



### [What you need](/help/what_you_need) < Previous | Next > [User Interface](/help/user_interface)
