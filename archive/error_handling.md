# Everything fails at some point
Accept this and code defensively when calling other services.
Every HTTP call could error or hang - handle failures appropriately and fail fast. Don’t let long-running external calls impact your user experience.
Aim to provide useful information to end users and people working on the code, when something fails.
