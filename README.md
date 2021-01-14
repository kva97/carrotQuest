# flutter_carrotquest

A Carrot quest flutter plugin for Android and IOS.

## Implementation

### Android

```gradle
android {
    
    defaultConfig {
        ...
        minSdkVersion 21
        ...
    }
    ...
    packagingOptions {
        exclude 'META-INF/*.kotlin_module'
    }
    ...
}
```
### IOS

Nothing is required

## Getting Started

```dart
import 'package:flutter_carrotquest/flutter_carrotquest.dart';
```

```dart
await Carrot.setup(apiKey: 'your apiKey', appId: 'your appId')
        .catchError((onError) => print(onError));
```

```dart
await Carrot.setDebug()
        .catchError((onError) => print(onError));
```

```dart
await Carrot.auth(userId: 'your userId', userAuthKey: 'your userAuthKey')
        .catchError((onError) => print(onError));
```

```dart
await Carrot.deinit()
        .catchError((onError) => print(onError));
```

```dart
await Carrot.openChat();
```

## Features and bugs

Please file feature requests and bugs at the [issue tracker][tracker].

[tracker]: https://gitlab.com/dipdev.studio/open-source/flutter/flutter_carrotquest/-/issues
