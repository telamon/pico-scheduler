[`pure | 📦`](https://github.com/telamon/create-pure)
[`code style | standard`](https://standardjs.com/)
# pico-scheduler

> Tiny O(1) discrete time scheduler

## Use

```bash
$ npm install pico-scheduler
```

Simple example using an arbitrary time-unit:

(Using `new Date().getTime()` is fine too)

```js
const Scheduler = require('pico-scheduler')

const s = new Scheduler()

s.enque(320, () => console.log('Future'))
s.enque(5, () => console.log('World'))
s.enque(14, () => console.log('says'))
s.enque(3, () => console.log('Hello'))

let time = 0
while (!s.empty) s.tick(time++)
console.log(`Ticked ${time} times`)
```

Produces:

```
> Hello
> World
> says
> Future
> 320
```

## Donations

```ad
 _____                      _   _           _
|  __ \   Help Wanted!     | | | |         | |
| |  | | ___  ___ ___ _ __ | |_| |     __ _| |__  ___   ___  ___
| |  | |/ _ \/ __/ _ \ '_ \| __| |    / _` | '_ \/ __| / __|/ _ \
| |__| |  __/ (_|  __/ | | | |_| |___| (_| | |_) \__ \_\__ \  __/
|_____/ \___|\___\___|_| |_|\__|______\__,_|_.__/|___(_)___/\___|

If you're reading this it means that the docs are missing or in a bad state.

Writing and maintaining friendly and useful documentation takes
effort and time. In order to do faster releases
I will from now on provide documentation relational to project activity.

  __How_to_Help____________________________________.
 |                                                 |
 |  - Open an issue if you have ANY questions! :)  |
 |  - Star this repo if you found it interesting   |
 |  - Fork off & help document <3                  |
 |.________________________________________________|

I publish all of my work as Libre software and will continue to do so,
drop me a penny at Patreon to help fund experiments like these.

Patreon: https://www.patreon.com/decentlabs
Discord: https://discord.gg/tJhmxqX
```


## Changelog

### 1.0.0 first release
- Extracted from [hyper-simulator](https://github.com/decentstack/hyper-simulator) codebase

## Contributing

By making a pull request, you agree to release your modifications under
the license stated in the next section.

Only changesets by human contributors will be accepted.

## License

[AGPL-3.0-or-later](./LICENSE)

2020 &#x1f12f; Tony Ivanov
