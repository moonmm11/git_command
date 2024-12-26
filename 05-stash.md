## Stash
```bash
git stash push -m "메시지"
```
사라진 내역 확인
```bash
git stash list
```
![alt text](assets/image-stash.png)   

사라진 내역 자세히 확인
```bash
git stash show <stash아이디> -p
```

사라진 내역 가져오기
```bash
git stash apply <stash아이디> # stash 내역은 남기고 가져오기
git stash pop <stash아이디> # stash 내역 삭제하고 가져오기
```

삭제하기
```bash
git stash drop <stash아이디> # 가져오지 않고 삭제
git stash clear # stash 내역 모두 삭제
```

## Cherry Pick
다른 브랜치에 있는 커밋아이디를 입력해 내용을 가져올수 있다
```bash
git cherry-pick 커밋아이디
```
충돌났을경우 그내용과 커밋메시지를 수정할수 있다
```bash
git cherry-pick --continue
```
