# uuid

```dart
var uuid = const Uuid();
if (uuidType.contains("v1")) { //time-based
  controller.text = uuid.v1();
} else if (uuidType.contains("v4")) { //random
  controller.text = uuid.v4();
} else if (uuidType.contains("v5")) { //namespace-name-sha1-based
  controller.text = uuid.v5(Uuid.NAMESPACE_DNS, controller.text);
}
```
