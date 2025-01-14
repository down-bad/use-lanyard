# `use-lanyard`

### [View Demo](https://codesandbox.io/s/use-lanyard-demo-kokjd?file=/index.js)

React hook for [lanyard](https://github.com/Phineas/lanyard/), an easy way to track your Discord presence through REST or websockets.

It's easy to use and fully typed. It returns an [swr](https://github.com/vercel/swr) `responseInterface`, but if you don't know what that means, here's an example:

```tsx
import {useLanyard} from 'use-lanyard';

const DISCORD_ID = '268798547439255572';

export function Activity() {
	const {data: activity} = useLanyard(DISCORD_ID);

	return <>...</>;
}
```

### Socket

There is also a hook for using the websocket that Lanyard provides, here's an example:

```tsx
import {useLanyardWs} from 'use-lanyard';

const DISCORD_ID = '268798547439255572';

export function Activity() {
	const activity = useLanyardWs(DISCORD_ID);

	return <>...</>;
}
```

### Types

You can also import the named types as follows

```ts
import { Data, Activity, ...etc } from 'use-lanyard';
// See src/types.ts for all types
```

## Acknowledgements

- [Phineas Walton](https://github.com/Phineas/) – Author of lanyard
- [Alistair Smith](https://github.com/alii/) – Author of this library
