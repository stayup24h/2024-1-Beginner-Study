## git log
- commit 기록을 최신순으로 확인 <br/>
- ```--oneline``` 옵션을 사용하면 각 커밋을 한 줄에 요약

## Commit Id

- commit의 식별을 위해 사용하는 40자 길이의 16진수 <br/>
- SHA-1 해시 함수를 사용해 중복 확률은 1/2^80

## Head
- 현재 작업중인 위치 <br/>
- 현재 작업중인 브랜치의 가장 최근 commit <br/>
- 다음 commit의 base가 되는 commit <br/>
- 새로운 commit이 생기면 HEAD도 변경 
## git status
- Untracked <br/>
- Staged <br/>
- Modified <br/>

## commit --amend
- 마지막 commit의 내용에 변경이 있을 때 사용 <br/>
- 완전히 새로운 commit으로 대체 <br/>
- vim 으로 진입하여 commit message를 수정
```bash
    $ git commit --amend -m "<commit message>"
    # '-m' option으로 vim 진입 없이 commit message 수정

    $ git commit --amend --no-edit
    # '--no-edit' option으로 commit message 수정 없이 commit 수정
```
## reset
``` bash
    $ git reset --soft "<commit id>"
    #커밋만 취소

    $ git reset --mixed "<commit id>"
    # 커밋을 취소
    # 변경 사항을 workin directory로 돌아감

    $ git reset --hard "<commit id>"
    # 커밋을 취소
    # 변경사항을 모두 제거하고 이전 커밋으로 돌아감
```
## revert
- commit을 제거하지 않고 되돌림 <br/>
- 되돌리기 위한 새로운 commit이 생성됨<br/>
``` bash
    $ git revert --edit "<commit id>"
    # default

    $ git revert --no-edit "<commit id>"
    # 편집기 진입 없이 바로 revert 가능
    # 바로 commit 하지 않고 revert 내용을 Staging Area에 올림
```