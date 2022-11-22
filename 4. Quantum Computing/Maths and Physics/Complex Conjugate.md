**MOC**:: [[4. Quantum Computing MOC]]
**Tags**:: #quantum #maths 

# Definition
The conjugate of a complex number z is the complex number with the same real part as z but the opposite imaginary part.

# Complex conjugate operations
Let have complex number as $z=a+ib$ and complex conjugate as $\overline{z} = a-ib$.
## Addition
For addition, do real part plus imaginary part:
$$
z + \overline{z} = (a+a)+i(b-b)
$$
$$
z + \overline{z} = 2a
$$
So:
$$
2a = 2\Re(z)
$$
$$
\Re(z) = \frac{z + \overline{z}}{2}
$$
## Substraction
$$
z - \overline{z} = (a-a)+i(b-(-b))
$$
$$
z + \overline{z} = 2ib = 2\Im(z)
$$
$$
\Re(z) = \frac{z + \overline{z}}{2i}
$$
## Multiplication
$$
z \cdot \overline{z} = (a+ib)(a+ib)
$$
$$
z \cdot \overline{z} = a^2 - iab+iab+b^2
$$
$$
z \cdot \overline{z} = a^2 + b^2
$$

Now we have absolute value of $z^2$ (the absolute value of a real number is its numerical value considered without taking into account its sign):
$$
a^2 + b^2 = \left| z \right|^2
$$
