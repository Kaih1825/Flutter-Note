# UITest

{% code title="/integration_test/app_test.dart" %}
```dart
import 'package:d01/main.dart' as app;
import 'package:flutter/material.dart';
import 'package:flutter_test/flutter_test.dart';

void main(){
    group("Test Group", () {
          testWidgets("Test Description1", (tester) async {
            app.main();
            await tester.pumpAndSettle();
            //Test Code 1
          });
          testWidgets("Test Description2", (tester) async {
            app.main();
            await tester.pumpAndSettle();
            //Test Code 2
          });
    }
}
```
{% endcode %}

```dart
app.main(); //打開App
await tester.pump(); //調用一幀重整Widgets
await tester.pumpAndSettle(); //重複調用pump()直到所有Widgets更新完成
await tester.tap(finder); //點擊
await tester.drag(finder, const Offset(0, -100)); //往上滑100
expect(finder,findsOneWidget); //驗證有出現一個
expect(finder,findsNothing); //驗證沒有出現
expect(finder,findsWidgets); //驗證有出現
await Future.delayed(Duration(seconds: time)); //延遲Duration
```

```dart
Finder
find.text("Search Now"); //利用Text
find.textContaining("London"); //含有London的Text
find.byType(TextField); //利用Widget Type
find.byKey(const Key("Search Button")); //利用Key
find.byIcon(Icons.add); //利用Icon

finder.first; //第一個Widget
finder.at(index); //第index個Widget
finder.last; //最後一個Widget
```

```dart
//滑動ListView直到"London"出現後再滑下去一點
while (true) {
  await tester.drag(find.byType(ListView), const Offset(0, -50));
  await tester.pump();
  try {
    expect(find.textContaining("London"), findsOneWidget);
    await tester.drag(find.byType(ListView), const Offset(0, -100));
    await tester.pumpAndSettle();
    break;
  } catch (ex) {}
}
```
