# 지역과 원격 저장소 연동 (Push & Pull)

## 학습 개요
1. Personal Access Token
2. Push와 Pull
3. Fetch

## 학습 목표
1. GitHub 계정에 PAT(Personal Access Token)을 생성하고 저장할 수 있다.
2. 원격 저장소와 연동하여 원격 저장소의 수정을 pull할 수 있다.
3. 원격 저장소와 연동하여 원격 저장소의 수정을 fetch한 후 병합할 수 있다.
4. 원격 저장소와 연동하여 지역 저장소의 수정을 push할 수 있다.

## Personal Access Token 생성
1. GitHub 계정에 Personal Access Token 생성
2. Personal Access Token 인증 개요
3. Personal Access Token 생성 방법
4. Personal Access Token 생성 후 관리 필요

## GitHub 원격 저장소 연동
1. 원격 저장소의 수정을 pull
2. 원격 저장소의 수정을 fetch 후 병합
3. 지역 저장소의 수정을 원격 저장소로 push

## 명령어 정리
- `git pull`: 원격 저장소의 수정을 가져와 병합
- `git fetch`: 원격 저장소의 수정을 가져오기만 함
- `git push`: 지역 저장소의 수정을 원격 저장소로 전송
- `git merge` : 변경된 정보를 로컬 저장소의 내용과 병합

## 요약
- 원격 저장소 복제 연동: `git clone https://github.com/atom/atom.git`
- 원격 저장소 수정 사항 pull: `git pull origin main`
- 원격 저장소 수정 사항 fetch: `git fetch origin main`
- 원격 저장소로 수정 사항 push: `git push origin main`
