# How to Commit This Project to GitHub

This document outlines the steps taken to commit the `bash-basics` project to GitHub.

## Steps Performed

1. **Initialize Git Repository**

   ```bash
   git init
   ```

2. **Add All Files to Staging**

   ```bash
   git add .
   ```

3. **Commit Changes**

   ```bash
   git commit -m "Initial commit: add hello_world.sh, reference.md, shortcuts.md"
   ```

4. **Add Remote Origin (GitHub Repository)**

   ```bash
   git remote add origin https://github.com/cwhiterite/bash-basics
   ```

5. **Push to GitHub and Set Upstream**
   ```bash
   git push -u origin master
   ```

## Result

- The project is now hosted at: https://github.com/cwhiterite/bash-basics
- The local `master` branch tracks `origin/master`.
- Future changes can be pushed with `git push` and pulled with `git pull`.

## Notes

- Ensure you always have write access to the repository.
- If the repository already exists, you may need to force push or resolve conflicts.
- Consider renaming the default branch to `main` if preferred:
  ```bash
  git branch -m main
  git push -u origin main
  ```
