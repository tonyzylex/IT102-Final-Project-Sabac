# C-ToolKit

A small menu-based program written in C. It's a bunch of mini tools in one place: a pattern generator, Pascal's triangle, a grade calculator, and a palindrome checker.

## Running it

You need a C compiler (I used gcc).

```
gcc Fp.c -o Fp.exe
./Fp.exe
```

On Windows it's `Fp.exe` instead of `./Fp`.

Heads up: the program calls `system("cls")` to clear the screen, which only works on Windows. If you're on Linux or macOS, change every `"cls"` to `"clear"` or the screen won't clear (it'll just print an error).

## What's in the menu

```
[1] The Pattern Generator
[2] Pascals Triangle
[3] Grade Calculator & Evaluator
[4] Palindrome Checker
[5] Exit program
```

### 1. Pattern Generator

Pick a shape, then type a size. The shapes are:

1. Right triangle
2. Square
3. Isosceles triangle
4. Inverted right triangle
5. Christmas tree (an isosceles triangle with a trunk, the trunk height is half the size)

Size has to be 1 or more.

### 2. Pascal's Triangle

Type how many rows you want and it prints them centered. It uses `long long`, so if you go with a really big number the values will overflow and you'll get garbage. Anything up to around 20 rows looks fine.

### 3. Grade Calculator

Enter four grades (prelim, midterm, pre-final, final), each between 1 and 5. It averages them and tells you if you passed. The grading is the 1.0 to 5.0 style where lower is better, so an average of 3.0 or below is a pass and anything above is a fail.

If you type a letter or a grade outside 1-5, it asks you to start over from prelim.

### 4. Palindrome Checker

Type a word or phrase and it tells you whether it reads the same backwards. It ignores uppercase/lowercase and spaces, so "Never odd or even" counts. It does NOT ignore punctuation though, so something like "A man, a plan, a canal: Panama" will come out as not a palindrome. Input is capped at 99 characters.

## Input handling

Every `scanf` is followed by a loop that clears whatever is left in the input buffer, so typing letters where a number should go won't break the menu. After each tool finishes it waits for you to press Enter before going back to the main menu.

## Created by

Francis Anthony J. Sabac
Harley Hersha Apurado

## Files

- `Fp.c` - the whole program
- `Fp.exe` - the compiled sourced file
- `Documentation` - A folder containing Algoritms, Flowchart, and Psuedocodes
- `.vscode` - A folder containing the configuration set up, in running or debugging the source code
