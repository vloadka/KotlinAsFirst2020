git clone https://github.com/vloadka/KotlinAsFirst2020.git 
cd KotlinAsFirst2020  
git remote add upstream-my https://github.com/vloadka/KotlinAsFirst2021.git  
git fetch upstream-my  
git checkout -b backport  
git cherry-pick d535f359...FETCH_HEAD  
git remote add upstream-theirs https://github.com/ChaVi6/KotlinAsFirst2021.git  
git fetch upstream-theirs  
git checkout master  
git merge backport upstream-theirs/master  
git add -A  
git merge --continue  
git remote -v  
git remote -v > remotes  
git add *  
git commit -m "test"  
git push  
git touch howto.md  
git add *  
git commit -m "howto"  
git push  
