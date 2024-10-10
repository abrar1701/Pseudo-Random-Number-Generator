# Pseudorandom Number Generator
## Aim:
## Design Steps:
### Step 1:
Design of the Pseudorandom Number Generator.
### Step 2:
Implement using C or Python code.
### Step 3:
PRNGs are used in probability and statistics applications to produce large quantities of random digits. They are not truly random, but they should pass the same statistical tests for randomness as a sequence of truly random numbers.
## Program:
```c
#include <stdio.h>
#define A 1664525
#define C 1013904223
#define M 4294967296 // 2^32

unsigned int lcg(unsigned int seed) {
    return (A * seed + C) % M;
}

int main() {
    unsigned int seed;
    int n, i;
    printf("*Pseudorandom number generator*\n\n");
    printf("Enter the seed value: ");
    scanf("%u", &seed);
    printf("Enter how many random numbers to generate: ");
    scanf("%d", &n);
    printf("Random numbers:\n");
    for (i = 0; i < n; i++) {
        seed = lcg(seed);
        printf("%u\n", seed);
    }
    return 0;
}
```
## Output :
![Screenshot 2024-10-10 090419](https://github.com/user-attachments/assets/5e44a2cd-f0c3-444a-910f-0bd42e5bc20f)

## Result:
The program is executed successfully.
