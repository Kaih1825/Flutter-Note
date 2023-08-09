# SliverAppBar

<figure><img src="https://i.ytimg.com/vi/tAu333sf8L0/maxresdefault.jpg" alt=""><figcaption></figcaption></figure>

```dart
 DefaultTabController(
  length: 3,
  child: Scaffold(
    body: NestedScrollView(
      body: const TabBarView(
        children: [
          Text("ss1"),
          Text("ss2"),
          Text("ss3"),
        ],
      ),
      headerSliverBuilder: (BuildContext context, bool innerBoxIsScrolled) {
        return [
          SliverAppBar(
            expandedHeight: 300,
            collapsedHeight: 100,
            leading: Container(),
            flexibleSpace: const Align(
              alignment: Alignment.bottomCenter,
              child: TabBar(
                tabs: [
                  Tab(
                    child: Text("H1"),
                  ),
                  Tab(
                    child: Text("H2"),
                  ),
                  Tab(
                    child: Text("H3"),
                  ),
                ],
              ),
            ),
            pinned: true,
          )
        ];
      },
    ),
  ),
);
```
