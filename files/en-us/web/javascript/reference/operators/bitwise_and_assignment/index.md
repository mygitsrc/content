---
title: Bitwise AND assignment (&=)
slug: Web/JavaScript/Reference/Operators/Bitwise_AND_assignment
tags:
- Assignment operator
- JavaScript
- Language feature
- Operator
- Reference
browser-compat: javascript.operators.bitwise_and_assignment
---
{{jsSidebar("Operators")}}

The bitwise AND assignment operator (`&=`) uses the binary representation of
both operands, does a bitwise AND operation on them and assigns the result to
the variable.

{{EmbedInteractiveExample("pages/js/expressions-bitwise-and-assignment.html")}}

## Syntax

<pre class="brush: js"><strong>Operator:</strong> x &#x26;= y
<strong>Meaning:</strong>  x  = x &#x26; y
</pre>

## Examples

### Using bitwise AND assignment

```js
let a = 5;
// 5:     00000000000000000000000000000101
// 2:     00000000000000000000000000000010
a &= 2; // 0
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Assignment operators in the JS guide](/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Assignment)
- [Bitwise AND operator](/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_AND)