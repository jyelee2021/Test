# How to edit the AI Tool Quick Check yourself

You don't need to know how to code. Everything you'd want to change (questions,
help text, follow-up questions, result messages) is in one clearly labeled block
near the top of `ai-tool-checklist.html`.

## Where to edit

1. On GitHub, open this repository (`jyelee2021/Test`) and choose the branch
   `claude/child-welfare-ethics-checklist-a9rk8h`.
2. Click `ai-tool-checklist.html`, then the **pencil icon** (Edit this file).
3. Scroll down to the block that starts with `EDIT HERE`.
   It ends at `END OF EDIT-HERE SECTION`. Change things only between those two lines.
4. Click **Commit changes**. You can undo any edit later from the file's History.

## What each piece does

Each question looks like this:

```js
{ q: "Does a trained person make the final decision, not the tool?",
  hint: "",
  ask: "Who reviews the tool's output before anything happens to a family?",
  key: true },
```

| Part   | What it is |
|--------|------------|
| `q`    | The question people see. |
| `hint` | Small help text behind "What to look for". Use `""` for none. |
| `ask`  | The follow-up question shown when someone answers No or Not sure. |
| `key`  | Optional. `key: true` means a "No" answer triggers the red **Stop and ask first** message. Delete the line (and the comma before it) if you don't want it. |

## Common changes

- **Reword a question:** change the text between the quote marks.
- **Add a question:** copy one whole `{ ... },` block, paste it right after another
  one in the same section, and change the words.
- **Delete a question:** delete its whole `{ ... },` block.
- **Rename a section (principle):** change `name: "Equity"` to whatever you want.
- **Change how strict the result is:** change the number in
  `CAUTION_IF_NO_OR_UNSURE_AT_LEAST`. Lower is stricter.
- **Change the result messages:** edit the `MSG_...` lines.

## Rules that prevent breakage

- Keep every piece of text inside straight quote marks `"like this"`.
- If your text needs a quote mark inside it, write `\"` (a backslash then a quote), or use an apostrophe `'` instead.
- Keep the commas at the end of each line and after each closing `}`.
  The last item in a list can have no comma.
- Keep the square brackets `[ ]` and curly braces `{ }` in matching pairs.

## Check your change before you rely on it

1. On GitHub, open the file and click the **Download raw file** icon.
2. Double-click the downloaded file. It opens in your browser.
3. Click through a few answers. If the page shows only the title and no questions,
   something in the edit-here block is missing a quote, comma or bracket.
   Go back to GitHub, open **History**, and revert your last commit, or fix the typo.

## The other checklist

`ai-research-checklist.html` (for judging AI-assisted studies) has its questions in
the section starting `var PRINCIPLES`. The pattern is the same but uses `t:` (question),
`h:` (hint) and `a:` (follow-up) instead of `q`, `hint` and `ask`.

## Note on the private preview links

Editing the file on GitHub changes the repository copy. A private preview link only
changes when the page is republished (ask Claude to republish, or publish the file
again yourself). The downloaded-file check above always shows your latest edit.
