# Password Generator

This is a Python-based password generator that creates secure, random passwords with specific constraints. The generator ensures that the password includes various types of characters such as uppercase letters, lowercase letters, digits, and special characters.

## Features

- Customizable password length.
- Constraints to ensure password contains digits, special characters, uppercase letters, and lowercase letters.
- Cryptographically secure random password generation using Python’s `secrets` module.
- Validation of password constraints with regular expressions.

## Usage

To generate a password, simply call the `generate_password()` function with the desired parameters.

### Parameters:
- **`length`**: The length of the generated password. Default is `16`.
- **`nums`**: Whether the password should include digits. Set to `1` to include, `0` to exclude. Default is `1`.
- **`special_chars`**: Whether the password should include special characters. Set to `1` to include, `0` to exclude. Default is `1`.
- **`uppercase`**: Whether the password should include uppercase letters. Set to `1` to include, `0` to exclude. Default is `1`.
- **`lowercase`**: Whether the password should include lowercase letters. Set to `1` to include, `0` to exclude. Default is `1`.


