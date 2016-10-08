# 002_Tutorial_button_click_notification

## Purpose
Tutorial: show notification message upon button click

2016.10.02 by Szőke Sándor

Android Studio version: 2.2 (September 15, 2016)

## Steps needed
* create application
* drag button onto layout
* add code to: class MainActivity 

```java
    public void buttonOnClick(View v)
    {
        NotificationCompat.Builder mBuilder = new NotificationCompat.Builder(this);
        mBuilder.setSmallIcon(ic_dialog_info);
        mBuilder.setContentTitle("Notification Demo");
        mBuilder.setContentText("Demo notification upon button click!");

        // Sets an ID for the notification
        int mNotificationId = 001;
        // Gets an instance of the NotificationManager service
        NotificationManager mNotifyMgr =
                (NotificationManager) getSystemService(NOTIFICATION_SERVICE);
        // Builds the notification and issues it.
        mNotifyMgr.notify(mNotificationId, mBuilder.build());
    }
```
* attach code to button onClick: buttonOnClick
* place cursor after "(View v)" and press ALT+ENTER to extentend includes
* place cursor after "(Button)" and press ALT+ENTER to extentend includes
* place cursor after "NotificationCompat" and press ALT+ENTER to extentend includes, choose version v4 or v7 to import
* place cursor after "NotificationManager" and press ALT+ENTER to extentend includes, choose version v4 or v7 to import
* place cursor after "ic_dialog_info" and press ALT+ENTER to extentend includes
* exetute and click
