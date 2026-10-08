# Git Notes

Meri personal Git cheatsheet. Roz ke kaam aane wale commands, examples ke saath.

## Git kya hai?
Git ek **version control system** hai. Ye har change ka record rakhta hai, taaki purane version pe wapas ja sako aur team ke saath bina conflict ke kaam kar sako.
**Git** = tool (laptop pe chalta hai), **GitHub** = website jahan repos online store hote hain.

## Setup (ek baar)
```bash
git config --global user.name "your user name"
git config --global user.email "your-email@example.com"
```

## Basic workflow
```bash
git init                    # naya repo banao
git status                  # kya change hua dekho
git add file.txt            # ek file stage karo
git add .                   # saari files stage karo
git commit -m "message"     # snapshot save karo
git log --oneline           # history dekho
```

## GitHub ke saath
```bash
git clone <url>             # repo download karo
git remote -v               # remote URL dekho
git push origin main        # local commits upload karo
git pull origin main        # latest changes lao
```

## Branching
```bash
git branch                  # branches ki list
git checkout -b feature-x   # nayi branch banao aur usme jao
git merge feature-x         # feature-x ko current branch me milao
git branch -d feature-x     # branch delete karo
```

## Galti sudharna
```bash
git restore file.txt        # unstaged changes hatao
git restore --staged file   # stage se wapas nikalo
git commit --amend          # last commit ka message badlo
git revert <commit-id>      # kisi commit ko undo karo (safe)
git stash / git stash pop   # changes temporarily side me rakho
```

## Good commit messages
- Achha: `Add two-pointer solutions for arrays`
- Bura: `update`, `fix`, `abc`

## Common mistakes
- `git add .` se pehle `git status` check karo, nahi to galti se `.env` jaisi secret files push ho jaati hain.
- `.gitignore` me wo files likho jo repo me nahi chahiye.

## Aage seekhna hai
- [ ] rebase vs merge
- [ ] Pull Request workflow
- [ ] Merge conflict resolve karna
