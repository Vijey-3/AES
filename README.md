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

int main()
{
    char plain[100], key[100], cipher[100], decrypt[100];
    int i, len, keyLen;

    printf("Enter the plaintext: ");
    scanf("%s", plain);

    printf("Enter the key: ");
    scanf("%s", key);

    len = strlen(plain);
    keyLen = strlen(key);

    printf("\nENCRYPTED MESSAGE (ASCII): ");

    for (i = 0; i < len; i++)
    {
        cipher[i] = plain[i] ^ key[i % keyLen];
        printf("%d ", (unsigned char)cipher[i]);
    }

    cipher[len] = '\0';

    printf("\nDECRYPTED MESSAGE: ");

    for (i = 0; i < len; i++)
    {
        decrypt[i] = cipher[i] ^ key[i % keyLen];
        printf("%c", decrypt[i]);
    }

    decrypt[len] = '\0';

    return 0;
}
```
# OUTPUT:
<img width="1919" height="908" alt="image" src="https://github.com/user-attachments/assets/525ff5b8-5397-4e48-8514-d144e44e3068" />

# RESULT:
Successfully implemented using Advanced Encryption Standard (AES) Algorithm.



