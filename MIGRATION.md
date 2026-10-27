# Repository history and development

The six repositories in https://github.com/waling-imis were copied from the corresponding repositories in https://github.com/birendranagar-imis using Git clone and Git push. Original commits retain their authors, dates, and hashes; branches and tags are preserved. Existing licenses and attribution are retained.

| Repository | Default branch | Visibility |
| --- | --- | --- |
| web_app | master | Private |
| mobile_app | main | Private |
| deployment_documentation | master | Public |
| user_manual | master | Public |
| additional_resources | master | Public |
| .github | master | Public |

## Work with a Waling repository

Clone into a new folder, then retain a separate upstream remote for comparison:

```powershell
git clone https://github.com/waling-imis/web_app.git
cd web_app
git remote add upstream https://github.com/birendranagar-imis/web_app.git
git fetch upstream
git log --oneline --graph --decorate --all
```

For another repository, substitute its name. Use main as the base branch for mobile_app and master for the other repositories.

Create a branch for new work, commit, and push to Waling:

```powershell
git switch -c codex/your-change
# Make your changes, then stage only the intended files.
git add path/to/changed-file
git commit -m "Describe your change"
git push -u origin codex/your-change
```

New commits should use the author's own GitHub-linked email. Copying existing history preserves original authorship; it does not reassign other authors' commits to the account performing the push.

The organization overview is maintained in profile/README.md in this repository. Edit, commit, and push that file to update the overview.

This migration copies Git data and repository files. Issues, pull requests, organization membership, teams, repository secrets, and deployment configuration are managed separately in GitHub.