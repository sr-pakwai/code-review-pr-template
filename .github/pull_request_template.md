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
- [] Is it secure/free from risk? If unsure, have a threat modeling discussion.
- [] Are external inputs validated and sanitized?
- [] Is the logic involves in sensitive, confidential, or personal information?
    - [] Check the logs to ensure those are not leaking.
    - [] Error handling for those hotspots is handled properly to prevent accidental leaks.
- [] Is the page/API only allowed for specific user groups and permissions?
    - [] Ensure that it is protected with proper authentication or authorization.
    - [] Include the security test such as edge case.
- [] Is this an auditable event, such as logins, failed logins, and high-value transactions? If yes, make sure they are logged.
- [] Are you introducing any new library?
    - [] Ensure that the license met our legal requirement.
    - [] Ensure that the license is safe to use. Eg. they are from a well-known and reliable source.

## Documentation
Ensure that the changes are documented properly, including inline code comments and updates to any user-facing documentation.
- [] Does the change worthy of an ADR? If yes, create an ADR.
- [] Does the change affect existing documentation? If yes, update the docs.
- [] Does the change affect the pipeline? If yes, update your README.

## Performance
Check for any performance issues related to the changes, including potential bottlenecks or unnecessary resource usage.
