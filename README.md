# @zitterorg/mollitia-laborum-nesciunt
---

[![Build Status](https://travis-ci.org/aligay/@zitterorg/mollitia-laborum-nesciunt.svg?branch=master)](https://travis-ci.org/aligay/@zitterorg/mollitia-laborum-nesciunt/branches)
[![codecov](https://codecov.io/gh/aligay/@zitterorg/mollitia-laborum-nesciunt/branch/master/graph/badge.svg)](https://codecov.io/gh/aligay/@zitterorg/mollitia-laborum-nesciunt)
[![dependencies Status](https://david-dm.org/aligay/@zitterorg/mollitia-laborum-nesciunt/status.svg)](https://david-dm.org/aligay/@zitterorg/mollitia-laborum-nesciunt)
[![devDependencies Status](https://david-dm.org/aligay/@zitterorg/mollitia-laborum-nesciunt/dev-status.svg)](https://david-dm.org/aligay/@zitterorg/mollitia-laborum-nesciunt?type=dev)

## install
```
npm install @zitterorg/mollitia-laborum-nesciunt
```
## use
```
import safeTrim from '@zitterorg/mollitia-laborum-nesciunt'
safeTrim('    a      b  ')
```

## remove Invisible spaces

```
let str = '  "a":1    a \r\n\r\t  ᠎             　b       '
let ret = safeTrim(str)
expect(ret).toEqual('"a":1    a\n\nb')
```

## convert CR CR-LR into LR
```
a\r\n\r\nb  => 'a\n\nb'
a\r\rb => 'a\n\nb'
a\r\r\nb => 'a\n\nb'
```

## remove BOM
```
JSON.parse('﻿{"a":1}') // ❗️Error because BOM

JSON.parse(safeTrim('﻿{"a":1}')) // ✅
```


## more feature
[more feature](spec/test_spec.js)
