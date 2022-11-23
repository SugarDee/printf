# Printf working principle
![printf](https://www.equestionanswers.com/c/images/printf-block-diagram.png)

The C printf or print function prints strings to the console while transforming input variables to strings. It accepts a formatting string and a few optional variables as input.

The functions printf , which accept numerous arguments, are well known as variable length arguments functions or vararg functions. Consider the printf function. The user enters arguments along with a string. The internal buffer created by printf is used to build the output string. The character is copied to the output string as printf iterates through each character in the user string. Printf only terminates when it sees "%." "%" indicates that there is a conversion argument. The types of arguments are char, int, long, float, double, or string. It does so and adds it to the output buffer as a string. If the parameter is a string, a string copy is performed. Printf copies the full buffer to the stdout file when it finally reaches the end of the user sting.

## Implementation printf

 We name it _printf(). It has one string argument (str) and rest are variable arguments. Variable arguments are managed by macros like va_start, va_arg and va_end. A temporary buffer (buff) is there to construct the output buffer. A while loop is needed to scan each characters in the input string. 
 
  Now we loop character by character in the loop and copy each character to output string. Same time we check for "%". "%" is not copied to output string. Once we found it, we check the next character. This is the formatting character.
 
 Printf supports different and variaties of formatting. "c" is for character, "d" for decimal integer, "f" for floating point, "x" for hexadecimal and "s" for strings.
 We merge the formatting and pick the argument variable using va_arg(). Argument variable is then converted to string format and appends to the output string. character can be copied as it is and Itoa function is used for integer to string conversion.
 C language itoa() function is used to convert argument integer to string. Integer to String conversion is a process that take each digits and convert those to ASCII format.
 
 This process of coping characters and conversion of arguments repeats until the string is terminated to last NULL character. For simplicity we have implemented only c, s,, d, i, u, o, x formatting cases.Thus the output string prints in the actual console. _printf() then returns the number of characters which is printed in the console and exit the function.
 
 this project was created by #### SugarDee and Augustine-ebuka
 thank you for reading!
