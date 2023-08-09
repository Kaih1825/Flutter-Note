# FlutterLocalNotifications

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

```dart
await FlutterLocalNotificationsPlugin().show(
    0,
    title,
    body,
    NotificationDetails(
      android: AndroidNotificationDetails(
        'worldskills',
        DateTime.now().toString().split('.')[0],
        channelDescription: "sss",
        importance: Importance.max,
        ticker: 'ticker',
      ),
    ),
    payload: "0");
```
