# TabBar & TabBarView

Controller

```dart
class _FavoriteState extends State<Favorite> with TickerProviderStateMixin
.
.
.
TabController? controller;
@override
void initState() {
  controller = TabController(length: allTags.length, vsync: this);
}
```

TabView

```dart
TabBar(
    controller: controller,
    isScrollable: true,
    tabs: [for (var i in allTags) Tab(text: i)],
    indicatorColor: Colors.white,
    indicatorPadding: EdgeInsets.symmetric(horizontal: 10),
),
```



TabBarView

```dart
TabBarView(controller: controller,children:[])
```
