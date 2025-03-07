# Vec.js

![version](https://img.shields.io/npm/v/@leodeslf/vec.js?color=3af) ![license](https://img.shields.io/npm/l/@leodeslf/vec.js?color=3af)

```txt

            .                 .
    <--------\               /-------->
      <-------\.           ./------->
        <------\\         //------>
          <-----\\.     .//----->
            <----\\\   ///---->
              <---\\\ ///--->
                <--\\Y//-->
                  <-\|/->
                     V

```

## Table of contents

* [About](#about)
* [Installation](#installation)
* [CDNs](#cdns)
* [Usage](#usage)
  * [Properties](#properties)
    * [Shortcuts](#shortcuts)
    * [Alias](#alias)
  * [Linear Algebra](#linear-algebra)
  * [Copying & Creating](#copying--creating)
  * [Boolean Conditions](#boolean-conditions)
  * [Magnitude Manipulation](#magnitude-manipulation)
  * [Miscellaneous](#miscellaneous)
* [Author](#author)
* [License](#license)

## About

>JavaScript vector library.

A set of classes that provide functionality related to basic **linear-algebra**, **geometry**, and more, for **2, 3, and 4-dimensional vectors**.

## Installation

```bash
npm i @leodeslf/vec.js
```

```bash
pnpm i @leodeslf/vec.js
```

```bash
yarn add @leodeslf/vec.js
```

```bash
bun i @leodeslf/vec.js
```

## CDNs

```bash
https://unpkg.com/@leodeslf/vec.js
```

```bash
https://cdn.jsdelivr.net/npm/@leodeslf/vec.js
```

## Usage

Most methods are available as both *instance* and `static` members. The ones that modify the current vector return `this`, thus we can *chain method calls*. Other than e.g.: `vector.x`, `vector.y`, and `vector.xy` (as an array), vectors are iterable, so it's possible to iterate trough their components using `for-of` or spread operator (e.g.: `...vector`).

```javascript
// E.g.:
import { Vec2 } from '@leodeslf/vec.js';

const position = new Vec2(1, 1.8);
const target = new Vec2(1, 10);
const distance = position.distance(target); // 8.2
const direction = Vec2.subtract(target, position).normalize(); // { x: 0, y: 1 }
```

### Properties

|Name|`Vec2`|`Vec3`|`Vec4`|
|:-|:-:|:-:|:-:|
|`angleW`|||✓\*|
|`angleX`|✓|✓\*|✓\*|
|`angleY`|✓|✓\*|✓\*|
|`angleZ`||✓\*|✓\*|
|`magnitude`|✓|✓|✓|
|`magnitudeSq`\*|✓|✓|✓|
|`w`|||✓|
|`x`|✓|✓|✓|
|`y`|✓|✓|✓|
|`z`||✓|✓|

*Property is `readonly`.

#### Shortcuts

To set/get components straight as/from arrays.

|Name|`Vec2`|`Vec3`|`Vec4`|
|:-|:-:|:-:|:-:|
|`xy`|✓|||
|`xyz`||✓||
|`xyzw`|||✓|

#### Alias

For 3D and 4D vector components and shortcuts.

|(Name) Alias|`Vec3`|`Vec4`|
|:-|:-:|:-:|
|(`w`) `a`||✓|
|(`x`) `r`|✓|✓|
|(`y`) `g`|✓|✓|
|(`z`) `b`|✓|✓|
|(`xyz`) `rgb`|✓||
|(`xyzw`) `rgba`||✓|

### Linear Algebra

|Name|`Vec2`|`Vec3`|`Vec4`|
|:-|:-:|:-:|:-:|
|`add`|✓|✓|✓|
|`angleBetween`|✓|✓|✓|
|`cross`||✓||
|`distance`|✓|✓|✓|
|`distanceChebyshev`\*|✓|✓|✓|
|`distanceManhattan`\*|✓|✓|✓|
|`distanceMinkowski`\*|✓|✓|✓|
|`distanceSq`|✓|✓|✓|
|`dot`|✓|✓|✓|
|`immutable`\*|✓|✓|✓|
|`lerp`\*|✓|✓|✓|
|`negate`|✓|✓|✓|
|`normalize`|✓|✓|✓|
|`project`|✓|✓|✓|
|`rotateX`||✓||
|`rotateY`||✓||
|`rotateZ`|✓|✓||
|`scale`|✓|✓|✓|
|`subtract`|✓|✓|✓|
|`zero`|✓|✓|✓|

*Static method only.

### Copying & Creating

|Name|`Vec2`|`Vec3`|`Vec4`|
|:-|:-:|:-:|:-:|
|`clone`|✓|✓|✓|
|`copy`|✓|✓|✓|
|`fromCylindricalCoords`\*||✓||
|`fromPolarCoords`\*|✓|||
|`fromSphericalCoords`\*||✓||
|`random`|✓|✓|✓|

*Static method only.

### Boolean Conditions

|Name|`Vec2`|`Vec3`|`Vec4`|
|:-|:-:|:-:|:-:|
|`satisfyEquality`|✓|✓|✓|
|`satisfyOpposition`|✓|✓|✓|
|`isInfinite`|✓|✓|✓|
|`isNaN`|✓|✓|✓|
|`isZero`|✓|✓|✓|

### Magnitude Manipulation

|Name|`Vec2`|`Vec3`|`Vec4`|
|:-|:-:|:-:|:-:|
|`limitMax`|✓|✓|✓|
|`limitMin`|✓|✓|✓|
|`clamp`|✓|✓|✓|

### Miscellaneous

|Name|`Vec2`|`Vec3`|`Vec4`|
|:-|:-:|:-:|:-:|
|`lookAt`|✓|✓|✓|
|`turnLeft`|✓|||
|`turnRight`|✓|||

## Author

Copyright (c) [Leonardo de S. Leal F.](https://github.com/leodeslf "GitHub profile"), 2018-present.

## License

MIT License.
