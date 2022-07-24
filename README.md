# Notifications-Android-13 (API level 33) [![GitHub license](https://img.shields.io/badge/forks-repo%20found-brightgreen)](https://github.com/HerikaSethi/Notifications-Android13.git)

A demo project in kotlin which shows the implementation of runtime permission notifications in Android-13(Api level 33).
Android 13 (API level 33) introduces a new runtime permission for sending non-exempt notifications from an app: POST_NOTIFICATIONS.

How Runtime permissions for Notification in Android 13 differ from Android 12 or lower versions?
In Android 12 or lower versions as soon as the app is launched, the user starts getting notifications but with Android 13, google will introduce runtime notification 
permissions which will display a dialgoue box to the user as soon as the user launches the app asking for permission to either allow notification or don't allow. If user closes the dialogue box without giving any permissions, then temporary permissions will be provided automatically.

Now since each foreground service needs to come with a notification, so now if you want to ,launch a foreground service in android, then, 
1. Create the service itself.
2. Create a notification channel and configure it.
3. Properly handle runtime permissions for showing notification keeping the following cases in mind:
          - What if user declines the permission.
          - what if user permanently declines it then we need to show some other kind of dialogue.
          
<h2>App capabilities depend on user choice in permissions dialog</h2>

In this dialog, users have the following actions available to them:



- Select allow
- Select don't allow
- Swipe away from the dialog, without pressing either button


## The following sections describe how your app behaves, based on which action the user takes.

<img width="434" alt="image" src="https://user-images.githubusercontent.com/43989738/180645011-d237ee3f-f0a9-4d3f-aa93-22b1a43ae77e.png">


- User selects **"Allow"**
If the user selects the allow option, your app can do the following:

Send notifications. All notification channels are allowed.
Post notifications related to foreground services. These notifications appear in the notification drawer.

- User selects **"Don't allow"**
If the user selects the don't allow option, your app can't send notifications. All notification channels are blocked, except for a few specific roles. This is similar to the behavior that occurs when the user manually turns off all notifications for your app in system settings.

*If your app targets 12L (or lower) and the user taps Don't allow, even just once, they aren't prompted again until one of the following occurs:*

         - The user uninstalls and reinstalls your app.
         - You update your app to target Android 13.*

- User **swipes away** from dialog
If the user swipes away from the dialog—that is, they don't select either allow or don't allow—the state of the notification permission doesn't change.

## Preview of demo app <img width="35" height="20" alt="image" src="https://user-images.githubusercontent.com/43989738/180645760-65474079-7a94-4c5c-8b2c-1145d75356df.png">

img width="50" height="80" alt="image" src="https://user-images.githubusercontent.com/43989738/180645893-d84976b2-21e3-43fc-8979-1dca01958e09.png">




We will need to request these permissions for all apps that target android 13


Steps to follow 
1. 


