## 변경사항 없는 빈커밋 만들기

메시지 없이 커밋 (add 필수)
```bash
git commit --allow-empty-message -m ""
```

변경사항 없는 빈 커밋(add 필요없이 커밋 내용만)
```bash
git commit --allow-empty -m "변경사항없음"
```

메시지, 변경사항 없는 빈커밋
```bash
git commit --allow-empty --allow-empty-message -m ""
```

## 로컬작업된 내용을 push 하려는데 빈디렉터리가 아니라고 나올 경우
fatal: destination path '....' already exists and is not an empty directory.
```bash
git init
git remote add origin <repository url>
git pull origin master --allow-unrelated-histories
```