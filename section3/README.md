## 3. 시간 여행하기
### 1. 변화를 타임캡슐에 담아 묻기
#### 1) 프로젝트의 변경사항들을 타임캡슐(버전)에 담기

- 변경사항 확인
  - git status
  - 추적하지 않는(untracked) 파일: Git의 관리에 들어간 적 없는 파일
- 파일 하나 담기
  - git add tigers.yaml
  - git status로 확인
- 모든 파일 담기
  - git add .
  - git status로 확인

#### 2) 타임캡슐 묻기
commit
- git commit
메시지까지 함께 작성
- git commit -m "first commit"
내용 확인
- git log

### 2. 과거로 돌아가는 두 가지 방법
- Git에서 과거로 돌아가는 두 방식
  - reset : 원하는 시점으로 돌아간 뒤 이후 내역들을 지웁니다.
  - revert : 되돌리기 원하는 시점의 커밋을 거꾸로 실행합니다.
  