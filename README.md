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

### Example Usage:
```python
new_password = generate_password()
print(f'Generated password: {new_password}')

This will generate a password of 16 characters, ensuring it contains at least one digit, one special character, one uppercase letter, and one lowercase letter.

Customization:
To generate a password with different constraints, adjust the function parameters:

python
Copy
Edit
new_password = generate_password(length=12, nums=0, special_chars=0)
print(f'Generated password: {new_password}')
This will generate a 12-character password without digits or special characters.

Methods Used
secrets.choice(): The secrets module securely selects random characters from the available character sets (letters, digits, symbols) to ensure cryptographic strength.
string.ascii_letters, string.digits, string.punctuation: Predefined sets of characters representing letters, digits, and punctuation, respectively.
Regular Expressions (re.findall()): Used to check if the generated password satisfies the constraints:
r'\d' checks for digits.
fr'[{symbols}]' checks for special characters.
r'[A-Z]' checks for uppercase letters.
r'[a-z]' checks for lowercase letters.
The password is checked against the defined constraints, and if any constraint is not met, a new password is generated.
