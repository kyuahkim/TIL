# Git 원격 저장소

## remote repository
    - 온라인 상에서 여러 개발자가 코드와 버전 관리 이력을 저장하는 공간
- 로컬 vs 원격 저장소
    - 위에서 배운 커밋을 하면 우선 로컬저장소에 저장된다.
    - 원격 저장소로 옮기려면 git remote 명령어 사용 필요
    
    ```bash
    git remote add (별칭) remote_repo_url #로컬에 remote repo 등록
    git push (별칭) (브랜치명) # remote로 push
    ```
    
- git pull vs git clone
    - git pull : 원격 저장소의 변경사항만을 받아옴 (업데이트), 로컬 레포가 존재해야 함 (.git)’
        - `git pull orgin master`
    - git clone : 원격 저장소 전체를 복제, 로컬 레포가 없음 (.git X)
- 항상 기준은 remote!! ssafy 강의장도, home도 remote와 버전 맞추고 commit
    - `git pull → 작업 → add → commit → push` 순서로
- .gitignore
    - git에서 특정 파일이나 디렉토리를 추적하지 않도록 설정하는데 사용되는 텍스트파일
    - `.gitignore` 라는 명칭으로 파일 생성
    - gitignore 만들고 git init하는걸 추천
    - .gitignore에 넣지 않고 commit → 이후에 .gitignore에 추가 → ignore되지 않는다.
    - 추가로 gitignore하고 싶다면 `git rm —cached {file}`
    - → 즉 처음부터 gitignore에 넣어놓는게 속 편함
    - [gitignore.io](http://gitignore.io) 참고해서 만들기
        + 설정 목록은 사용언어, 환경, 에디터, 프레임워크
        ex. python, visualstudiocode, jupyternotebook, django
## TIL (Today I learned)
- 내가 학습하는 것을 마크다운으로 기록하는 곳
    - https://wayhome25.github.io/ 참고해서 TIL 만들기
    - 잔디를 심자