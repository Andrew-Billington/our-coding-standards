# Code should be correct, clear, concise - in that order
* Correct means provably correct - with tests (ideally) and / or documented Quality Assurance.  Automated tests are ideal because they allow the code to be refactored with confidence.
* All fixes & new features should include tests to prevent regressions (i.e. reappearance of the bug you just fixed).
* Choose clarity over cleverness - use advanced language tricks with care.
* Don’t Repeat Yourself - The [‘Rule of Three’](https://en.wikipedia.org/wiki/Rule_of_three_(computer_programming)) is a good approach to managing duplication. Less code is usually better - but not at the expense of clarity
* To help with clarity and establish patterns within the team, please use either the [PEP8](https://pypi.python.org/pypi/pep8) style guide (for Python) or [LintR](https://github.com/jimhester/lintr) (for R).  The relavant linters will help you with this.
* Ensure that your tests and linters run automatically on all pull requests by setting up [TravisCI](https://travis-ci.org/) on your repo.