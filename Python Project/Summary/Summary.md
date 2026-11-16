# Project Summary - Password Strength Checker (PS 2)

## 1. Problem
Accounts are easily hacked because of weak passwords. In this project, a Python program has
been built that checks a password against security rules, classifies it as
**Weak / Medium / Strong**, and gives suggestions for the rules that failed.

## 2. Rules (1 rule = 1 point)
| # | Rule |
|---|------|
| 1 | Length >= 8 |
| 2 | At least 1 uppercase letter (A-Z) |
| 3 | At least 1 lowercase letter (a-z) |
| 4 | At least 1 digit (0-9) |
| 5 | At least 1 special character (@ # $ % & * !) |

**Scoring:** 0-2 = Weak, 3-4 = Medium, 5 = Strong

## 3. Approach (How the Code Works)
1. The user's password is taken using `input()` and passed to the `check_password()` function.
2. Invalid input is checked first: if the password is empty or contains a space, an error
   message is printed and the program stops.
3. The program starts with `score = 0` and an empty `suggestions` list.
4. Each rule has an `if / else` check. If the rule passes, `score += 1`; otherwise, a
   suggestion is added to the list using `append()`.
5. `re.search()` (Regex) is used to check for uppercase, lowercase, digit, and special characters.
6. Based on the final score, `if / elif / else` decides whether the password is Weak, Medium, or Strong.
7. The strength, score, and suggestions (printed in bullet form using a loop) are displayed.

## 4. Concepts Used
- **Strings:** `len()` for the length check, `" " in password` for the space check
- **Lists:** to store suggestions
- **Conditions:** `if / elif / else` to evaluate rules and decide strength
- **Loop:** a `for` loop to print all suggestions
- **Regex (`re` module):** pattern matching, such as `[A-Z]`, `[a-z]`, `[0-9]`, `[@#$%&*!]`
- **Functions:** `check_password()`

## 5. Test Results
| Test Case | Input | Output | Status |
|-----------|-------|--------|--------|
| 1 Normal | abc123 | Weak (2/5), 3 suggestions | Pass |
| 2 Boundary | Hello123 | Medium (4/5), add a special character | Pass |
| 3a Invalid | (empty) | Password cannot be empty. | Pass |
| 3b Invalid | Hello 123 | Password must not contain spaces. | Pass |
| 4 Strong | Hello@123Xy | Strong (5/5), no suggestions | Pass |

Screenshots are in the `Screenshots/` folder (test1.png, test2.png, test3a.png, test3b.png, test4.png).

## 6. Conclusion
The program gives the correct output for all test cases. The user can instantly see how
strong their password is and what to do to improve it.