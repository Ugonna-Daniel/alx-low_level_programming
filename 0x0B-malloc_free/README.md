0. Float like a butterfly, sting like a bee Write a function that creates an a   rray of chars, and initializes it with a specific char. Prototype: char *cr   eate_array(unsigned int size, char c); Returns NULL if size = 0 Returns a p   ointer to the array, or NULL if it fails

1. The woman who has no imagination has no wings Write a function that returns   a pointer to a newly allocated space in memory, which contains a copy of th   e string given as a parameter. Prototype: char *_strdup(char *str); The _st   rdup() function returns a pointer to a new string which is a duplicate of t   he string str. Memory for the new string is obtained with malloc, and can b   e freed with free. Returns NULL if str = NULL On success, the _strdup funct   ion returns a pointer to the duplicated string. It returns NULL if insuffic   ient memory was available

2. He who is not courageous enough to take risks will accomplish nothing in li   fe Write a function that concatenates two strings. Prototype: char *str_con   cat(char *s1, char *s2); The returned pointer should point to a newly alloc   ated space in memory which contains the contents of s1, followed by the con   tents of s2, and null terminated if NULL is passed, treat it as an empty st   ring The function should return NULL on failure

3. If you even dream of beating me you'd better wake up and apologize Write a    function that returns a pointer to a 2 dimensional array of integers. Proto   type: int **alloc_grid(int width, int height); Each element of the grid sho   uld be initialized to 0 The function should return NULL on failure If width   or height is 0 or negative, return NULL

4. It's not bragging if you can back it up Write a function that frees a 2 dim   ensional grid previously created by your alloc_grid function. Prototype: vo   id free_grid(int **grid, int height); Your program should not crash if the    grid is invalid (NULL or size = 0) Note that we will compile with your allo   c_grid.c file. Make sure it compiles

5. It isn't the mountains ahead to climb that wear you out; it's the pebble in   your shoe Write a function that concatenates all the arguments of your prog   ram. Prototype: char *argstostr(int ac, char **av); Returns NULL if ac == 0   or av == NULL Returns a pointer to a new string, or NULL if it fails Each a   rgument should be followed by a \n in the new string

6. I will show you how great I am
   Write a function that splits a string into words.
   Prototype: char **strtow(char *str);
   The function returns a pointer to an array of strings (words)
   Each element of this array should contain a single word, null-terminated
   The last element of the returned array should be NULL
   Words are separated by spaces
   Returns NULL if str == NULL or str == ""
   If your function fails, it should return NULL