## Amend
커밋 메시지 수정하기
```bash
git commit --amend
```
직전 커밋 메시지를 수정할수 있다
![alt text](image.png)

## Restore
unstaged상태로 되돌린다
```bash
git restore --staged <파일명>  # staged된 특정파일만
git restore --source=(헤드 또는 커밋 해시) 파일명  # 파일을 특정 커밋의 상태로 되돌리기
```

## Reset
```bash
git reset --mixed <커밋아이디> # mixed 생략가능 변경사항은 남기고 unstaged상태로 되돌린다
git reset --soft <커밋아이디>  # 변경사항은 남기고 staged 상태로 되돌린다
git reset --hard <커밋아이디>  # 변경사항까지 되돌린다
```

## Reflog
reset한 내역까지 전부 확인할수 있고 해당 커밋 해시를 입력해서 다시 되돌릴수 있다
```bash
git reflog
git reset --hard <커밋해시>
```

## Revert
변경사항 남기고 되돌아가기
```bash
git revert 커밋아이디
```
커밋하지 않고 Revert하기
```bash
git revert --no-commit (되돌릴  커밋 해시)
```

## HEAD 연산자
```bash
HEAD # 최근커밋
HEAD^ # 최근커밋의 이전 커밋 (^의 갯수만큼 이전으로 이동)
HEAD^^  # 최근커밋의 이이전 커밋
HEAD^^^  # 최근 커밋의 이이이전 커밋
HEAD~n # 최근커밋의 n번째 이전 커밋
```
