# 파일 diff, rm, restore 실습

## 학습 목표
- **깃 3 영역**의 파일 비교 방법 학습
- **커밋 간**의 파일 비교
- 파일 삭제 및 복구 실습

## 파일 비교 (`diff`)
### 기본 명령어
- **작업 디렉토리와 스테이징 영역 비교**: `git diff`
- **깃 저장소와 작업 디렉토리 비교**: `git diff HEAD`
- **깃 저장소와 스테이징 영역 비교**: `git diff --staged`

### 예제 흐름
1. **파일 수정 후 비교**  
   - 작업 디렉토리만 다른 상태에서 `git diff` 명령어를 통해 변경 사항 확인.
2. **파일 추가 후 비교**  
   - 스테이징 영역과 저장소의 파일 변경을 비교.
3. **커밋 후 비교**  
   - 모든 영역이 동일한 상태(`clean`)에서 비교.

### 커밋 간 비교
- `git diff HEAD~ HEAD`: 이전 커밋과 현재 커밋 간의 변경 확인.
- `git diff HEAD HEAD~`: 반대 방향으로 비교.

---

## 파일 삭제 (`rm`)와 복구 (`restore`)
### 파일 삭제
- 작업 디렉토리와 스테이징 영역에서 함께 삭제:  
  ```bash
  git rm <파일명>
  ```
- 스테이징 영역에서만 삭제:
  ```bash
  git rm --cached <파일명>
  ```
- 작업 디렉토리에서만 삭제:
  ```bash
  rm <파일명>
  ```
### 파일 복구

- 스테이징 영역의 파일을 작업 디렉토리에 복원:
  ```bash
  git restore <파일명>
  ```

- 깃 저장소에서 스테이징 영역으로 복원:
  ```bash
  git restore --staged <파일명>
  ```

- HEAD 기준으로 작업 디렉토리에 복원:
  ```bash
  git restore --source=HEAD --worktree <파일명>
  ```

- HEAD 기준으로 스테이징 영역과 작업 디렉토리에 복원:
  ```bash
  git restore --source=HEAD --staged --worktree <파일명>
  ```

-----

### 명령 별칭 (Alias)
반복적인 명령어를 짧게 설정:
```bash
git config --global alias.<별칭> '<명령어>'
```
예:
- `git config --global alias.ss 'status -s'`
- `git config --global alias.c commit`
설정 후:
- `git ss` → `git status -s`
- `git c` → `git commit`

------

### 요약
#### 주요 비교 명령어 
- `git diff`: 스테이징 영역 기준 작업 디렉토리 비교.
- `git diff HEAD`: 깃 저장소 기준 작업 디렉토리 비교.
- `git diff --staged HEAD`: 깃 저장소 기준 스테이징 영역 비교.
#### 주요 복구 명령어 
- 파일을 작업 디렉토리에 복원: git restore <파일명>
- 파일을 스테이징 영역과 작업 디렉토리에 모두 복원:
  `git restore --source=HEAD --staged --worktree <파일명>`
