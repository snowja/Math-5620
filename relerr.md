# Math 5620 Relative Error

**Routine Name:**           re

**Author:** Jeffrey Snow

**Language:** C++. The code can be compiled using the GNU C++ compiler (g++).

For example,

    g++ rError.cpp

will produce an executable **./a.exe** that can be executed. If you want a different name, the following will work a bit
better

    g++ -o rError rError.cpp

**Description/Purpose:** This routine will compute the relative error given a calculated value and an exact value.

**Input:** Two inputs are required. The first is a calculated or estimated value. The second is the exact or analytical value.

**Output:** This function returns an extended double precision value of the absolute value of the difference between the two input
values divided by the absolute value of the exact value.

**Usage/Example:**

The function requires two numerical arguments and returns an extended double precision floating point value that represents the relative
error between those arguments.

      long double relative, calc, ex;

      calc = .1;
      ex = .11;
      relative = re(calc, ex);

      cout << relative << endl;

Output from the lines above:

      0.0909091

This value (0.0909091) is absolute value of the difference between the two inputs divided by the absolute value of the exact input.

**Implementation/Code:** The following is the code for the re function

      long double re(long double calculated, long double exact)
      {
        return abs(calculated - exact) / abs(exact);
      }

**Last Modified:** January/2018
