# Git과 GitHub 이해하기
* add, commit, push
* pull, fetch
 - pull => 다운과 병합(merge)을 한번에 한다
 - fetch => 다운만 한다, 비교(diff) 후 merge 를 따로 해주어야 한다

* stash
 - 수정한 내용을 다른 곳에 저장해 두기
$ git stash save "리스트기능"
$ git stash list
$ git stash apply 
$ git stash apply stash@{0}
$ git stash drop 
$ git stash drop stash@{0}

* revert
 - 커밋한 내용을 되돌리기 (이력을 남기면서)
$ git revert HEAD // 가장 최근에 한 커밋을 되돌리기
HEAD^,  HEAD~1 (commit before HEAD)
HEAD~2 (two commits before HEAD)

* reset
 - 커밋한 내용을 되돌리기 (이력을 남기지 않음)
$ git reset --hard HEAD~1 # 커밋이력 없어지고, code도 원래대로 되돌려짐
$ git reset --soft HEAD^ # 커밋이력 없어지고, code는 되돌리지 않는다
