
## 0.9.0

### alpha.3 [WIP]

- [enhancement] make `.chain()` compatible with Fantasy Land
- [enhancement] make `.map()` compatible with Fantasy Land
- [enhancement] make `.equals()` compatible with Fantasy Land
- [enhancement] add lowercase factory functions to satisfy linters -- thanks to @LukaszTheProgrammer ( #107 )
  - `Maybe.some(val)` and `Maybe.none()`
  - `Either.right(val)` and `Either.left(err)`
- [enhancement] make `.ap()` compatible with Fantasy Land and Ramda -- thanks to @char0n ( #112 )
- [new] add `.ap()` to Identity (so it's copmpatible with FantasyLand) -- thanks to @char0n ( #121 )
- [new] add `.orNoneIf()` (alias `.orNothingIf()`) to Maybe -- thanks to @emmanueltouzery ( #100 )
- [new] add `.fromFalsy()` to Maybe static -- thanks to @kpudlik ( #98 )
- [new] add `.forEach()` to Identity, Maybe, Either, Validation, List and NEL -- thanks to @emmanueltouzery ( #95 ). And:
  - `.orElseRun()` to Maybe
  - `.forEachLeft()` to Either
  - `.forEachFail()` to Validation
- [new] add `.contains()` to Identity, Maybe, Either, Validation, List and NEL -- thanks to @emmanueltouzery ( #93 )
- [new] add `.find()` to List and NEL -- thanks to @emmanueltouzery ( #90 )
- [new] add `.fold()` as alias for `.cata()` to Either and Validation -- thanks to @tbrisbane ( #82 )
- [new] add `.foldLeft()` and `.foldRight()` to Maybe, Either, Validation, List and NEL -- thanks to @tbrisbane ( #82 )
- [new] add `.orNull()` to Maybe -- thanks to @emmanueltouzery ( #86 )
- [fix] fix typings to work with `--noImplicitAny`
- [fix] fix typings to work with `--strictNullChecks` -- thanks to @emmanueltouzery ( #86 )
 
### alpha.2

- [fix] fix List's `.size()` ( #79 )
- [fix] fix List's `.map` ( #64 )

### alpha.1

- [fix] fix Free monad

### alpha.0

- [new] `.equals()` method added to most entities
- [breaking] all native prototype extentions extracted to `monet-pimp.js`
- [enhancement] typings compatible with TS2.x
- [fix] updated module pattern

## 0.8.10

- [fix] Fixed `bower.json` issues ( #51 )
- [fix] Fixed internal `curry` implementation ( #55 )

## 0.8.9

- [new] add TypeScript typings
- [new] add `.ap()` to List, Free and NonEmptyList -- thanks to @WojciechP ( #44 )
- [new] add `"use strict";` -- thanks to @krjackso ( #41 )


### Typings

TypeScript typings added to repository, so now anyone can:

``` typescript
import { Maybe } from 'monet';

export function getStoredData(key: string): Maybe<SomeData> {
  return Maybe.fromNull(localStorage)
    .flatMap(ls => Maybe.fromNull(ls.getItem(key)))
    .map(JSON.parse);
}
```

## 0.8.7

- [new] add `.cata(…)` to Maybe -- thanks to Crisson Jno-Charles @crisson 
