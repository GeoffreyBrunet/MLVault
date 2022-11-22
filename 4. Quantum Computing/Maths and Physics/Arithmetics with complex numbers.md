**MOC**:: [[4. Quantum Computing MOC]]
**Tags**:: #quantum #maths 

# Arithmetic operations
Let have 2 [[Complex numbers]]: $z_1=a+ib$ and $z_2=c+id$ for each operation.

## Addition
$$
z_1 + z_2 = (a+c)+i(b+d)
$$
## Substration
$$
z_1 - z_2 = (a-c)+i(b-d)
$$
## Multiplication
$$
z_1 \cdot z_2 = (a+ib)(c+id)
$$
$$
z_1 \cdot z_2 = ac+iad + ibc + i^2bd
$$

Now separate real part and imaginary part ($ac$ and $i^2bd$ are real part, $i^2=-1$):
$$
z_1 \cdot z_2 = ac-bd +i(ad + bc)
$$
## Division
$$
\frac{z_1}{z_2} = \frac{a+ib}{c+id}
$$
Need to find and eliminate imaginary part from denominator, done by multiplying the numerator and the denominator with the complex conjugate of the denominator, which is defined as:
$$
\frac{z_1}{z_2} = \frac{a+ib}{c+id} \cdot \frac{c-id}{c-id}
$$
$$
\frac{z_1}{z_2} = \frac{ac-iad-ibc+bd}{c^2-icd+icd+d^2}
$$
$$
\frac{z_1}{z_2} = \frac{ac-iad+ibc+bd}{c^2+d^2}
$$
Split real part and imaginary part of the numerator:
$$
\frac{z_1}{z_2} = \frac{(ac+bd)+i(-ad+bc)}{c^2+d^2}
$$
