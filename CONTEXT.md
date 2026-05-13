# Palindro — Domain Context

## Glossary

### Palindrome
A string that reads the same forwards and backwards after normalization. "Palindrome" applies to the normalized form, not the raw input.

### Raw Input
The original string the user types. May contain spaces, punctuation, mixed case. Never mutated.

### Normalized String
Derived from Raw Input by stripping all non-alphanumeric characters and lowercasing. This is what palindrome comparison runs on. Shown to the user alongside the result.

### Result
Binary verdict: **Palindrome** or **Not a palindrome**. Derived from comparing the Normalized String to its reverse.

## Decisions

- Normalization strips all non-alphanumeric characters and lowercases. "A man, a plan, a canal: Panama" normalizes to "amanaplanacanalpanama".
- UI shows Result + Normalized String. Does not show raw input annotated or chars dimmed.
- Single input field — checks one phrase at a time. Does not scan for palindromes within larger text.
- Vanilla HTML/CSS/JS. No framework.
