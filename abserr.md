# Math 5620 Absolute Error

**Routine Name:**           ae

**Author:** Jeffrey Snow

**Language:** C++. The code can be compiled using the GNU C++ compiler (g++).

For example,

    g++ aError.cpp

will produce an executable **./a.exe** that can be executed. If you want a different name, the following will work a bit
better

    g++ -o aError aError.cpp

**Description/Purpose:** This routine will compute the absolute error given a calculated value and an exact value.

**Input:** Two inputs are required. The first is a calculated or estimated value. The second is the exact or analytical value.

**Output:** This function returns an extended double precision value absolute value of the difference between the two input values.

**Usage/Example:**

The function requires two numerical arguments and returns an extended double precision floating point value that represents the absolute
error between those arguments.

      long double absolute, calc, ex;

      calc = .1;
      ex = .11;
      absolute = ae(calc, ex);

    	cout << absolute << endl;

Output from the lines above:

      0.01

This value (0.01) is absolute value of the difference between the two inputs.

**Implementation/Code:** The following is the code for the ae function

      long double ae(long double calculated, long double exact)
      {
        return abs(calculated - exact);
      }

**Last Modified:** January/2018
