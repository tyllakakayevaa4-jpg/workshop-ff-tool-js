
# FindFirst (ff.js) Command-Line Tool

## Section 1 - Command Description

**What your tool does:**
ff.js (Find First) is a custom Node.js command-line utility. It looks for specific text pattern strictly within the first N lines in a given file. If the pattern is found within that line limit, the script prints the matching lines to the terminal.

**How to run it:**
Use Node.js to execute the script in the terminal. The script requires three arguments in this exact order: the pattern to search for, the file name, and the number of lines to scan.

\`\`\`bash
node ff.js <PATTERN> <FILENAME> <NUMBER_OF_LINES>
\`\`\`
*Example:* node ff.js "Error" sample_log.txt 10

**What commands it combines:**
This tool combines the functionality of two standard Linux commands:
1. head: which extracts the first N lines of a file.
2. grep: which searches for and prints lines containing a specific pattern.
In a traditional Linux terminal, the similar/same piped command would be: document.

---

## Section 2 - AI‑Assisted Programming

**What I asked AI:**
During this workshop, I used AI to explain the standard Linux grep and head commands to understand the behavior I needed to replicate. I also asked the AI to generate a sample log file for testing, suggest robust test cases, point out edge cases, and provide the terminal steps to create and push to a GitHub repository.

**Where AI helped:**
The AI was extremely helpful because it showed a structured set of test cases to verify standard matches, out-of-range matches, and multiple matches. It also helped me identify edge cases I needed to test(such as case sensitivity issues, passing zero or negative numbers for the line count, handling empty files).

**Where I had to think independently:**
I had to write the commands myself. I structured the arguments by myself, set up the error handling for missing arguments or files during the class, and used the core logic used in JS. I also needed figure out how to bound the search loop using a ternary operator so the script would not crash if the user asked to search more lines than the file actually contains.
 
**What AI got wrong or missed?**
AI first assumed the command line arguments were in a different order which did not really match my code's Create the READstructure, so I had to correct its usage examples. Actually, AI did not miss much, but I had to manually fix a syntax error it did not catch in my loop.