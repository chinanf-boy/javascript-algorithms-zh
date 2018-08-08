# Bit Manipulation

#### Get Bit

This method shifts the relevant bit to the zeroth position. 
Then we perform `AND` operation with one which has bit 
pattern like `0001`.  This clears all bits from the original
number except the relevant one. If the relevant bit is one, 
the result is `1`, otherwise the result is `0`.

> See `getBit` function for further details.

#### Set Bit

This method shifts `1` over by `bitPosition` bits, creating a
value that looks like `00100`. Then we perform `OR` operation
that sets specific bit into `1` but it does not affect on
other bits of the number.

> See `setBit` function for further details.

#### Clear Bit

This method shifts `1` over by `bitPosition` bits, creating a
value that looks like `00100`. Than it inverts this mask to get
the number that looks like `11011`. Then `AND` operation is
being applied to both the number and the mask. That operation 
unsets the bit.

> See `clearBit` function for further details.

#### Update Bit

This method is a combination of "Clear Bit" and "Set Bit" methods.

> See `updateBit` function for further details.

#### Multiply By Two

This method shifts original number by one bit to the left.
Thus all binary number components (powers of two) are being
multiplying by two and thus the number itself is being 
multiplied by two.

```
Before the shift
Number: 0b0101 = 5
Powers of two: 0 + 2^2 + 0 + 2^0 

After the shift
Number: 0b1010 = 10
Powers of two: 2^3 + 0 + 2^1 + 0 
```

> See `multiplyByTwo` function for further details.

#### Divide By Two

This method shifts original number by one bit to the right.
Thus all binary number components (powers of two) are being
divided by two and thus the number itself is being 
divided by two without remainder.

```
Before the shift
Number: 0b0101 = 5
Powers of two: 0 + 2^2 + 0 + 2^0 

After the shift
Number: 0b0010 = 2
Powers of two: 0 + 0 + 2^1 + 0 
```

> See `divideByTwo` function for further details.

#### Switch Sign

This method make positive numbers to be negative and backwards.
To do so it uses "Twos Complement" approach which does it by
inverting all of the bits of the number and adding 1 to it.

```
1101 -3
1110 -2
1111 -1
0000  0
0001  1
0010  2
0011  3
``` 

> See `switchSign` function for further details.

## References

- [Bit Manipulation on YouTube](https://www.youtube.com/watch?v=NLKQEOgBAnw&t=0s&index=28&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
- [Negative Numbers in binary on YouTube](https://www.youtube.com/watch?v=4qH4unVtJkE&t=0s&index=30&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
- [Bit Hacks on stanford.edu](https://graphics.stanford.edu/~seander/bithacks.html)
