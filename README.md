# Fun with Regular Expressions - CSCI 3501

*Lab by Ken Broden*

## Synopsis

### Task 1: Java Regular Expressions (21 points)

Study the Java regular expressions tutorial (ignore the Test Harness section, we use our own testing class). Instead of using the `Pattern` and `Matcher` classes directly, you will be using `RegExTester.java` which provides methods for searching, splitting, and replacing strings based on regular expressions. Study examples in the `main` method of that class.

Important: By default, regular expressions will find a matching sequence within the given input; they do not match the entire input. For instance, a regular expression "DFA" will find a match in an input "DFAs are cool".

Also important: Java strings use `\` as a special character. Therefore, you need `\\` for predefined regex classes, e.g., `\\d+` matches one or more digits.

Your tasks are as follows (assume case-insensitive matches unless specified otherwise):

1. Find all occurrences of letter combinations "dfa" and "nfa" in a text.
2. Find all integer numbers (i.e., sequences of digits with no other characters) in a text. Use a predefined class `\d` to match a single digit.
3. Find all negative integer numbers, i.e., numbers preceded by a `-` sign.
4. Find all words that start with a letter `t`.
5. Find all words in a text that have letters `t` and/or `i` in them (in any order).
6. Use the `doRegExSplit` method to split a string into items separated by `|`.
7. Use the `doRegExReplace` method to replace all occurrences of "today" with "yesterday".

Submit your code (some method calls may be commented out) and a copy of your test data for each regular expression (as a separate file or in comments).

### Task 2: Convert Regular Expressions to an NFA (6 points)

In this task, you will convert the given regular expressions to Non-deterministic Finite Automata (NFA) using the JFLAP tool. Follow the tutorial on Regular Expressions and Converting to an NFA. Note that JFLAP uses `+` for union and `*` for the star operation. Ensure that parentheses are set correctly in your expressions.

JFLAP provides hints and a "(De)-expressionify Transition" button to break down regular expressions into smaller subexpressions. Add empty transitions to complete each step. As you convert a regular expression to an NFA, write down the intermediate expressions as notes on the JFLAP screen. Use the selection tool, right-click on the JFLAP screen, and choose "add note" to document each step.

Convert the following regular expressions to NFAs:

1. `((0+1)0)*`
2. `(00)*+(10)*`

Export and submit your NFAs. Results can be found in `Broden_Task2_Part1.png` and `Broden_Task2_Part2.png`.
