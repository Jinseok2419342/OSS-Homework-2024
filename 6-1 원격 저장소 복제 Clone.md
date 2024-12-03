# 원격 저장소 복제 (Clone)

## 학습 개요
1. 지역 저장소와 원격 저장소
2. 원격 저장소 복제
3. Vscode로 원격 저장소 복제

## 학습 목표
1. GitHub에서 원격 저장소를 생성할 수 있다.
2. 원격 저장소를 지역 저장소에 복제할 수 있다.
3. 원격 저장소의 별칭 이름을 이해하고 관리할 수 있다.
4. Vscode에서 원격 저장소를 복제할 수 있다.

## 클론 개념
- 원격 저장소
- GitHub
- 원격 저장소를 지역 저장소에 복제 (clone)
- 공개된 저장소는 소유와 관계없이 누구나 가능

## Git 명령어 예시
```sh
$ git clone [복사된-주소]
$ git clone [복사된-주소] [새로운-폴더명]
$ git clone [복사된-주소] .
```

### 원격 저장소 관리
- 원격 저장소의 별칭 이름
- 원격 저장소 목록 보기
- 원격 저장소 정보 목록 표시
- 기본 이름 origin 설정
- 원격 저장소 추가, 이름 수정, 삭제


### 예시 명령어
```sh
$ git remote
$ git remote -v
$ git remote add origin URL
$ git remote show origin
$ git remote rename origin org
$ git remote rm org
```

### Vscode에서 Git 저장소 복제
1. Vscode 열기
2. Clone Git Repository 선택
3. URL 입력: https://github.com/git/git.git
복제 성공 확인
