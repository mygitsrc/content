---
title: Array.prototype.join()
slug: Web/JavaScript/Reference/Global_Objects/Array/join
tags:
- Array
- JavaScript
- Method
- Prototype
- Reference
browser-compat: javascript.builtins.Array.join
---
{{JSRef}}

<span class="seoSummary"

> The <code><strong>join()</strong></code> method creates and returns a new
> string by concatenating all of the elements in an array (or an <a

    href="/en-US/docs/Web/JavaScript/Guide/Indexed_collections#Working_with_array-like_objects"
    >array-like object</a

> ), separated by commas or a specified separator string. If the array has only
> one item, then that item will be returned without using the separator.</span

{{EmbedInteractiveExample("pages/js/array-join.html")}}

## Syntax

```js
join()
join(separator)
```

### Parameters

- `separator` {{optional_inline}}
  - : Specifies a string to separate each pair of adjacent elements of the
    array. The separator is converted to a string if necessary. If omitted, the
    array elements are separated with a comma (","). If `separator` is an empty
    string, all elements are joined without any characters in between them.

### Return value

A string with all array elements joined. If <code><em>arr</em>.length</code> is
`0`, the empty string is returned.

## Description

The string conversions of all array elements are joined into one string.

> **Warning:** If an element is `undefined`, `null` or an empty array `[]`, it
> is converted to an empty string.

## Examples

### Joining an array four different ways

The following example creates an array, `a`, with three elements, then joins the
array four times: using the default separator, then a comma and a space, then a
plus and an empty string.

```js
var a = ['Wind', 'Water', 'Fire'];
a.join();      // 'Wind,Water,Fire'
a.join(', ');  // 'Wind, Water, Fire'
a.join(' + '); // 'Wind + Water + Fire'
a.join('');    // 'WindWaterFire'
```

### Joining an array-like object

The following example joins array-like object
([`arguments`](/en-US/docs/Web/JavaScript/Reference/Functions/arguments)), by
calling {{jsxref("Function.prototype.call")}} on
`Array.prototype.join`.

<pre class="brush: js">function f(a, b, c) {
  var s = Array.prototype.join.call(arguments);
  console.log(s); // '<span class="message-body-wrapper"><span class="message-flex-body"><span class="devtools-monospace message-body"><span class="objectBox objectBox-string">1,a,true'</span></span></span></span>
}
f(1, 'a', true);
//expected output: "1,a,true"
</pre>

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{jsxref("String.prototype.split()")}}
- {{jsxref("Array.prototype.toString()")}}
- {{jsxref("TypedArray.prototype.join()")}}