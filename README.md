# Git-Flow에 대해서 알아보자

개발 tool을 사용하여 진행해 봅니다. (여기서는 Jira를 이용하는 것으로 가정합니다.)

### 작업 진행시에 지켜야할 규칙

1. 작업이 시작하면 jira의 issue를 생성합니다.
2. 1개의 issue ticket은 1개의 commit으로 합니다.
3. commit graph는 최대한 단순하게 가져갑니다.
4. 다른사람의 commit 내용은 함부로 변경하지 않습니다.
5. 리뷰어에게 꼭 리뷰를 받습니다.
6. 자신의 Pull Request는 스스로 merge 합니다.

### Git-Flow

- main: 제품으로 출시될 수 있는 브랜치
- develop: 다음 출시 버전을 개발하는 브랜치
- feature: 기능을 개발하는 브랜치
- release: 이번 출시 버전을 준비하는 브랜치
- bugfix: 다음 출시 버전에서 찾아낸 버그를 수정 하는 브랜치
- hotfix: 출시 버전에서 발생한 버그를 수정 하는 브랜치

### Github Branch Protect Rule

- main: main 브랜치는 직접 push가 불가능하며 `release` 브랜치의 PR을 통해서만 merge가 가능합니다. ( squash merge )
- develop: develop 브랜치는 직접 push가 불가능하며 `feature`, `bugfix` 브랜치의 PR을 통해서만 merge가 가능합니다. ( rebase merge )
  [More](docs/Github_Branch_Ruleset.md)

---

### feature 신규작업 진행

[Link](docs/Feature_신규작업_진행.md)

### bugfix 버그수정 진행

[Link](docs/Bugfix_버그수정_진행.md)

### hotfix 버그수정 진행

[Link](docs/Hotfix_버그수정_진행.md)

### release-it을 이용한 major 버전 증가시키기

### PR 규칙

`hotfix`, `feature` 브랜치에서 `develop` 브랜치로 PR을 생성합니다.

1. PR은 최소 1명 이상의 리뷰어를 지정합니다.
2. PR은 최소 1명 이상의 리뷰어의 approve가 있어야 merge가 됩니다.

### release 버전 출시 진행

1. `release` 브랜치를 생성합니다. (release/Version-Number)
2. `release` 브랜치에서 `develop` 브랜치의 버전에 맞는 commit들을 cherry-pick 합니다.
3. `release` 브랜치에서 버전에 맞는 테스트를 진행합니다.
4. `release` 브랜치에서 `main` 브랜치로 PR을 생성합니다.

### release-it을 이용한 버전 관리
