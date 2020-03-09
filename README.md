# GIT

```bash
git init

# Cambios y confirmación
git add .
git commit -m "First commit"

# Nuevas ramas
git breach feature
git breach hotfix
git branch
git checkout feature

# Cambios en rama feature, que corresponden a hotfix, se almacenan en stash
git stash save "Changes for hotfix"

# Aplica y remueve el stash sobre hotfix
git checkout hotfix
git stash list
git stash show
# Aplica y remueve el último stash
git stash pop
# Aplica el stash N, pero no lo remueve
git stash apply stash@{N} 
# Remueve un stash N
git stash drop stash@{N}
# Remueve todos los stash
git stash clear
git add .
git commit -m "Repara defecto"

# Merge desde master
git checkout master
git merge hotfix
git show 
# En caso de revertir el merge
git revert <commit id>
# Se repara y confirman cambios en hotfix
git checkout hotfix
git add .
git commit -m "nuevos cambios"

# Merge desde master y se elimina hotfix
git checkout master
git merge hotfix
git branch
git branch -d hotfix
git branch

# Merge desde feature
git checkout feature
# Cambios existentes/nuevos sobre la rama
git add .
git commit -m "Cambios sobre feature"
git merge master
# Solucionan los conflictos
git add .
git commit -m "Merge con master"
# Regresa a mater y merge con feature
git checkout master
git merge feature 
git status
git branch
git branch -d feature
git branch
```
