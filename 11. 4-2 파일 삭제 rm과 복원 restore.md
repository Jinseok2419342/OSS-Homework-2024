# 파일 삭제와 복원

### 파일 삭제 명령어
1. **리눅스 파일 삭제**
    ```bash
    $ rm [file]
    ```

    - 작업 디렉토리에서 파일 삭제

2. 깃 명령 파일 삭제
    - 작업 디렉토리와 스테이징 영역에서 모두 파일 삭제:
    ```bash
    $ git rm [file]
    ```
    - 스테이징 영역에서만 파일 삭제:
    ```bash
    $ git rm --cached [file]
    ```

-----

### 파일 복원 명령어 

1. 작업 디렉토리 복원
    - 스테이징 영역 상태로 복원:
    ```bash
    $ git restore [file]
    ```
2. 스테이징 영역 복원
    - 깃 저장소 상태로 복원:
    ```bash
    $ git restore --staged [file]
    ```
3. 작업 디렉토리와 스테이징 영역 동시에 복원
    - 깃 저장소 상태를 한 번에 복원:
    ```bash
    $ git restore --source=HEAD --staged --worktree [file]
    ```
4. HEAD 상태로 복원
    - 작업 디렉토리 복원:
    ```bash
    $ git restore --source=HEAD [file]
    ```
    - 특정 이전 커밋으로 복원:
    ```bash
    $ git restore --source=HEAD^ --staged [file]
    ```

-----------

### 깃의 3 영역과 상태 변화
- 작업 디렉토리(Working Directory): 로컬 파일이 저장된 공간
- 스테이징 영역(Staging Area): 커밋 준비 파일이 대기 중인 공간
- 깃 저장소(Git Repository): 커밋이 저장된 영역

**예시**
- 작업 디렉토리, 스테이징 영역, 저장소의 파일 상태를 복원하거나 삭제하는 다양한 명령어를 사용해, 파일 상태를 관리

------

### 정리
- 파일 삭제 명령어:
    - 작업 디렉토리: `$ rm [file]`
    - 스테이징 영역: `$ git rm --cached [file]`
    - 둘 모두: `$ git rm [file]`
파일 복원 명령어:
    - 스테이징 → 작업 디렉토리: `$ git restore [file]`
    - 저장소 → 스테이징: `$ git restore --staged [file]`
    - 저장소 → 작업 디렉토리 + 스테이징: `$ git restore --source=HEAD --staged --worktree [file]`

