### 섹션 2. Git 시작하기 (32분)
#### 4. 🐰 Git을 배워야 하는 이유  

1) Git은 프로젝트의 시간과 차원을 자유롭게 넘나들수 있도록 해줍니다.
시간 - 프로젝트의 버전을 과거로 되돌리거나 특정 내역을 취소할 수 있습니다.
차원 - 프로젝트의 여러 모드를 쉽게 전환하고 관리할 수 있습니다.
2) Git은 여러 사람들이 프로젝트에서 협업할 수 있도록 도와줍니다.


#### 5. 설치와 세팅 (윈도우)  
#### 6. 설치와 세팅 (맥)  
- git 설치
- SourceTree 설치 (https://www.sourcetreeapp.com/)
- VS Code 설치
- iTerms2 설치 (https://iterm2.com/)
  - 탭, split view, 자동완성 등 다양한 기능
  - 얄코 설정 (https://yalco.notion.site/iTerm2-7866389fbcc449ebb07a587b8b761303)

#### 7. 🐰 CLI vs GUI: 무엇을 사용해야 할까?  
1) Git을 사용하는 방법은 아래의 둘로 나뉩니다.
터미널에 명령어를 이용하는 CLI 방식
소스트리 등의 프로그램을 사용하는 GUI 방식

2) Git 학습과 사용에 있어서 얄코가 추천하는 방식은 아래와 같습니다.
Git을 공부할 때는 CLI 위주로 실습해서 명령어들과 동작 방식을 익힐 것
사용할 때는 작업의 성질에 따라 편리하고 유리한 것으로 혼용할 것

#### 8. Git 설정 및 프로젝트 시작  
- Git폴더 초기화
`git init`
- git 폴더의 상태
`git status`

#### 9. Git에게 맡기지 않을 것들  
- 포함할 필요가 없을 때
  - 자동으로 생성 또는 다운로드 되는 파일
- 포함하지 말아야 할 때
  - 보안상 민감정보 파일
- .gitignore
  - 배제할 파일 및 폴더 등을 지정할 수 있다.
  - secret.yaml 파일 생성
    - 민감정보 저장
  - .gitignore 파일에 secret.yaml 파일을 목록에 추가
  - git status를 통해 상태 확인
<pre> 
- .gitignore 형식 (https://git-scm.com/docs/gitignore)
# 이렇게 #를 사용해서 주석

# 모든 file.c
file.c

# 최상위 폴더의 file.c
/file.c

# 모든 .c 확장자 파일
*.c

# .c 확장자지만 무시하지 않을 파일
!not_ignore_this.c

# logs란 이름의 파일 또는 폴더와 그 내용들
logs

# logs란 이름의 폴더와 그 내용들
logs/

# logs 폴더 바로 안의 debug.log와 .c 파일들
logs/debug.log
logs/*.c

# logs 폴더 바로 안, 또는 그 안의 다른 폴더(들) 안의 debug.log
logs/**/debug.log
</pre>

