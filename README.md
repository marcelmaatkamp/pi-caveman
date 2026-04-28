# Pi Caveman

**Inspired by [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman)**

Makes the Pi coding agent speak like a caveman — cutting **~75% of output tokens** while keeping full technical accuracy.

## Quick Start

### Install via pi

```bash
$ pi install git:github.com/v2nic/pi-caveman
```

### Manual Install

```bash
cp -r extensions/caveman ~/.pi/agent/extensions/
```

### Or use with `-e` flag (temporary)

```bash
pi -e ./extensions/caveman
```

## Features

- `/caveman` - Toggle caveman mode on/off
- `/caveman lite` - Drop filler, keep grammar (professional)
- `/caveman full` - Default caveman mode (drop articles, fragments)
- `/caveman ultra` - Maximum compression, telegraphic

Auto-triggers on explicit token-saving requests: "caveman mode", "talk like caveman", "less tokens", "fewer tokens"

## What It Does

| Thing | Caveman Do? |
|-------|------------|
| English explanation | 🪨 Caveman smash filler words |
| Code blocks | ✍️ Write normal (caveman not stupid) |
| Technical terms | 🧠 Keep exact (polymorphism stay polymorphism) |
| Error messages | 📋 Quote exact |
| Articles (a, an, the) | 💀 Gone |
| Pleasantries | 💀 "Sure I'd be happy to" is dead |
| Hedging | 💀 "It might be worth considering" extinct |
| Git commits / PRs / docs / legal-security output | Normal unless explicitly requested |

## Benchmarks

From the original caveman project:

| Task | Normal (tokens) | Caveman (tokens) | Saved |
|------|---------------:|----------------:|------:|
| Explain React re-render bug | 1180 | 159 | 87% |
| Fix auth middleware token expiry | 704 | 121 | 83% |
| Set up PostgreSQL connection pool | 2347 | 380 | 84% |
| Explain git rebase vs merge | 702 | 292 | 58% |
| Debug PostgreSQL race condition | 1200 | 232 | 81% |
| **Average** | **1214** | **294** | **65%** |

## Example

**Normal:**
> "The reason your React component is re-rendering is likely because you're creating a new object reference on each render cycle. When you pass an inline object as a prop, React's shallow comparison sees it as a different object every time, which triggers a re-render. I'd recommend using useMemo to memoize the object."

**Caveman:**
> "New object ref each render. Inline object prop = new ref = re-render. Wrap in `useMemo`."

**Same answer. 75% less words.**

## Files

```
extensions/caveman/  - Pi extension
skills/caveman/      - Skill version
```

## Also See

- [Original caveman repository](https://github.com/JuliusBrussee/caveman)

## License

MIT
