gitvimdiff
==========
Invokes vim in diff mode on your git changes, with capability
to navigate across pairs of files.  Typically, the right hand
is editable.

Usage
-----

      $ gitvimdiff [options for git diff]

I commonly use `gitvimdiff --cached`, `gitvimdiff origin/master..`, 
and just `gitvimdiff`.

Then, in vim, use `Ctrl-N`, `Ctrl-P` to navigate to the
next and previous pairs of files.  `Ctrl-A` restarts
at the beginning.  `Ctrl-Q` quits.

Motivation
----------
I run `gitvimdiff` before sending code out for review.  It lets
me see the code in the same way how a reviewer would see it (if
they were using Reviewboard or Mondrian or gerritt or whatever other
side-by-side review tool).  Because the right-hand side is editable,
I typically add comments, fix spelling errors, and do other cleanup
in this last pass.

Note that `git-difftool` calls vimdiff on every pair of files that
change.  Hence, navigating requires you popping out of vim.

Credits
-------
gitvimdiff is based on a hack by by John Reese (jtr@google.com).
Philip Zeyliger adapted it for git.
