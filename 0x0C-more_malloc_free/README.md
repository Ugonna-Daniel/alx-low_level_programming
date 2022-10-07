0. Trust no one Write a function that allocates memory using malloc. Pr   ototype: void *malloc_checked(unsigned int b); Returns a pointer to    the allocated memory if malloc fails, the malloc_checked function sh   ould cause normal process termination with a status value of 98

1. string_nconcat Write a function that concatenates two strings. Proto   type: char *string_nconcat(char *s1, char *s2, unsigned int n); The    returned pointer shall point to a newly allocated space in memory, w   hich contains s1, followed by the first n bytes of s2, and null term   inated If the function fails, it should return NULL If n is greater    or equal to the length of s2 then use the entire string s2 if NULL i   s pass, treat it as an empty string

2. _calloc Write a function that allocates memory for an array, using m   alloc. Prototype: void *_calloc(unsigned int nmemb, unsigned int siz   e); The _calloc function allocates memory for an array of nmemb elem   ents of size bytes each and returns a pointer to the allocated memor   y. The memory is set to zero If nmemb or size is 0, then _calloc ret   urns NULL If malloc fails, then _calloc returns NULL

3. array_range Write a function that creates an array of integers. Prot   otype: int *array_range(int min, int max); The array created should    contain all the values from min (included) to max (included), ordere   d from min to max Return: the pointer to the newly created array If    min > max, return NULL If malloc fails, return NULL

4. _realloc Write a function that reallocates a memory block using mall   oc and free Prototype: void *_realloc(void *ptr, unsigned int old_si   ze, unsigned int new_size); where ptr is a pointer to the memory pr    viously allocated with a call to malloc: malloc(old_size)
   old_size is the size, in bytes, of the allocated space for ptr
   and new_size is the new size, in bytes of the new memory block
   The contents will be copied to the newly allocated space, in the ran   ge from the start of ptr up to the minimum of the old and new sizes
   If new_size > old_size, the “added” memory should not be initialized
   If new_size == old_size do not do anything and return ptr
   If ptr is NULL, then the call is equivalent to malloc(new_size), for   all values of old_size and new_size
   If new_size is equal to zero, and ptr is not NULL, then the call is    equivalent to free(ptr). Return NULL
   Don’t forget to free ptr when it makes sense
   FYI: The standard library provides a different function: realloc. Ru   n man realloc to learn more