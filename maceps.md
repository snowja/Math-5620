# Math 5620 Machine Epsilon

**Routine Name:**           me

**Author:** Jeffrey Snow

**Language:** C++. The code can be compiled using the GNU C++ compiler (g++).

For example,

    g++ mEpsilon.cpp

will produce an executable **./a.exe** that can be executed. If you want a different name, the following will work a bit
better

    g++ -o mEpsilon mEpsilon.cpp

**Description/Purpose:** This routine will compute the extended double precision value for the machine epsilon or the number of digits
in the representation of real numbers in extended double precision. This is a routine for analyzing the behavior of any computer. This
usually will need to be run one time for each computer.

**Input:** There are no inputs needed in this case.

**Output:** This function returns an extended double precision value for the number of decimal digits that can be represented on the
computer being queried.

**Usage/Example:**

The function requires no argument and returns an extended double precision floating point value that represents the system's machine
epsilon.

      long double precision;
      precision = me();
      cout << precision << endl;

Output from the lines above:

      1.0842e-19

This value (1.0842e-19) is related to the decimal value of the number of digits that can be represented on the system. This value is
roughly nineteen (e-19 on the end of the example value).

**Implementation/Code:** The following is the code for me()

      long double me()
      {
        long double mEpsilon = 1.0;
        int count = 0;

        while (1.0 + 0.5 * mEpsilon != 1.0)
        {
          mEpsilon *= 0.5;
          count++;
        }
      //	cout << "The size of this machine's \"long double\" is " << sizeof(long double) << " bytes\n";
      //	cout << "The machine epsilon is calculated to be " << mEpsilon << ".\n";
      //	cout << "Another way of writing that is 2^-" << count << ".\n";

        return (mEpsilon);
      }

**Last Modified:** January/2018
