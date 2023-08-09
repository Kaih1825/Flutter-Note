# OpenCotainer(Animate)

```dart
OpenContainer(
      //背景颜色
      closedColor: Colors.transparent,
      //阴影
      closedElevation: 0.0,
      //圆角
      closedShape: const RoundedRectangleBorder(
        borderRadius: BorderRadius.all(Radius.circular(10.0)),
      ),
      //显示的布局
      closedBuilder: (context, action) {
        return Container(
          color: Colors.grey,
          height: 120,
          margin: EdgeInsets.all(20),
        );
      },
      //过渡的方式
      transitionType: ContainerTransitionType.fade,
      //过渡的时间
      transitionDuration: const Duration(milliseconds: 3500),

      //即将打开的 Widget 的边框样式
      openShape: const RoundedRectangleBorder(
        borderRadius: BorderRadius.all(Radius.circular(1.0)),
      ),
      //即将打开的 Widget 的背景
      openColor: Colors.transparent,
      //阴影
      openElevation: 1.0,
      //布局
      openBuilder: (context, action) {
        return DetailsPage();
      },
      )
```
