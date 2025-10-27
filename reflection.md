Reflection

1. Which issues were the easiest to fix, and which were the hardest? Why?

Easiest: Removing eval() and replacing print() with logging — these were simple, one-line fixes.

Hardest: Handling the mutable default argument (logs=[]) and removing the global keyword. These required refactoring and understanding how data was shared between functions.

2. Did the static analysis tools report any false positives? If so, describe one example.

Yes, Flake8 flagged a long comment line as a style issue, even though it didn’t affect functionality. This was more of a formatting preference than an actual problem.

3. How would you integrate static analysis tools into your actual software development workflow?

I would integrate Pylint, Flake8, and Bandit into a GitHub Actions CI pipeline so they automatically check every commit or pull request. Developers can also run them locally before pushing changes.

4. What tangible improvements did you observe in the code quality, readability, or potential robustness after applying the fixes?

The code became cleaner, safer, and easier to maintain.

Logging improved traceability, exception handling became more specific, and removing risky patterns (like eval and bare except) made the program more robust and secure.
