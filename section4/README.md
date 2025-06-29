## 4. 차원 넘나들기
### 1. 여러 branch 만들어보기
- Branch : 분기된 가지 (다른 차원)
  - 프로젝트를 하나 이상의 모습으로 관리해야 할 때
    - 예) 실배포용, 테스트서버용, 새로운 시도용
  - 여러 작업들이 각각 독립되어 진행될 때
    - 예) 신기능 1, 신기능 2, 코드개선, 긴급수정...
    - 각각의 차원에서 작업한 뒤 확정된 것을 메인 차원에 통합

#### 1. 브랜치 생성 / 이동 / 삭제하기
- add-coach란 이름의 브랜치 생성
  - git branch add-coach
- branch 목록 확인
  - git branch
- add-coach 브랜치로 이동
  - git switch add-coach
- 브랜치 생성과 동시에 이동하기
  - git switch -c new-teams
- 브랜치 삭제하기
  - git branch -d (삭제할 브랜치명)
- 브랜치 강제 삭제 (다른 브랜치로 가져오지 않은 내용이 있는 브랜치를 삭제)
  - git branch -D (강제삭제할 브랜치명)
- 브랜치 이름 바꾸기
  - git branch -m (기존 브랜치명) (새 브랜치명)

#### 2. 각각의 브랜치에서 서로 다른 작업해보기
- main 브랜치
  - Leopards의 members에 Olivia 추가
    - 커밋 메시지: Add Olivia to Leopards
  - Panthers의 members에 Freddie 추가
    - 커밋 메시지: Add Freddie to Panthers
  - add-coach 브랜치로 이동하여 해당 코드들 확인
- add-coach 브랜치
  - Tigers의 매니저 정보 아래 coach: Grace 추가
    - 커밋 메시지: Add Coach Grace to Tigers
  - Leopards의 매니저 정보 아래 coach: Oscar 추가
    - 커밋 메시지: Add Coach Oscar to Leopards
  - Panthers의 매니저 정보 아래 coach: Teddy 추가
    - 커밋 메시지: Add Coach Teddy to Panthers
- new-teams 브랜치
  - pumas.yaml 추가
    - 커밋 메시지: Add team Pumas
    <pre>
    team: Pumas

    manager: Jude

    members:
    - Ezra
    - Carter
    - Finn
    </pre>
  - jaguars.yaml
    - 커밋 메시지: Add team Jaguars
    <pre>
    team: Jaguars

    manager: Stanley

    members:
    - Caleb
    - Harvey
    - Myles
    </pre>

#### 3. 결과 살펴보기
- git log
- 여러 브랜치의 내역 편리하게 보기
  - git log --all --decorate --oneline --graph

### 2. branch를 합치는 두 가지 방법
서로 다른 브랜치를 합치는 두 방식
- merge : 두 브랜치를 한 커밋에 이어붙입니다.
  - 브랜치 사용내역을 남길 필요가 있을 때 적합한 방식입니다.
  - 다른 형태의 merge에 대해서도 이후 다루게 될 것입니다.
- rebase : 브랜치를 다른 브랜치에 이어붙입니다.
  - 한 줄로 깔끔히 정리된 내역을 유지하기 원할 때 적합합니다.
  - 이미 팀원과 공유된 커밋들에 대해서는 사용하지 않는 것이 좋습니다.

### 3. branch 합치기 실습
- merge로 합치기
  - add-coach 브랜치를 main 브랜치로 merge
    - main 브랜치로 이동
    - 아래의 명령어로 병합
      - git merge add-coach
- merge는 reset으로 되돌리기 가능
  - merge도 하나의 커밋
  - merge하기 전 해당 브랜치의 마지막 시점으로
- 병합된 브랜치는 삭제
  - 삭제 전 소스트리에서 add-coach 위치 확인
  - git branch -d add-coach
- rebase로 합치기
  - new-teams 브랜치를 main 브랜치로 rebase
  - new-teams 브랜치로 이동
    - merge때와는 반대!
  - 아래의 명령어로 병합
    - git rebase main
  - main 브랜치로 이동 후 아래 명령어로 new-teams의 시점으로 fast-forward
    - git merge new-teams
  - new-teams 브랜치 삭제

### 4. 충돌 해결하기

### 5. 