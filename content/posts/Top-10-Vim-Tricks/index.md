---
author: "Pratham Dupare"
title: Top 10 essential Vim Tricks
date: 2024-12-08
description: "Privacy is a fundamental human right, these tools will provide you with that experience."
tags: ["Privacy", "Security"]
thumbnail: "/2022/tools-privacy-security/tools-privacy.jpg"
---

### 1. Jump to Matching Parentheses or Braces

`function matchingBraces() {
  if (true) {
    console.log("Jump between these braces using %");
  }
}`

### 2. Visual Block Editing

#### Use `<C-v>` to select a block of text and edit all rows simultaneously.

`const ock1 = "Edit me!";
const ock2 = "Edit me!";
const ock3 = "Edit me!";`

### 3. Move by Search History

#### Use `/log` to search for "log", then press `n` to move to the next match and `N` for the previous match.

`console.log("Search for this log statement.");
console.log("Another log statement.");`

### 4. Try `ci"` or `di"` to modify or delete the text inside these quotes.

`const greeting = "Change or delete this text.";
const foo = () => {
console.log("Vim is awesome");
};`

### 5. Repeat the Last Command

#### Delete this line using `dd`, then press `.` on the next line to repeat the delete.

`const repeatCommand = "Repeat this delete.";`

### 6. Replace Text Globally

#### Use `:%s/old/new/g` to replace all instances of "old" with "new".

`const oldVariable = "Replace all 'old' instances.";`

### 7. Swap Two Lines

#### Use `ddp` to swap this line...

`console.log("This line should be swapped below...");`

### 8. Increment/Decrement Numbers

#### Place your cursor on the numbers below and press `<C-a>` to increment or `<C-x>` to decrement.

`let number = 40; // Increment or decrement this number.`

### 9. Reformat Code

#### Select this block of code and press `=` to auto-indent it.

`function messyCode() {
const foo = "fjkdj";
}`

### 10. Toggle Case

#### Place your cursor on the text below and press `~` to toggle its case.

`const caseToggle = "Toggle This Case.";`
