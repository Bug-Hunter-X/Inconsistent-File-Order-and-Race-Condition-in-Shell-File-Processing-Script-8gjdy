# Shell Script File Processing Bug

This repository demonstrates a subtle bug in a shell script that processes files in a directory. The script uses `find` and `while` loop to process files, and it's vulnerable to race conditions and inconsistent file ordering across systems.

## Bug Description
The script processes files based on their position in the output of the `find` command, which can vary across different systems and even between runs on the same system. This leads to two key issues:

1. **Inconsistent File Order:** Files may not be processed in the intended order.
2. **Race Conditions:** If files are added or removed from the directory while the script is running, it might lead to unexpected behavior or errors.

## Bug Solution
The solution addresses these issues by employing a more robust method to process files, ensuring consistency and avoiding race conditions.