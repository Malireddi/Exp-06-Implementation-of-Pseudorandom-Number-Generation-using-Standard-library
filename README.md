# Exp-06-Implementation of Pseudorandom Number Generation using Standard library

## AIM:
To implement Pseudorandom Number Generation using Standard Library.

## ALGORITHM:
### Step 1: 
Get the number of random numbers to generate from the user.
### Step 2: 
Read the minimum and maximum values for the random number range.
### Step 3: 
Initialize the random seed using the current time.
### Step 4: 
Generate a random number by calculating the remainder of division with the range (max - min + 1) and adding the minimum value.
### Step 5: 
Repeat the random number generation for the specified count.
### Step 6: 
Print each generated random number.
### Step 7: 
End the program.

## PROGRAM:
## DEVELOPED BY : Nandyala malyadri reddy
## REGISTER NO. : 212223100037
```c
#include <stdio.h>

#define A 1234567
#define C 7654321
#define M 9876543210

// Linear Congruential Generator function
unsigned int lcg(unsigned int seed) {
    return (A * seed + C) % M; // Generate the next pseudorandom number
}

int main() {
    unsigned int seed;
    int n, i;

    printf("* Pseudorandom Number Generator *\n\n");
    
    printf("Enter the seed value: ");
    scanf("%u", &seed); // Input seed value
    
    printf("Enter how many random numbers to generate: ");
    scanf("%d", &n); // Input number of random numbers to generate
    
    printf("Random numbers:\n");
    
    for (i = 0; i < n; i++) {
        seed = lcg(seed); // Generate the next random number
        printf("%u\n", seed); // Output the random number
    }

    return 0;
}
```
## Output:

![image](https://github.com/user-attachments/assets/80ed71d5-243c-40e9-af9f-e0a643c4e1c8)

## Result :
The program for Pseudorandom Number Generation is executed successfully
