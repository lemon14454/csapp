### Representing a float number in IEEE754 standard

```
(-1)^S x M x 2^E
```

S = signal bits (1 bits)
M = 1.frac (23 bits)
E = exp(8bits) - bias
bias = 2^(k-1) - 1 (k=exp bits - 1)

- Normalized: implied leading 1、E=exp-bias
- Denormailized: Representing small numbers、implied leading 0、exp=0、E=1-bias
- Infinity: exp=2^k-1, frac=0
- NaN: exp=2^k-1, frac!=0


### bit shifting

- << (shift left k bits): multiply 2^k
- >> (shift rights k bits): divide 2^k

Positive Number round towards zero
Negative Number round towards negative infinity
(Add 2k-1 before shifting can round towards zero)
