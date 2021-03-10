# fengari-lua: Dart bindings for fengari-web, a Lua 5.3 interpreter.

## Installation

1. Add the fengari_lua package to your pubspec:

```yaml
dependencies:
  fengari_lua: ^1.2.0
```

2. Add fengari-web.js to your html:

```html
<head>
    ...
    <script src="https://github.com/fengari-lua/fengari-web/releases/download/v0.1.4/fengari-web.js"></script>
</head>
```

## Usage

This library comes with bindings for most of the Lua API, see https://www.lua.org/manual/5.3/

It also includes a wrapper which greatly simplifies interaction with Lua states, Example:

```dart
import 'package:fengari_lua/lua.dart';
main() {
  var state = LuaState();
  state.loadString("""
    print("Hello, World!")
  """);
  state.call();
  state.close();
}
```

## Example

An example project can be found at https://github.com/PixelToast/dart-fengari-lua/tree/master/example/lua_repl, it
provides a simple web based REPL:

![Screenshot of REPL](https://raw.githubusercontent.com/PixelToast/dart-fengari-lua/master/example/lua_repl/screenshot.png)