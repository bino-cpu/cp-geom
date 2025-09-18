
# Best practices to keep your work and the repository safe at the end of each session:

## Quick Checklist for Shared Computers
- [x] Commit and push your work to GitHub.
- [x] Remove your repository folder if needed.
- [x] Delete or move your SSH keys if used.
- [x] Unset your Git user/email if set globally.
- [x] Log out of GitHub in all browsers.

1. Remove Your Local Changes (Optional but Safe)
- If you don’t want your local work left behind on the computer:
	- Commit and push your changes to GitHub:
		```bash
		git add .
		git commit -m "Your commit message"
		git push origin main   # or your branch name
		```
	- Delete your local clone (optional):
		```bash
		cd ..
		rm -rf your-repo-folder
		```
2. Clear Your Git Credentials
	- If you used HTTPS and entered your username/password:
		- Clear saved credentials (in Windows Credential Manager or macOS Keychain).
	- If you used SSH:
		- Remove your SSH key from the .ssh folder if you added it temporarily:
			```bash
			rm ~/.ssh/id_ed25519
			rm ~/.ssh/id_ed25519.pub
			```
		- Or move your keys to a USB drive.
3. Unset Git User Identity (Optional)
	- If you set your user.name and user.email globally, reset or unset them:
		```bash
		git config --global --unset user.name
		git config --global --unset user.email
		```
4. Sign Out of GitHub in the Browser
	- Always log out of your GitHub account in any web browsers used on the shared machine.
5. Check for Uncommitted Work
	- Run git status before leaving to ensure you’ve committed and pushed everything you need.
6. Remove Local Repository If Needed
	- If privacy is critical, delete the local repository folder as shown above.

*Clear the Current Session History*
```bash
history -c
```