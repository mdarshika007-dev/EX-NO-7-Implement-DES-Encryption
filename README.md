# EX-NO-7-Implement-DES-Encryption

## DATE: 05-08-26
## Aim:

To use the Data Encryption Standard (DES) algorithm for a practical application, such as securing sensitive data transmission in financial transactions.

## ALGORITHM:

1. DES is based on a symmetric key encryption technique that encrypts data in 64-bit blocks.
2. DES uses a Feistel network structure with 16 rounds of processing for encryption.
3. DES has a 64-bit key, but only 56 bits are used for encryption (the remaining 8 bits are for parity).
4. DES applies initial and final permutations along with 16 rounds of substitution and permutation transformations to produce ciphertext.

## Program:
~~~
#include <stdio.h>

int main() {
    char text[100];
    char key;
    int i;

    printf("Enter Plain Text: ");
    scanf("%s", text);

    printf("Enter Key (single character): ");
    scanf(" %c", &key);

    for(i = 0; text[i] != '\0'; i++) {
        text[i] = text[i] ^ key;
    }

    printf("Encrypted Text: %s\n", text);

    for(i = 0; text[i] != '\0'; i++) {
        text[i] = text[i] ^ key;
    }

    printf("Decrypted Text: %s\n", text);

    return 0;
}
~~~


## Output:
<img width="1911" height="662" alt="image" src="https://github.com/user-attachments/assets/035829c4-5faa-49f5-b0ce-650111bb4b4e" />



## Result:
  The program is executed successfully

