# Password Strength Checker

A Python 3 console program that checks a password against 5 security rules,
classifies it as **Weak / Medium / Strong**, and gives suggestions for improvement.

## Features
- Checks the password against 5 rules (length, uppercase, lowercase, digit, special character)
- Score out of 5 and strength classification
- Suggestions for the rules that failed
- Error handling for empty passwords and passwords containing spaces
- Uses Regex (`re` module)

## Rules
1. Length >= 8
2. Uppercase letter
3. Lowercase letter
4. Digit
5. Special character (`@ # $ % & * !`)

**Score:** 0-2 Weak | 3-4 Medium | 5 Strong

## Requirements
- Python 3.x
- No extra libraries needed (`re` is built-in)

## How to Run
```bash
cd Code
python password_checker.py
```
When `Enter your password:` appears, type your password and press Enter.

## Sample Output
```
Enter your password: abc123
Strength: Weak (2/5)
Suggestions:
- Use at least 8 characters.
- Add an uppercase letter.
- Add a special character.
```
```
Enter your password: Hello@123Xy
Strength: Strong (5/5)
No suggestions. Your password is secure.
```

## Test Cases
| Input | Output |
|-------|--------|
| abc123 | Weak (2/5) + 3 suggestions |
| Hello123 | Medium (4/5), Add a special character. |
| (empty) | Password cannot be empty. |
| Hello 123 | Password must not contain spaces. |
| Hello@123Xy | Strong (5/5), No suggestions. Your password is secure. |

Output screenshots are in the `Screenshots/` folder.

## Folder Structure
```
Password_Strength_Checker/
├── Summary/       -> summary.md
├── Readme/        -> README.md
├── Code/          -> password_checker.py
├── Screenshots/   -> test1.png, test2.png, test3a.png, test3b.png, test4.png
└── PPT/           -> presentation
```

## Author
Name: Mo.Jamal Khan |  ERF: RU-26-00654