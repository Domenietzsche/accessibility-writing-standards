# Error messages

## Principle

A field-level error message states what happened and what to do next.
Nothing else belongs in it.

## Structure

Two parts, in this order:

1. What happened. The specific problem with the value entered.
2. What to do next. The action that resolves it.

**Failing:** "Invalid input."
**Passing:** "This date is in the past. Enter a date from today onward."

## What belongs in helper text instead

Conversion logic, system rules, and format requirements are persistent
information. They belong in helper text below the field, visible before,
during, and after input.

Putting them in the error component means the user only learns the rule
after failing.

**Failing:** error reads "Amount must be a multiple of 100."
**Passing:** helper text reads "Amounts are processed in multiples of 100."
Error reads "Enter an amount in multiples of 100. The nearest options are
400 and 500."

## WCAG mapping

- **3.3.1 Error Identification (Level A).** The item in error is identified
  and described in text.
- **3.3.3 Error Suggestion (Level AA).** When a correction is known, it is
  provided to the user.

3.3.3 is the stronger criterion for the "what to do next" half. An error
that identifies the problem without offering the correction can satisfy
3.3.1 and still fail 3.3.3.

## Examples

| Failing | Passing |
|---|---|
| Invalid input | Card numbers are 16 digits. This one has 15. |
| Error | Passwords need at least one number. Add one and try again. |
| Something went wrong | We could not reach the server. Try again in a moment. |
