# My HackerRank Python Practice

![Python](https://img.shields.io/badge/Python-3.13-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

**Karim Elawadi**
A personal collection of solved Python exercises and coding challenges, built as part of an ongoing path toward Data Science and Machine Learning. This repository serves as both a practice log and a portfolio artifact, documenting steady progress from language fundamentals through functional programming patterns.

## Table of Contents

- [About This Repository](#about-this-repository)
- [Repository Structure](#repository-structure)
- [Topics Covered](#topics-covered)
- [Complete Notebook Index](#complete-notebook-index)
- [Techniques & Patterns Practiced](#techniques--patterns-practiced)
- [Environment & Setup](#environment--setup)
- [Notes on Approach](#notes-on-approach)

## About This Repository

Each notebook targets a specific Python concept and includes a solved exercise with example input/output. Where relevant, exercises are annotated with explanations of *why* an approach works, not just *that* it works — including a few side-by-side comparisons of a naive solution versus an optimized one (see the [Optimization](#optimization-writing-efficient-code) section below).

A recurring stylistic choice across several notebooks — particularly `Workshop.ipynb` — is the deliberate use of the **immediately-invoked lambda expression (IIFE) pattern**, `(lambda x: expression)(x)`, inside list and dictionary comprehensions. This was practiced intentionally to build fluency with `lambda` syntax and scoping rules, even in cases where a plain comprehension would be simpler in production code.

## Repository Structure

```
HackerRank/
├── Workshop.ipynb                          # Core lambda/comprehension practice set
├── Assignamet-1.ipynb                      # Manual sort + string repetition
├── Assignment-2.ipynb                      # List slicing + dictionary updates
├── Python_Introduction.ipynb               # Language basics
├── Python_Basic_Data_Types.ipynb           # Lists, nested lists, tuples
├── Python_Strings.ipynb                    # String manipulation
├── Python_Sets.ipynb                       # Set theory operations
├── Python_Collections.ipynb                # collections.Counter
├── Python_Built-Ins.ipynb                  # zip(), eval()
├── Python_Functionals.ipynb                # lambda + map()
├── Python_Closures_and_Decorators.ipynb    # Decorator patterns
├── Python_Errors_and_Exceptions.ipynb      # try/except, regex validation
├── Python_Regex_and_Parsing.ipynb          # Pattern matching, matrix decoding
├── Python_Math.ipynb                       # pow(), divmod(), complex numbers
└── README.md
```

## Topics Covered

### Strings: Text Processing Fundamentals
**File:** `Python_Strings.ipynb`

Strings are fundamental sequences of characters used to represent and manipulate text data. This section covers substring counting, case swapping, split & join operations, string validation methods (`isalnum`, `isalpha`, `isdigit`, `islower`, `isupper`), in-place-style mutation (via slicing, since strings are immutable), text wrapping, and word capitalization.

### Lists: Organizing and Managing Collections
**File:** `Python_Basic_Data_Types.ipynb`

Lists are ordered, mutable collections central to everyday Python work. This section covers the full range of built-in list operations (`append`, `insert`, `remove`, `sort`, `pop`, `reverse`), nested list structures, tuple hashing, identifying runner-up values in a dataset, and computing percentages/averages from parsed input.

### Sets: Unique Elements and Fast Lookups
**File:** `Python_Sets.ipynb`

Sets are unordered collections optimized for uniqueness and membership testing. This section covers union, intersection, difference, and symmetric difference operations, in-place set mutations (`update`, `intersection_update`, etc.), subset/superset validation, and applied problems such as computing distinct averages and solving allocation-style logic puzzles.

### Dictionaries: Key-Value Relationships
**File:** `Workshop.ipynb`

Dictionaries model key-value relationships with O(1) average-time lookup. This section's core exercise inverts a dictionary — swapping keys and values — implemented via a dict comprehension that pairs a `(value, key)` tuple returned from a lambda, then reassembles the result with `dict(...)`.

### Tuples: Immutable Sequences
**File:** `Workshop.ipynb`

Tuples are ordered, immutable sequences — ideal when data shouldn't change after creation. This section covers the standard round-trip: converting a tuple to a list, targeting a specific index for modification using `enumerate` paired with a conditional lambda, and converting the result back to a tuple.

### Functions: Reusable Code Blocks
**Files:** `Python_Introduction.ipynb`, `Workshop.ipynb`, `Python_Closures_and_Decorators.ipynb`

Functions are the primary unit of reuse in Python. This section spans basic function definitions with parameters and return values (e.g. a leap-year checker), two functions built around list/dict comprehensions with lambda-based logic (`is_palindrome`, `count_occurrences`), and a closures/decorators exercise that wraps and reformats phone number output.

### While Loops: Repetition and Control Flow
**File:** `Workshop.ipynb`

`while` loops repeat based on a condition rather than a fixed range, which makes them well-suited to problems where the number of iterations isn't known in advance. This section's exercise accumulates numbers into a list until their running total exceeds a threshold, demonstrating correct loop-condition design and variable updates to avoid infinite loops.

### Optimization: Writing Efficient Code
**File:** `Workshop.ipynb`

This section is a direct case study in algorithmic efficiency: a straightforward `remove_duplicates` implementation using `if item not in list` (average O(n) per check, O(n²) overall) is compared against an optimized version using a `set` for membership tracking (average O(1) per check, O(n) overall). The comparison illustrates why data structure choice matters more than micro-optimizations as input size grows.

### Advanced Dictionaries: Complex Data Structures
**Files:** `Workshop.ipynb`, `Assignment-2.ipynb`

This section goes beyond flat key-value pairs: building a dictionary that maps each unique word to its index positions using `enumerate`, updating a salary dictionary from a separate list of `(id, percentage)` increment tuples with conditional existence checks, and counting item occurrences with a dynamically added "target" key.

## Complete Notebook Index

| Notebook | Core Topics |
|---|---|
| `Python_Introduction.ipynb` | Hello World, arithmetic operators, division, if-else, loops, functions, formatted output |
| `Python_Basic_Data_Types.ipynb` | List operations, nested lists, tuples & hashing, runner-up scores, percentage calculations |
| `Python_Strings.ipynb` | Substring counting, case swapping, split & join, string validation, mutation, text wrapping |
| `Python_Sets.ipynb` | Union, intersection, difference, symmetric difference, mutations, subset/superset checks |
| `Python_Collections.ipynb` | `collections.Counter` for counting and inventory-style problems |
| `Python_Built-Ins.ipynb` | `zip()`, `eval()` |
| `Python_Functionals.ipynb` | Lambda functions with `map()`, Fibonacci sequence generation |
| `Python_Closures_and_Decorators.ipynb` | Building decorators (phone number formatting example) |
| `Python_Errors_and_Exceptions.ipynb` | `try`/`except` handling, regex validation with error handling |
| `Python_Regex_and_Parsing.ipynb` | Matrix-based string decoding using regular expressions |
| `Python_Math.ipynb` | `pow()`, `divmod()`, complex numbers, angle/coordinate calculations |
| `Assignamet-1.ipynb` | Manual list merge & sort (no built-in `sort()`), string repetition without `if` |
| `Assignment-2.ipynb` | Filtering products by price threshold, updating salaries from increment tuples |
| `Workshop.ipynb` | Vowel counting, list doubling, set operations, dict swap, tuple mutation, palindrome check, occurrence counting, while-loop accumulation, duplicate removal, word-index mapping |

## Techniques & Patterns Practiced

- **Core data structures** — lists, tuples, sets, dictionaries, and their trade-offs
- **String processing** — parsing, formatting, and validating text
- **Functional programming** — `lambda`, `map()`, `filter()`, list/dict comprehensions, and the IIFE pattern (`(lambda x: ...)(x)`)
- **Control flow** — `for`/`while` loops, conditional expressions, ternary logic
- **Error handling** — `try`/`except` for robust, defensive input handling
- **Algorithmic efficiency** — comparing brute-force vs. optimized approaches (e.g., list vs. set membership checks) and reasoning about time complexity
- **Closures & decorators** — wrapping function behavior without modifying the original function

## Environment & Setup

- **Language:** Python 3.13
- **Interface:** Jupyter Notebook (also compatible with VS Code + Jupyter extension)

To run these notebooks locally:

```bash
pip install jupyter
jupyter notebook
```

## Notes on Approach

Where an exercise explicitly requires avoiding a built-in (e.g., implementing sort manually, or solving without `if` statements), the solution respects that constraint even when a shorter built-in alternative exists — the goal is demonstrating underlying mechanics, not just producing the shortest correct output.

## Key Takeaways

This repository reflects steady progress through Python fundamentals: solid command of core data structures (strings, lists, sets, dictionaries, tuples), control flow (functions, loops), and an emerging awareness of algorithmic efficiency. Continued practice — particularly with functional patterns and time-complexity trade-offs — remains an ongoing focus.

## Contact

**Karim Elawadi**

- **Email:** [hamedkarim343@gmail.com](mailto:hamedkarim343@gmail.com)
- **LinkedIn:** [linkedin.com/in/karim-elawadi](https://www.linkedin.com/in/karim-elawadi)
- **HackerRank:** [hackerrank.com/profile/hamedkarim343](https://www.hackerrank.com/profile/hamedkarim343)
