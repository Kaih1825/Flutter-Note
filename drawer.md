# Drawer

```dart
GlobalKey<ScaffoldState> key = GlobalKey(debugLabel: "Scaffold");
Scaffold(
      key: key,
)
key.currentState!.openDrawer();
key.currentState!.closeDrawer();
```
