<p align="center">
    <img src="https://raw.githubusercontent.com/openpeep/watchout/main/.github/watchout-logo.png" width="170px"><br>
    š Fast, small, language agnostic <strong>File System Monitor for devs</strong><br>
    ā”ļø Just... yellin' for changes! (WIP)
</p>

## š Key Features
- [ ] Lightweight & Multi-threading
- [ ] **Watchout as Nimble** library for **Nim programming** š
- [ ] **Watchout as Binary** for CLI / language agnostic purposes š
- [ ] Yelling for `changes` and `deletions`
- [ ] `Clean` terminal on update
- [ ] Yelling for `files` and `directories`
- [ ] Sleep time in `ms`
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
from std/strutils import `%`

proc yelling() =
    proc watchoutCallback(file: FileObject) {.gcsafe, closure.} =
        echo "\nāØ Watchout is yelling for changes..."
        echo "\"$1\" has been updated" % [file.getName()]
    
    var monitor = Watchout.init(cleanOutput = false)
    monitor.addFile("sample.txt", watchoutCallback)
    monitor.start(ms = 400)

when isMainModule:
    yelling()
```

## Roadmap
_to add roadmap_

### ā¤ Contributions
If you like this project you can contribute to Watchout by opening new issues, fixing bugs, contribute with code, ideas and you can even [donate via PayPal address](https://www.paypal.com/donate/?hosted_button_id=RJK3ZTDWPL55C) š„°

### š Discover Nim language
<strong>What's Nim?</strong> Nim is a statically typed compiled systems programming language. It combines successful concepts from mature languages like Python, Ada and Modula. [Find out more about Nim language](https://nim-lang.org/)

<strong>Why Nim?</strong> Performance, fast compilation and C-like freedom. We want to keep code clean, readable, concise, and close to our intention. Also a very good language to learn in 2022.

### š© License
Watchout is an Open Source Software released under `MIT` license. [Developed by Humans from OpenPeep](https://github.com/openpeep).<br>
Copyright &copy; 2022 OpenPeep & Contributors &mdash; All rights reserved.
