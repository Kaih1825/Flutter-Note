# Provider

{% code title="main.dart" %}
```dart
import 'package:flutter/material.dart';
import 'package:git/value.dart';
import 'package:provider/provider.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    // Add provider
    return MultiProvider(
      providers: [ChangeNotifierProvider.value(value: ValueClass())],
      //Provider.of(context) should not be used in the same class as MultiProvider
      child: const MaterialApp(home: Next()),
    );
  }
}

class Next extends StatefulWidget {
  const Next({Key? key}) : super(key: key);

  @override
  State<Next> createState() => _NextState();
}

class _NextState extends State<Next> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      floatingActionButton: FloatingActionButton(
        onPressed: () {
          //Increment counter value
          Provider.of<ValueClass>(context, listen: false).increment();
        },
        child: const Icon(Icons.add),
      ),
      //Get counter value
      body: Center(child: Text(Provider.of<ValueClass>(context).count.toString())),
    );
  }
}
```
{% endcode %}

{% code title="value.dart" %}
```dart
import 'package:flutter/material.dart';

class ValueClass with ChangeNotifier {
  // 設定一個整數私有變數 _count的欄位，初值為零
  int _count = 0;

  //可以透過 Consumer 來獲得當下 count 值
  int get count => _count;

  //當點擊右下角＋ 浮動按鈕，會呼叫此方法
  //此方法會將 _count 累加 1，並叫 notifyListeners
  increment() {
    _count++;
    notifyListeners();
  }
}
```
{% endcode %}

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p>Result</p></figcaption></figure>
