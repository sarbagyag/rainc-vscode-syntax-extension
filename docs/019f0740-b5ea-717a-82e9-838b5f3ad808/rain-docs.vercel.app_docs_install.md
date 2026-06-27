---
url: "https://rain-docs.vercel.app/docs/install"
title: "Build & CLI · Rain docs · Rain"
---

Rain is a C bytecode VM. Clone the repo, run `make`, and use the `./rain` binary in the project root.

On macOS you may need libcurl and sqlite3 (e.g. `brew install curl sqlite` or MacPorts under `/opt/local`).

## Clone and build

Clone and build

```
git clone https://github.com/yugal109/rainc.git
cd rainc
make
./rain hello.rn
```

## REPL

REPL

```
./rain
```

## Clean rebuild

Clean rebuild

```
make clean && make
```

## Exit codes

| Symbol | Description |
| --- | --- |
| `64` | Wrong CLI usage |
| `65` | Compile-time error |
| `70` | Runtime error |
| `74` | Could not read file |