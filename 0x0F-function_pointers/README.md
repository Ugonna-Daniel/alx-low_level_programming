0. What's my name Write a function that prints a name. Prototype: void print_na   me(char *name, void (*f)(char *));

1. If you spend too much time thinking about a thing, you'll never get it done    Write a function that executes a function given as a parameter on each eleme   nt of an array. Prototype: void array_iterator(int *array, size_t size, void   (*action)(int)); where size is the size of the array and action is a pointer   to the function you need to use

2. To hell with circumstances; I create opportunities mandatory Write a functio   n that searches for an integer.

   Prototype: int int_index(int *array, int size, int (*cmp)(int)); where size    is the number of elements in the array array cmp is a pointer to the functio   n to be used to compare values int_index returns the index of the first elem   ent for which the cmp function does not return 0 If no element matches, retu   rn -1 If size <= 0, return -1

3. A goal is not always meant to be reached, it often serves simply as somethin   g to aim at Write a program that performs simple operations.
   You are allowed to use the standard library Usage: calc num1 operator num2 Y   ou can assume num1 and num2 are integers, so use the atoi function to conver   t them from the string input to int operator is one of the following: +: add   ition -: subtraction *: multiplication /: division %: modulo The program pri   nts the result of the operation, followed by a new line You can assume that    the result of all operations can be stored in an int if the number of argume   nts is wrong, print Error, followed by a new line, and exit with the status    98 if the operator is none of the above, print Error, followed by a new line   , and exit with the status 99 if the user tries to divide (/ or %) by 0, pri   nt Error, followed by a new line, and exit with the status 100 This task req   uires that you create four different files.

   3-calc.h

   This file should contain all the function prototypes and data structures use   d by the program. You can use this structure:

   /**

   struct op - Struct op
   @op: The operator * @f: The function associated */ typedef struct op { char    *op; int (*f)(int a, int b); } op_t;

   3-op_functions.c

   This file should contain the 5 following functions (not more):

   op_add: returns the sum of a and b. Prototype: int op_add(int a, int b); op_   sub: returns the difference of a and b. Prototype: int op_sub(int a, int b);   op_mul: returns the product of a and b. Prototype: int op_mul(int a, int b);   op_div: returns the result of the division of a by b. Prototype: int op_div(   int a, int b); op_mod: returns the remainder of the division of a by b. Prot   otype: int op_mod(int a, int b);

   3-get_op_func.c

   This file should contain the function that selects the correct function to p   erform the operation asked by the user. You’re not allowed to declare any ot   her function.

   Prototype: int (*get_op_func(char *s))(int, int); where s is the operator pa   ssed as argument to the program This function returns a pointer to the funct   ion that corresponds to the operator given as a parameter. Example: get_op_f   unc("+") should return a pointer to the function op_add You are not allowed    to use switch statements You are not allowed to use for or do ... while loop   s You are not allowed to use goto You are not allowed to use else You are no   t allowed to use more than one if statement in your code You are not allowed   to use more than one while loop in your code If s does not match any of the    5 expected operators (+, -, , /, %), return NULL You are only allowed to dec   lare those two variables in this function: op_t ops[] = { {"+", op_add}, {"-   ", op_sub}, {"", op_mul}, {"/", op_div}, {"%", op_mod}, {NULL, NULL} }; int    i; 3-main.c

   This file should contain your main function only.

   You are not allowed to code any other function that main in this file You ar   e not allowed to directly call op_add, op_sub, op_mul, op_div or op_mod from   the main function You have to use atoi to convert arguments to int You are n   ot allowed to use any kind of loop You are allowed to use a maximum of 3 if    statements

4. Most hackers are young because young people tend to be adaptable. As long as   you remain adaptable, you can always be a good hacker

   Write a program that prints the opcodes of its own main function.

   Usage: ./main number_of_bytes
   Output format:
   the opcodes should be printed in hexadecimal, lowercase
   each opcode is two char long
   listing ends with a new line
   see example
   You are allowed to use printf and atoi
   You have to use atoi to convert the argument to an int
   If the number of argument is not the correct one, print Error, followed by a   new line, and exit with the status 1
   If the number of bytes is negative, print Error, followed by a new line, and   exit with the status 2
   You do not have to compile with any flags
   Note: if you want to translate your opcodes to assembly instructions, you ca   n use, for instance udcli.
   Note 0: je is equivalent to jz
   Note 1: depending on how you write your main function, and on which machine    you compile your program, the opcodes (and by extension the assembly code) m   ight be different than the above example