## Title
Include the work (backlog) ticket number. And a summary of this PR.

## Description
Provide a clear and concise description of the changes being made, the reasoning behind the changes, and any potential impacts or risks.

## Code changes
Include a summary of the code changes being made, including any new code, modified code, or removed code.

## Testing
Specify the tests that have been run and the results, and any new tests that have been added.

## Security
Consider any security implications of the code changes, including potential vulnerabilities or exposure of sensitive data.
- [] Is it secure/free from risk? If unsure, have a threat modelling discussion.
- [] Are external inputs validated and sanitised?
- [] Is the logic involves sensitive, confidential, or personal information?
    - [] Check the logs to ensure those are not leak.
    - [] Error handling for those hotspot is handled properly to prevent accidental leak.
- [] Is the page/api only allow for specific permission?
    - [] Ensure that it is protected with proper authentication or authorization.
    - [] Include the security test such edge case.
- [] Is this an auditable event, such as logins, failed logins, and high-value transactions? If yes, make sure they are logged.

## Documentation
Ensure that the changes are documented properly, including inline code comments and updates to any user-facing documentation.
- [] Does the change worthy of an ADR? If yes, create an ADR.
- [] Does the change affect existing documentation? If yes, update the docs.
- [] Does the change affect the pipeline? If yes, update your README.

## Performance
Check for any performance issues related to the changes, including potential bottlenecks or unnecessary resource usage.
