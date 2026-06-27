# Rain Language Support (C) — VS Code Extension

Syntax highlighting and file icon support for the [Rain programming language](https://rain-docs.vercel.app/) — **C bytecode VM edition** — in Visual Studio Code.

Rain (C) programs live in `.rn` files and are run with the `rain` binary you build from [rainc](https://github.com/yugal109/rainc).

---

## Features

- **Syntax highlighting** for `.rn` files
  - Keywords: `var`, `fun`, `class`, `if`, `else`, `while`, `for`, `return`, `break`, `continue`, `print`, `printin`, `this`, `super`
  - Module imports with `benutzen` and `name::function()` call syntax
  - Array literals `#[...]` and method calls `->len()`, `->push()`, `->pop()`, etc.
  - String literals, numbers, booleans (`true` / `false`), `nil`
  - Line comments (`//`)
  - Function and class definitions, inheritance with `<`
  - Logical operators: `and`, `or`, `not`, `!`
- **Custom file icon** for `.rn` files in the Explorer
- **Language configuration** — bracket matching, comment toggling with `Cmd+/` / `Ctrl+/`, auto-indent inside `{}`

---

## Installation

### Option 1 — From VS Code Marketplace

1. Open VS Code
2. Press `Cmd+Shift+X` (macOS) or `Ctrl+Shift+X` (Windows/Linux) to open the Extensions panel
3. Search for **Rain Language (C)**
4. Click **Install**

### Option 2 — Local install from VSIX

1. Download `rainlang-0.0.1.vsix` (or build it yourself — see below)
2. Run in your terminal:

```bash
code --install-extension rainlang-0.0.1.vsix
```

3. Fully quit and reopen VS Code (`Cmd+Q` on macOS, `Alt+F4` on Windows)

### Enable the file icon

After installing, activate the Rain file icon theme so `.rn` files show the custom icon in the Explorer:

1. Press `Cmd+Shift+P` (macOS) or `Ctrl+Shift+P` (Windows/Linux)
2. Type `File Icon Theme` and select it
3. Choose **Rain Icons (C)**

---

## Building the VSIX from source

Requires [Node.js](https://nodejs.org/) and the `vsce` packaging tool.

```bash
npm install -g @vscode/vsce
cd rainlang
vsce package
```

This produces `rainlang-0.0.1.vsix` in the same folder. Install it with:

```bash
code --install-extension rainlang-0.0.1.vsix
```

---

## Building the Rain interpreter

Rain (C) is a C bytecode VM. Build it from source:

```bash
git clone https://github.com/yugal109/rainc.git
cd rainc
make
```

On macOS you may need libcurl and sqlite3 first:

```bash
brew install curl sqlite
```

Run a Rain program:

```bash
./rain hello.rn
```

Start the REPL:

```bash
./rain
```

Clean and rebuild:

```bash
make clean && make
```

### Exit codes

| Code | Meaning |
|------|---------|
| `64` | Wrong CLI usage |
| `65` | Compile-time error |
| `70` | Runtime error |
| `74` | Could not read file |

---

## Language quick-reference

```rn
// variables
var name = "Rain";
var count = 0;

// print
print name;
print "value: " + count;

// if / else
if (count >= 10) {
  print "big";
} else {
  print "small";
}

// while
var i = 0;
while (i < 5) {
  print i;
  i = i + 1;
}

// for
for (var j = 0; j < 3; j = j + 1) {
  print j;
}

// arrays — literal uses #[...]
var nums = #[10, 20, 30];
print nums[0];
nums->push(40);
print nums->len();

// functions
fun add(a, b) {
  return a + b;
}
print add(3, 4);

// classes
class Dog {
  init(name) {
    this.name = name;
  }
  bark() {
    print this.name + " says: Woof!";
  }
}
Dog("Rex").bark();

// module imports
benutzen math;
print math::sqrt(16);
```

---

## Project structure

```
rainlang/
├─ images/
│  ├─ icon.png               # Extension icon (shown in Extensions panel)
│  └─ rain-icon.svg          # File icon (shown in Explorer sidebar)
├─ fileicons/
│  └─ rainc-icon-theme.json  # File icon theme definition
├─ syntaxes/
│  └─ rainc.tmLanguage.json  # TextMate grammar (syntax highlighting)
├─ language-configuration.json
├─ package.json
└─ README.md
```

---

## About Rain

Rain is a lightweight, dynamically typed scripting language with a clean C-family syntax. The C edition (`rainc`) is a bytecode VM written in C — fast to build and easy to embed.

Key characteristics:
- **Dynamically typed** — numbers, strings, booleans, `nil`, arrays
- **Array-first** — literal `#[...]` syntax with built-in methods (`->push`, `->pop`, `->sort`, `->slice`, etc.)
- **Modules** — load with `benutzen`, call as `module::function()`
- **OOP** — `class`, single inheritance with `<`, `this` / `super`
- **C-style loops** — `for (init; condition; increment)`

→ [Rain Documentation](https://rain-docs.vercel.app/docs)

→ [Rain C source (rainc)](https://github.com/yugal109/rainc)

---

## Publisher

**rain-lang** — made with ☔
