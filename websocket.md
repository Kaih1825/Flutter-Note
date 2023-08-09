# WebSocket

<pre class="language-dart"><code class="lang-dart"><strong>import 'dart:io';
</strong><strong>
</strong><strong>WebSocket? websocket = await WebSocket.connect("ws://10.0.2.2:8080/");
</strong>websocket!.listen((event) {
  messages.add(jsonDecode(Utf8Decoder().convert(event))); //Get from websocket
  setState(() {});
});
websocket!.add(json); //Add to websocket
</code></pre>

```dart
import 'package:web_socket_channel/web_socket_channel.dart';

final channel = WebSocketChannel.connect(Uri.parse("ws://10.0.2.2:8080/"));

channel.stream.listen((snapshot) {
      messages.add(jsonDecode(Utf8Decoder().convert(snapshot))); //Get from websocket
      setState(() {});
});
channel.sink.add(json); //Add to websocket
```
