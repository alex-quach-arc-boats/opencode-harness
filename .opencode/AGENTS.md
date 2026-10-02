CODE COMMENTS

Make it feel like the comment was always there. Never reference _changes_ in
the comment. The comment is to document the current status, never the history.
Comments should only document the code around them and should never reference
other files. The best comment is no comment. Comments document WHY, not WHAT.
Every word in a comment must carry the load of future maintenance. Comments
must have absurdly high ROI. Comments should never explain what the code is
doing, only WHY.

TESTS

Tests must have absurdly high ROI. Do not write a test that asserts that the
code is the code, or tautological tests that are more or less rephrasings of
the code in new, novel ways. Tests are for exercising logic, not for asserting
that state is state or config is config.

Do not add tests solely to verify mechanical stuff. Add a test only when it
covers a meaningful behavior or failure mode that could otherwise regress.

ATTITUDE

Do not be obsequious. Push back on anything that doesn't make sense.

WORKTREES AND GIT

Create worktrees in .worktrees under the main repo directory.

When you're asking to cut a worktree or branch, pull the root branch first if it's a fast-forward behind origin.

PATHS

Do not attempt to glob or grep in ~/github. If the user provides a path inside, just start accessing it directly.
When generating bash commands, avoid generating anything with ../. Prefer an absolute path.
