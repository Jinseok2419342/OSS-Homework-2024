# Git 임시 저장(Stash) 요약

## 실습 
1. 파일 f가 3 영역이 모두 다르고 추적되지 않은 파일 g도 생성

`$ echo 111 > f`  
`$ git add f`  
`$ git commit -m A`  
`$ echo 222 >> f`  
`$ echo aaa > g`  
`$ echo 333 >> f`  
  
2. 임시 저장에 저장  
`$ git stash`

4. 임시 저장을 다시 작업 디렉토리에 복사  
`$ git stash apply`

5. 스테이징 영역도 함께 복원  
`$ git stash apply --inde`


## 임시 저장(Stash) 기초
- **임시 저장 수행**: `git stash`, `git stash save`
- **임시 저장 복원**: `git stash apply`, `git stash pop`
- **임시 저장 목록 확인 및 삭제**: `git stash list`, `git stash drop`, `git stash clear`

## 임시 저장 관련 다양한 명령
- **스테이징 영역 유지**: `git stash save -k`
- **Untracked 파일 포함**: `git stash save -u`
- **메시지 저장**: `git stash -m '메시지'`

## 임시 저장 복원 시 충돌 해결
- **충돌 발생 시 상태 확인**: `git status`
- **충돌 해결 후 커밋**: `git add`, `git commit`

## Untracked 파일 삭제
- **파일 삭제 명령**: `git clean -f`
