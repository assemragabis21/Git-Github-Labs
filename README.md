#### **Part 1: Branches & Merging**

**1. Create Project & Push to Remote**

```bash
mkdir lab2 && cd lab2
git init
echo "# Lab 2" > README.md
git add README.md
git commit -m "Initial commit"
git remote add origin <REMOTE_URL>
git push -u origin main

```

**2. Create `dev` & `test` Branches, Add Files, Push**

```bash
# Dev branch
git checkout -b dev
touch dev_file.txt
git add . && git commit -m "Add dev file"
git push -u origin dev

# Test branch (branching off main)
git checkout main
git checkout -b test
touch test_file.txt
git add . && git commit -m "Add test file"
git push -u origin test

```

**3. Merge to Main & Push**

```bash
git checkout main
git merge dev
git merge test
git push origin main

```

**4. Remove Branches (Locally & Remotely)**

```bash
# Delete locally
git branch -d dev test

# Delete remotely
git push origin -d dev test

```

**5. Checkout Another Branch Without Committing**
Use `git stash` to temporarily save your uncommitted work so you can switch branches cleanly.

```bash
git stash
git checkout <other-branch>

# When you come back, restore your changes:
# git stash pop

```

---

#### **Part 2: Tags & Documentation**

**1. Create Annotated Tag & Push**

```bash
git tag -a v1.9 -m "Version 1.9 tag"
git push origin v1.9

```

**2. List Tags**

```bash
git tag

```

**3. Delete Tag (Locally & Remotely)**

```bash
# Delete locally
git tag -d v1.9

# Delete remotely
git push origin --delete v1.9

```

**4. Add an Image in README.md**
Open your `README.md` file and drop in the markdown format (using your Dahab picture as the perfect example!):

![test](https://dahabsafari.com/wp-content/uploads/2019/11/bluehole-768x544.jpg)

