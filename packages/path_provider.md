# Path Provider

```dart
var path=await getTemporaryDirectory();
```

<table><thead><tr><th width="227">Directory</th><th width="97" align="center">Android</th><th width="87" align="center">iOS</th><th width="92" align="center">Linux</th><th width="95" align="center">macOS</th><th align="center">Windows</th></tr></thead><tbody><tr><td>Temporary</td><td align="center">✔️</td><td align="center">✔️</td><td align="center">✔️</td><td align="center">✔️</td><td align="center">✔️</td></tr><tr><td>Application Support</td><td align="center">✔️</td><td align="center">✔️</td><td align="center">✔️</td><td align="center">✔️</td><td align="center">✔️</td></tr><tr><td>Application Library</td><td align="center">❌️</td><td align="center">✔️</td><td align="center">❌️</td><td align="center">✔️</td><td align="center">❌️</td></tr><tr><td>Application Documents</td><td align="center">✔️</td><td align="center">✔️</td><td align="center">✔️</td><td align="center">✔️</td><td align="center">✔️</td></tr><tr><td>Application Cache</td><td align="center">✔️</td><td align="center">✔️</td><td align="center">✔️</td><td align="center">✔️</td><td align="center">✔️</td></tr><tr><td>External Storage</td><td align="center">✔️</td><td align="center">❌</td><td align="center">❌</td><td align="center">❌️</td><td align="center">❌️</td></tr><tr><td>External Cache Directories</td><td align="center">✔️</td><td align="center">❌</td><td align="center">❌</td><td align="center">❌️</td><td align="center">❌️</td></tr><tr><td>External Storage Directories</td><td align="center">✔️</td><td align="center">❌</td><td align="center">❌</td><td align="center">❌️</td><td align="center">❌️</td></tr><tr><td>Downloads</td><td align="center">❌</td><td align="center">✔️</td><td align="center">✔️</td><td align="center">✔️</td><td align="center">✔️</td></tr></tbody></table>