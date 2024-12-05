# SafeTransfer Project

SafeTransfer is a C++-based encryption and decryption program that ensures secure communication by leveraging time-based system information for dynamic key generation.
This project is designed to safeguard messages with an advanced layer of security.

## Features
- **Dynamic Key Generation:** Utilizes system date and time information for generating unique encryption keys.
- **Message Encryption:** Converts the input message into an encrypted format using ASCII transformations and binary representation.
- **Message Decryption:** Reconstructs the original message with the correct encryption key.
- **User-Friendly Menu:** Simple and intuitive options for encryption, decryption, and exiting the program.

## How It Works
1. **Key Generation:**
   - The key is derived from system information including year, month, day, hour, minute, second, and milliseconds.
   - The formula for the key combines these parameters into a unique value, ensuring every run produces a distinct key.

2. **Encryption:**
   - Each character in the input message is transformed using its ASCII value, the generated key, and cumulative sums.
   - The output is represented as a mix of 10-bit and 14-bit binary strings for added complexity.

3. **Decryption:**
   - The program validates the key provided by the user.
   - Using reverse transformations, it reconstructs the original message from the encrypted data.

## Usage
1. **Input a Message:** The program prompts the user to enter a message for encryption.
2. **Select an Option:**
   - **Encryption:** The program encrypts the message and displays the binary-encoded output.
   - **Decryption:** After entering the correct key, the program decrypts the message and displays the original text.
   - **Exit:** Terminate the program.

3. **Key Validation:** Only users with the correct key can decrypt the message, ensuring security.

## Example
- **Input:** "Hello, World!"
- **Encryption Output:** A binary string representing the encrypted message.
- **Decryption Output:** The original message, "Hello, World!"

## Dependencies
- C++ Standard Library (`iostream`, `chrono`, `ctime`, `bitset`, `iomanip`)
