Wechat Connector Demo Application
===================================

Description:
Based on the user URL input this demo application performs the following -

* /msg - URL verify and follower send message.
* /followerList - Get list of followers.
* /broadcast - Send Wechat openIdListBroadcastText to list of follower.
* /file - Upload image.
* /profile - Get follower profile.
* /remark - Change follower remark.


To be able to successfully run this application, this config values must be set in /src/main/app/mule-app.properties:
    -AppID: The unique certificate of wechat official account
    -AppSecret: The key of wechat official account's certificate
    -Token: Token set by the developer on the WeChat Official Account Admin Platform

Usage:
If AppID and AppSecret is valid. By default, once mule is up and running, Wecaht connector will use AppID and AppSecret to retrieve a access token from Wechat. And Wechat connector will automatically refresh the access token for you every 110 minutes.

* Example:org.mule.api.processor.LoggerMessageProcessor:Aq7uRMiulTly...

And then you can call http://localhost:8081/followerList for the app to return list of followers.

* Example:org.mule.api.processor.LoggerMessageProcessor:{total=994...