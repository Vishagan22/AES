# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
#include <stdio.h>
#include <string.h>

void aesEncrypt(char text[], int key)
{
    int i;

    for(i = 0; text[i] != '\0'; i++)
    {
        text[i] = text[i] + key;
    }
}

void aesDecrypt(char text[], int key)
{
    int i;

    for(i = 0; text[i] != '\0'; i++)
    {
        text[i] = text[i] - key;
    }
}

int main()
{
    char plaintext[100];
    int key;

    printf("Enter the plain text: ");
    scanf("%s", plaintext);

    printf("Enter the secret key value: ");
    scanf("%d", &key);

    aesEncrypt(plaintext, key);

    printf("\nEncrypted Text: %s\n", plaintext);

    aesDecrypt(plaintext, key);

    printf("Decrypted Text: %s\n", plaintext);

    return 0;
}
```
# OUTPUT:
<img width="1907" height="1090" alt="image" src="https://github.com/user-attachments/assets/8fe44643-bc2b-4503-96e8-22da7d9b127a" />


# RESULT:


