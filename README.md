# Fast-Inverse-Square-Root
Fast inverse square root, sometimes referred to as Fast InvSqrt() or by the hexadecimal constant 0x5F3759DF, is an algorithm that estimates 1⁄√x, the reciprocal (or multiplicative inverse) of the square root of a 32-bit floating-point number x in IEEE 754 floating-point format. This operation is used in digital signal processing to normalize a vector, i.e., scale it to length 1. For example, computer graphics programs use inverse square roots to compute angles of incidence and reflection for lighting and shading. The algorithm is best known for its implementation in 1999 in the source code of Quake III Arena, a first-person shooter video game that made heavy use of 3D graphics. The algorithm only started appearing on public forums such as Usenet in 2002 or 2003. At the time, it was generally computationally expensive to compute the reciprocal of a floating-point number, especially on a large scale; the fast inverse square root bypassed this step.

### The algorithm:
Accepts a 32-bit floating-point number as the input and stores a halved value for later use. Then, treating the bits representing the floating-point number as a 32-bit integer, a logical shift right by one bit is performed and the result subtracted from the number 0x5F3759DF, which is a floating point representation of an approximation of √2127. This results in the first approximation of the inverse square root of the input. Treating the bits again as a floating-point number, it runs one iteration of Newton's method, yielding a more precise approximation.

The algorithm was originally attributed to John Carmack, but an investigation showed that the code had deeper roots in both the hardware and software side of computer graphics. Adjustments and alterations passed through both Silicon Graphics and 3dfx Interactive, with Gary Tarolli's implementation for the SGI Indigo as the earliest known use. It is not known how the constant was originally derived, though investigation has shed some light on possible methods
