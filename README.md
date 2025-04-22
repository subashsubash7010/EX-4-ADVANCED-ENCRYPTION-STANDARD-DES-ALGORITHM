# EX-8-ADVANCED-ENCRYPTION-STANDARD-DES-ALGORITHM

## Aim:
  To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## ALGORITHM: 
  1. AES is based on a design principle known as a substitution–permutation. 
  2. AES does not use a Feistel network like DES, it uses variant of Rijndael. 
  3. It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits. 
  4. AES operates on a 4 × 4 column-major order array of bytes, termed the state

## PROGRAM: 
```
def simple_encrypt(plaintext, key):
    return ''.join(chr(ord(c) ^ ord(key[i % len(key)])) for i, c in enumerate(plaintext))

def simple_decrypt(ciphertext, key):
    return ''.join(chr(ord(c) ^ ord(key[i % len(key)])) for i, c in enumerate(ciphertext))

def print_ascii(ciphertext):
    print("Encrypted Message (ASCII values):", ' '.join(str(ord(c)) for c in ciphertext))

# Main
plaintext = input("Enter the plaintext: ")
key = input("Enter the key: ")

ciphertext = simple_encrypt(plaintext, key)
print_ascii(ciphertext)

decrypted = simple_decrypt(ciphertext, key)
print("Decrypted Message:", decrypted)
```
## OUTPUT:
![Screenshot 2025-04-22 185627](https://github.com/user-attachments/assets/7fefba81-8236-4622-bc9b-11587c380040)

## RESULT: 
The program is executed successfully .
