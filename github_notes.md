# Notes on using github

- `git log --oneline`
- reset to previous commit and delete current commit (not pushed)
    `--hard HEAD^`
- previous commit to new branch
    `git checkout -b old-state 4879e01` old-state is the new branch, then commit id
- Fix previous commit message not pushed
    `git commit --amend -m "amended message"`

- Merge to main
    `git checkout main`
    `git pull origin main`
    `git merge oldBranch`
    `git push origin main`