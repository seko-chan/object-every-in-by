# Object Every In By 🚀

![GitHub Release](https://img.shields.io/github/release/seko-chan/object-every-in-by.svg)
[![Visit Releases](https://img.shields.io/badge/Visit%20Releases-Click%20Here-blue)](https://github.com/seko-chan/object-every-in-by/releases)

Welcome to the **Object Every In By** repository! This project tests whether all properties of an object, both own and inherited, meet the criteria defined by a predicate function. It provides a simple and effective way to validate objects in JavaScript and Node.js applications.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API](#api)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

In JavaScript, objects are fundamental. They hold data and functionality. However, validating their properties can be tricky. This library simplifies that process. With **Object Every In By**, you can easily check if all properties in an object satisfy a given condition.

## Features

- **Simple Validation**: Quickly check if all properties pass a test.
- **Own and Inherited Properties**: Evaluate both types of properties.
- **Flexible Predicate Function**: Use any function that returns a boolean.
- **Lightweight**: Minimal footprint for your projects.
- **Node.js Compatible**: Works seamlessly in Node.js environments.

## Installation

To install the package, use npm:

```bash
npm install object-every-in-by
```

Alternatively, if you prefer yarn:

```bash
yarn add object-every-in-by
```

## Usage

To use **Object Every In By**, first, import the function into your project:

```javascript
const objectEveryInBy = require('object-every-in-by');
```

Next, create an object and a predicate function to test its properties.

## API

### `objectEveryInBy(obj, predicate)`

- **Parameters**:
  - `obj`: The object to validate.
  - `predicate`: A function that takes a property value and returns a boolean.

- **Returns**: `true` if all properties pass the test, otherwise `false`.

## Examples

### Basic Example

```javascript
const objectEveryInBy = require('object-every-in-by');

const testObject = {
  a: 1,
  b: 2,
  c: 3,
};

const isGreaterThanZero = value => value > 0;

const result = objectEveryInBy(testObject, isGreaterThanZero);
console.log(result); // true
```

### Example with Inherited Properties

```javascript
function Parent() {
  this.inheritedProperty = 10;
}

Parent.prototype.parentMethod = function() {
  return 'parent';
};

const child = Object.create(Parent.prototype);
child.ownProperty = 5;

const isNumber = value => typeof value === 'number';

const result = objectEveryInBy(child, isNumber);
console.log(result); // true
```

## Contributing

We welcome contributions! To contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch and create a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or suggestions, please reach out to the maintainer:

- **Name**: Seko Chan
- **Email**: seko.chan@example.com

Thank you for checking out **Object Every In By**! For more details, visit the [Releases section](https://github.com/seko-chan/object-every-in-by/releases). 

Let's make object validation easier together!