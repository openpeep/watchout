<p align="center">
    <img src="https://raw.githubusercontent.com/openpeep/watchout/main/.github/watchout-logo.png" width="170px"><br>
    🐶 A super small, language agnostic File System Monitor for development purposes
</p>

## 😍 Key Features
- [x] Open Source | `MIT` license

## Installing
```
nimble install watchout
```

## Examples

Quick example using Watchout as a standalone binary app
_todo_

In Nim language

```nim
import watchout
from std/os import execShellCmd

proc watchoutCallback(file: File) {.gcsafe, closure.} =
    discard execShellCmd("clear")                           # TODO Watchout for "cleanScreen"
    echo "✨ Watchout is yelling for changes..."
    echo "\"$1\" has been updated" % [file.getName()]

when isMainModule:
    var watch = Watchout.init(cleanScreen = true)
    watch.addFile("sample.txt", watchoutCallback)
    watch.start(400)
```

## Roadmap
_to add roadmap_

### ❤ Contributions
If you like this project you can contribute to Watchout by opening new issues, fixing bugs, contribute with code, ideas and you can even [donate via PayPal address](https://www.paypal.com/donate/?hosted_button_id=RJK3ZTDWPL55C) 🥰

### 👑 Discover Nim language
<strong>What's Nim?</strong> Nim is a statically typed compiled systems programming language. It combines successful concepts from mature languages like Python, Ada and Modula. [Find out more about Nim language](https://nim-lang.org/)

<strong>Why Nim?</strong> Performance, fast compilation and C-like freedom. We want to keep code clean, readable, concise, and close to our intention. Also a very good language to learn in 2022.

### 🎩 License
Watchout is an Open Source Software released under `MIT` license. [Developed by Humans from OpenPeep](https://github.com/openpeep).<br>
Copyright &copy; 2022 OpenPeep & Contributors &mdash; All rights reserved.
