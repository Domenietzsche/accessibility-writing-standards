# Link text

## Principle

Link text describes its destination. A user who encounters the link with
no surrounding context should know where it goes.

## Why "click here" fails

Screen reader users can navigate by pulling up a list of every link on the
page, stripped of surrounding text. A page with nine links reading
"click here" produces a list of nine identical items.

Sighted users skimming the page have the same problem in a milder form.

## The fix

Move the destination into the link text.

**Failing:** To review your statement, [click here].
**Passing:** [Review your statement].

Avoid the opposite failure: linking an entire sentence. The target stays
tight enough to be readable in a link list.

## Link text and buttons

Links navigate. Buttons perform actions. Writing "Click here to delete"
on a destructive button hides the consequence behind the mechanic.

**Failing:** [Click here]
**Passing:** [Delete this transfer]

## WCAG mapping

- **2.4.4 Link Purpose (In Context) (Level A).** The purpose of each link
  can be determined from the link text alone, or from the link text
  together with its programmatically determined context.
- **2.4.9 Link Purpose (Link Only) (Level AAA).** The purpose can be
  determined from the link text alone.

2.4.4 allows surrounding context to carry the meaning. 2.4.9 does not.
Writing to 2.4.9 is a content decision that costs nothing and removes the
dependency on context entirely.

## Examples

| Failing | Passing |
|---|---|
| Click here | Download the 2025 statement (PDF) |
| Read more | Read the full accessibility policy |
| Learn more about this here | How overdraft fees are calculated |