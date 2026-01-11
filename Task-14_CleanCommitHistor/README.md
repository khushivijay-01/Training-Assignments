1) Create multiple small commits.
2) Squash them into a single commit.
3) Verify the commit history is clean.

-Determine the number of commits to squash.
    -Use "git log --oneline" to view your recent commits and count how many you want to combine. Let's assume you want to squash the last 3     commits.
    -Start an interactive rebase session.
    -Run the "git rebase -i" command, specifying the commit before the oldest one you want to keep as the base.

    "git rebase -i HEAD~3"

    -This opens a text editor showing the last three commits. The oldest commit is at the top.
    -Edit the rebase instructions.
    -In the editor, the commits will be listed with pick next to them. Change pick to squash (or s) for all commits you want to merge into the previous one. Leave the first (oldest) commit as pick.

    -Save and close the editor.
    -Force push if necessary