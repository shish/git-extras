Shish's Git-Extras
~~~~~~~~~~~~~~~~~~

A few hacky third-party commands for git


git-autotag <target commit ID> "<message>"
------------------------------------------
Generate an auto-incrementing tag with the given message.

Tags are in the format mm00000 .. mm99999

As part of the github-flow model, this can be run in a post-merge-to-master
hook to easily keep track of previous release versions.


git-bare-merge <merge-to> <merge-from>
--------------------------------------
Do a merge in a bare repo.

(By checking out files into a temporary area, then attempting a merge there)


git-merge-status
----------------
List the mergability (already merged, mergable, conflicting) of feature
branches, eg

                      master
                      ~~~~~~
feature/more_pies     clean
feature/kittens       conflict
bugfix/fewer_beans    merged

Also has JSON output, to be used in eg a web-based merge manager tool.
