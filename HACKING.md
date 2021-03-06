SCM
===

 - anonymous checkouts

   `$ git clone git://git.freedesktop.org/git/PolicyKit.git`

 - checkouts if you got an ssh account on fd.o (username@ is optional)

   `$ git clone ssh://[username@]git.freedesktop.org/git/PolicyKit.git`

 - commit to local repository

   `$ git commit -a`

 - push local repository to master repository at fd.o (remember most patches
   requires review at the mailing list)

   `$ git push`

 - pull changes from master repository at fd.o

   `$ git pull`

 - diff of working tree versus local repository

   `$ git diff`

 - diff of local repository vs. master repository at fd.o

   synchronize with upstream repo:
   `$ git pull`

   (possibly merge changes)

   generate the diff:
   `$ git diff origin HEAD`

 - influential environment variables (set these in e.g. .bash_profile)

```bash
   export GIT_AUTHOR_NAME='Your Full Name'
   export GIT_COMMITTER_NAME='Your Full Name'
   export GIT_COMMITTER_EMAIL=youremail@domain.net
   export GIT_AUTHOR_EMAIL=youremail@domain.net
```

 - see also

    http://www.kernel.org/pub/software/scm/git/docs/


Committing code
===

 - Commit messages should be of the form (the five lines between the
   lines starting with ===)

> === **begin example commit** ===
> short explanation of the commit
>
>
>
> Longer explanation explaining exactly what's changed, whether any
> external or private interfaces changed, what bugs were fixed (with bug
> tracker reference if applicable) and so forth. Be concise but not too brief.
> === **end example commit** ===

 - Always add a brief description of the commit to the _first_ line of
   the commit and terminate by two newlines (it will work without the
   second newline, but that is not nice for the interfaces).

 - First line (the brief description) must only be one sentence and
   must not start with a capital letter. Don't use a trailing period
   either.

 - The main description (the body) is normal prose and should use normal
   punctuation and capital letters where appropriate. Normally, for patches
   sent to a mailing list it's copied from there.

 - When committing code on behalf of others use the --author option, e.g.
   ```bash
   git commit -a --author "Joe Coder <joe@coder.org>"

Coding Style
===

 - Please follow the coding style already used.

 - Write docs for all functions and structs and so on. We use gtkdoc format.

 - All external interfaces (network protocols, file formats, etc.)
   should have documented specifications sufficient to allow an
   alternative implementation to be written. Our implementation should
   be strict about specification compliance (should not for example
   heuristically parse a file and accept not-well-formed
   data). Avoiding heuristics is also important for security reasons;
   if it looks funny, ignore it (or exit, or disconnect).

Code of Conduct
===
As with other projects hosted on freedesktop.org, Polkit follows its
Code of Conduct, based on the Contributor Covenant. Please conduct
yourself in a respectful and civilized manner when using the above
mailing lists, bug trackers, etc:

  `https://www.freedesktop.org/wiki/CodeOfConduct`

