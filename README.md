## Git Lab 2: Step-by-Step Walkthrough

Here is the refined, step-by-step guide for your lab with each command on its own line for better clarity and reliability.

### Step 1: Create Project & Push to Remote

* Initialize your local repository.
* Create a starting file.
* Link and push to your remote server.

```bash
mkdir Git-Github-Labs
cd Git-Github-Labs
git init
echo "Test" > README.md
git add README.md
git commit -m "Initial commit"
git remote add origin <REMOTE_URL>
git push -u origin main

```

### Step 2: Create `dev` Branch, Add File, & Push

* Create and switch to a new branch for development.
* Add a specific file to track progress on this branch.

```bash
git checkout -b dev
echo "#/bin/bash " > test
git add .
git commit -m "Add dev file"
git push -u origin dev

```

### Step 3: Create `test` Branch, Add File, & Push

* Switch back to the main branch before creating the next branch.
* Create and switch to a test branch.

```bash
git checkout main
git checkout -b test
echo "#!/usr/bin/env python3 " > testx
git add .
git commit -m "Add test file"
git push -u origin test

```

### Step 4: Merge to Main & Push

* Switch back to the `main` branch to receive the changes.
* Merge the work from both `dev` and `test`.

```bash
git checkout main
git merge dev
git merge test
git push origin main

```

### Step 5: Remove Branches (Locally & Remotely)

* Clean up your repository after the merge is complete.

```bash
# Delete locally
git branch -d dev
git branch -d test

# Delete remotely
git push origin --delete dev
git push origin --delete test

```

### Step 6: The `git stash` Command

Use this when you have uncommitted work but need to switch branches urgently.

```bash
git stash
git checkout <other-branch>

# To get your work back later:
git stash pop

```

---

### Step 7: Create Annotated Tag & Push

* Tag a specific point in history (like a release) with metadata.

```bash
git tag -a v1.9 -m "Version 1.9 tag"
git push origin v1.9

```

### Step 8: List & Manage Tags

* View all tags or delete them if a mistake was made.

```bash
# List all tags
git tag

# Delete locally
git tag -d v1.9

# Delete remotely
git push origin --delete v1.9

```

### Step 9: Add an Image in README.md

* Update your documentation by adding the Markdown image syntax to your `README.md`.

![Dahab](https://dahabsafari.com/wp-content/uploads/2019/11/bluehole-768x544.jpg)


```

Would you like me to add a section on how to resolve merge conflicts if two branches change the same file?
