## Title
Include the work (backlog) ticket number. And a summary of this PR.

## Description
Provide a clear and concise description of the changes being made, the reasoning behind the changes, and any potential impacts or risks.

## Code changes
To help your reviewer quickly gain context and visualize the output.
- [] Include a summary of the code changes being made, including any new code, modified code, or removed code.
- [] Include a screenshot of the important change.
- [] Include sample data of input or output if exists.

## Testing
Specify the tests that have been run and the results, and any new tests that have been added.
- [] Did the test covers all the happy path, tested during the development stage?
- [] Are the tests stateless?

## Security
Consider any security implications of the code changes, including potential vulnerabilities or exposure of sensitive data.
- [] Is it secure/free from risk? If unsure, do a threat modeling.
- [] Is the implementation have an exclusive bypass or backdoor access? *If yes, remove them.*
- [] Is the implementation using secret environment variables?
    - [] Ensure that the variables aren't logged.
    - [] Will the logic work if the secret is rotated? *If no, do something about it, else document it properly.*
- [] Is the implementation protected against the [OWASP Top 10](https://owasp.org/www-project-top-ten/)?
- [] Are external inputs validated and sanitized?
- [] Is the logic involves in sensitive, confidential, or personal information?
    - [] Check the logs to ensure those are not leaking.
    - [] Error handling for those hotspots is handled properly to prevent accidental leaks.
- [] Is the page/API ONLY allowed for specific user groups and permissions?
    - [] Protected with proper authentication or authorization method.
    - [] Include the security (regression) test such as the edge case.
- [] Is this an auditable event, such as logins, failed logins, and high-value transactions? *If yes, make sure they are logged.*
- [] Is the log printed on the proper log level? *If yes, does it provide enough information for debugging?*
- [] Are you introducing any new library or framework?
    - [] Understand and comply with the license terms.
    - [] Ensure that the license is safe to use. *Eg. they are from a well-known and reliable source.*

## Documentation
Ensure that the changes are documented properly, including inline code comments and updates to any user-facing documentation.
- [] Does the change worthy of an ADR? *If yes, create an ADR.*
- [] Does the change affect existing documentation? *If yes, update the docs.*
- [] Does the change affect the pipeline? *If yes, update the README.*

## Performance
Check for any performance issues related to the changes, including potential bottlenecks or unnecessary resource usage.
- [] Does the [Big-O](https://www.bigocheatsheet.com) exceed the O(n^2) of complexitiy? *If yes, improve the implementation.*
- [] Does the input/variable need to handle large sizes of data (> 100,000 records)? *If yes, break it into smaller processes.*
- [] Does the implementation has a long processing time or wait time (> 3 secs)? *If yes, does it have a loader in place?*
- [] Does the implementation use up too much temp storage or collect garbage dump? *If yes, improve the implementation.*
