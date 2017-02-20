ADD
===

Sums two unsigned integers

Input stack: `a` `b`
Output stack: `c`

`AND` will push the sum of `a` and `b` to the top of the stack.

## Allocation

Runtime allocations for decoding numbers and heap allocation
for the result.

## Errors

[EmptyStack](../ERRORS/EmptyStack.md) error if there are less than two items on the stack

## Examples

```
1 2 UINT/ADD => 3
```

## Tests

```test
works : 2 1 UINT/ADD 3 EQUAL?.
empty_stack : [UINT/ADD] TRY UNWRAP 0x04 EQUAL?.
empty_stack_1 : [1 UINT/ADD] TRY UNWRAP 0x04 EQUAL?.
```