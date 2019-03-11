# Git Commands

### Git 명령어 모음

`
git commit
git commit --amend : 커밋 내용 정정
git checkout [branch/tag명] : 해당 [branch/tag명]으로 이동
git merge <A> :  현재 branch로 해당 <A> 병합
git branch <A> : branch <A>생성
git branch -f <A> : branch<A>를 현재 branch로 강제 이동
git branch -f <A> <B> : A브런치를 B브런치로 이동
git reset [branch명] : 로컬상에서 없던일로 되돌림
git revert [branch명] : remote에 push됨
git cherry-pick <C2 C4> : 개별 커밋을 골라서 HEAD위에 떨어뜨림(복수개 커밋 복사)
(C2와 C4 내용을 현재 브런치로 복사함)
git rebase -i HEAD~4 : 현재 브런치를 HEAD의 상위 4번째로 붙여넣기 한다.
(단 -i 옵션으로 인하여 바로 옮겨지지 않고 rebase할 commit을 선택하고 순서를 변경하여 rebase 한다.)
git rebase <A> <B> : A브런치에 B브런치를 rebase
git tag <태그명> : 현재 위치에 해당 <태그명>으로 태그생성
git tag <태그명> <커밋> : 해당 <커밋>(해시)에 <태그명>으로 태그 생성
git describe <ref:브랜치명>: 커밋 히스토리에서 앞 뒤로 여러 커밋을 이동하고 나서 커밋 트리에서 방향감각을 다시 찾느데 도움을 줌.
(<ref>에는 commit을 의미하는 그 어떤것을 쓸 수 있음)
명령어 출력결과: <tag>_<numCommits>_g<hash>, <tag>는 가장 가까운 부모 태그, <numCommits>는 얼마나 멀리 있는지, <hash>는 묘사하고 있는 커밋의 해시(부모의 커밋이 아님)
git bisect : 문제가 되는 커밋을 찾는 명령어
git fetch : 원격 저장소의 commit들을 로컬로 받아옴(하지만 로컬 master branch에 반영이 되는 것은 아님, merge를 별도로 해야함)
git pull : fetch + merge
git pull --rebase : pull + rebase
git checkout -b <A> <origin> : <A>라는 새 브런치 생성, origin을 추적하게 설정
git branch -u <origin> : 현재 브런치가 <origin>을 추적하도록 함.
git branch -u <origin> <A> : <A>라는 브런치가 <origin>을 추적하도록 함.
git push orgin <palce> : master
git push origin <source>:<destination>
git fetch origin <source>:<destination> : 원격저장소의 <source>를 로컬저정소의 <destination>으로 가져온다.
git push origin :<A> : 원격저장소의 <A>에 아무것도 없는 걸 push한다. 즉 원격저장소에 <A>브런치를 제거.
git fetch origin :<A> : 원격저장소에서 아무것도 없는걸 fetch한다. 즉 로컬저장소에 <A>브런치 생성
`

### Git Practice Site
 - https://learngitbranching.js.org/
