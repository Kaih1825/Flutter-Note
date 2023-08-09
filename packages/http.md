# http

## Post

```dart
import 'package:http/http.dart' as http;

var url = Uri.https('example.com', 'whatsit/create');
var response = await http.post(url, body: {'name': 'doodle', 'color': 'blue'},headers: {'Content-Type': 'application/json'});
print('Response status: ${response.statusCode}');
print('Response body: ${response.body}');

print(await http.read(Uri.https('example.com', 'foobar.txt')));
```

## Delete

```dart
import 'package:http/http.dart' as http;

void api() async{
  var url= Uri.http("jsonplaceholder.typicode.com","/posts/1");
  getRes=await http.delete(url);
  print(getRes.body);
}
```
