# svelte-bootstrap-icons

[![NPM][npm]][npm-url]
[![Build][build]][build-badge]

> [Bootstrap SVG icons](https://github.com/twbs/icons) as Svelte components.

<!-- REPO_URL -->

Try it in the [Svelte REPL](https://svelte.dev/repl/9a0e245df66248d59fadbbf007c06124).

---

<!-- TOC -->

## Install

```bash
yarn add -D svelte-bootstrap-icons
# OR
npm i -D svelte-bootstrap-icons
```

## Usage

Refer to [ICON_INDEX.md](./ICON_INDEX.md) for a full list of supported icons.

```svelte
<script>
  import {
    Alarm,
    CloudMoon,
    Github,
    PaintBucket,
    Wrench,
    ZoomOut,
  } from "svelte-bootstrap-icons";
</script>

<Alarm />
<CloudMoon />
<Github />
<PaintBucket />
<Wrench />
<ZoomOut />

```

### Direct import

Use the direct import for faster compiling during development.

**Note:** even if using direct imports, unused imports are still tree shakeable by application bundlers like Rollup or webpack.

```html
<script>
  import Alarm from "svelte-bootstrap-icons/lib/Alarm";
  // OR
  import Alarm from "svelte-bootstrap-icons/lib/Alarm/Alarm.svelte";
</script>
```

## API

`$$restProps` are forwarded to the `svg` element.

### Forwarded events

- on:click
- on:mouseover
- on:mouseenter
- on:mouseout
- on:keydown

## Usage with svelte:component

```svelte
<script>
  import * as icons from "svelte-bootstrap-icons";
</script>

{#each Object.keys(icons) as icon}
  <div>
    <svelte:component this={icons[icon]} title={icon} />
    {icon}
  </div>
{/each}

```

## TypeScript

Svelte version 3.31 or greater is required to use this library with TypeScript.

## Changelog

[Changelog](CHANGELOG.md)

## Contributing

See the [contributing guidelines](./CONTRIBUTING.md).

## License

[MIT](LICENSE)

[npm]: https://img.shields.io/npm/v/svelte-bootstrap-icons.svg?color=%237952b3&style=for-the-badge
[npm-url]: https://npmjs.com/package/svelte-bootstrap-icons
[build]: https://img.shields.io/travis/com/metonym/svelte-bootstrap-icons?color=24a148&style=for-the-badge
[build-badge]: https://travis-ci.com/metonym/svelte-bootstrap-icons
