///////////////////////////////A-create new project///////////////
Add index.html an push remote
     Command:git add .
     Command:git commit -m "initial commit"
     Command:git remote add origin git@github.com:mohamedtarek01141/Lab2.git
     Command:git push origin master
     Resutlt:
             Enumerating objects: 3, done.
             Counting objects: 100% (3/3), done.
             Compressing objects: 100% (2/2), done.
             Writing objects: 100% (3/3), 361 bytes | 45.00 KiB/s, done.
             To github.com:mohamedtarek01141/Lab2.git
             * [new branch]      master -> master

/////////////////////////////B-Craete two branches and push them///////////////////////////////
1-Create branch div and push script.js
      Command:git branch div
      Command:git checkout div
      Commamd: git add .
      Command: git commit -m "add js file"
      Command:git log --oneline
      Result:
             f75be0a (HEAD -> div) add js file
             d4be274 (origin/master, master) initial commit
       Command:git push origin test

2-Create branch test and push style.css
      Command:git branch test
      Command:git checkout test 
      Command:git add .
      Command:git commit -m "add css file"
      Command:git log --oneline
      Result:
             048b43 (HEAD -> test) add css file
             75be0a (master, div) add js file
             d4be274 (origin/master) initial commit
      Command:git push origin test
      Result:
            Enumerating objects: 7, done.
            Counting objects: 100% (7/7), done.
            Delta compression using up to 8 threads
            Writing objects: 100% (6/6), 495 bytes | 495.00 KiB/s, done.
            remote: Resolving deltas: 100% (1/1), done.
            remote:
            remote: Create a pull request for 'test' on GitHub by visiting:
            remote:      https://github.com/mohamedtarek01141/Lab2/pull/new/test
            remote:
             * [new branch]      test -> test

/////////////////////////////////C-merge and push/////////////////////////////
1-Merge div
       
           Command:git checkout master
           Command:git merge div
           Command:git push origin master

2-merge test
           Command:git merge div
           result:
                  Fast-forward
                  1 file changed, 0 insertions(+), 0 deletions(-)
                  create mode 100644 style.css
           Command:git push origin master
           Commamd:git log --oneline --graph
           Result:
                  * c048b43 (HEAD -> master, origin/test, origin/master, test) add css file
                  * f75be0a (origin/div, div) add js file
                  * d4be274 initial commit

/////////////////////////////4-How to remove///////////////////////////
1-Remove locally
          Command:git branch -d div
          Command:git branch -d div
2-remove Remote
          Command:git push origin :div
          Command:git push origin :test

////////////////////////////5-checkout without commit////////////////////
1- git stash
2- git checkout master

////////////////////////////6-create Tag/////////////////////////////

          Command:git tag -a V1.7 -m"add version V1.7"

////////////////////////////7-push Tag///////////////////////////////
          Command:git push --tag
          Result:
                umerating objects: 1, done.
                Counting objects: 100% (1/1), done.
                Writing objects: 100% (1/1), 167 bytes | 167.00 KiB/s, done.
                Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
                To github.com:mohamedtarek01141/Lab2.git
                * [new tag]         V1.7 -> V1.7

//////////////////////////////////8-List Tag/////////////////////////////

      Command:git tag

//////////////////////////////////9-Delele Tag//////////////////////////
1-Delete Locally
          Command:git tag -d V1.7

2-Delete Remote
          Command:git push origin --delete V1.7

//////////////////////////////////10-Add image to REadme file//////////////////////////
using Relativ paths
![My img](images/img1.png)



    