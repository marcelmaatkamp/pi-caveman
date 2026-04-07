# Pi Caveman

**Inspired by [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman)**

Ultra-compressed communication mode for the [Pi coding agent](https://github.com/mariozechner/pi-coding-agent). Cuts ~75% of output tokens while keeping full technical accuracy.

## Quick Start

### Install via pi

```bash
$ pi install git:github.com/v2nic/pi-caveman
```

### Manual Install

```bash
# Install extension
cp -r extensions/caveman ~/.pi/agent/extensions/

# Or use with -e flag
pi -e ./extensions/caveman
```

## Usage

```
/caveman        # toggle on/off (default: full mode)
/caveman lite   # drop filler, keep grammar
/caveman full   # drop articles, fragments
/caveman ultra  # maximum compression
```

Auto-triggers on: "caveman mode", "talk like caveman", "less tokens", "be brief"

## Example

**Normal:**
> "The reason your React component is re-rendering is likely because you're creating a new object reference on each render cycle..."

**Caveman:**
> "New object ref each render. Inline object prop = new ref = re-render. Wrap in `useMemo`."

## Files

```
extensions/caveman/  - Pi extension
skills/caveman/      - Skill version
```

## License

MIT
