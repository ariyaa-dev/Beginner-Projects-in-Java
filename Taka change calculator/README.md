# Taka Change Calculator

A beginner project that takes an amount in Bangladeshi Taka (৳) and shows the fewest notes and coins needed to make that amount.

It comes in two versions:

- **Java (console):** `Main.java`, run in the terminal.
- **Web (browser):** `index.html`, a pink-themed page with the same logic written in JavaScript.

## How it works

The program starts with the largest note and works down:

1. Divide the amount by the note value to get how many of that note are needed.
2. Use the remainder (`%`) as the new amount.
3. Repeat for the next smaller note until nothing is left.

Example for ৳1375: 1375 / 1000 = 1 note, remainder 375. Then 375 / 500 = 0 notes, remainder 375. Then 375 / 200 = 1 note, remainder 175. This continues down to ৳1.

Supported denominations: ৳1000, ৳500, ৳200, ৳100, ৳50, ৳20, ৳10, ৳5, ৳2, ৳1.

## Run the Java version

You need the JDK installed (Java 8 or newer).

```
javac Main.java
java Main
```

### Sample output

```
Enter your total amount in (taka):
1375
1000: 1
500: 0
200: 1
100: 1
50: 1
20: 1
10: 0
5: 1
2: 0
1: 0
```

A negative amount prints an error message instead of a result.

## Run the web version

Double-click `index.html` to open it in any browser, type an amount, and click **Break it down**. Only the notes and coins that are needed are shown as tiles, with the total count underneath.

## Project structure

```
taka-change-calculator/
├── Main.java    # Java console version
├── index.html   # Web version (HTML, CSS, JavaScript)
└── README.md
```

## Concepts used

- **Java:** variables, `Scanner` input, integer division (`/`), the remainder operator (`%`), and `if / else`.
- **Web:** HTML structure, CSS styling (flexbox and grid), and basic JavaScript with a loop over the denominations.

## What I'd improve next

- Replace the repeated blocks in `Main.java` with an array and a loop once I learn arrays.
- Add a loop so the user can calculate several amounts without restarting the program.
- Handle non-numeric input without the program crashing.