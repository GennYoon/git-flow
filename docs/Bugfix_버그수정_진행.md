# Bugfix 버그수정 진행

개발중 버그를 발견해서 수정이 필요할 때

### 진행 순서

1. `develop` 브랜치를 기준으로 `bugfix` 브랜치를 생성합니다. (bugfix/Issue-Number)
2. `bugfix` 브랜치에서 작업을 진행합니다.
3. 작업이 완료되면 `develop` 브랜치로 PR을 생성합니다.
4. PR이 승인되면 `develop` 브랜치로 merge합니다. ( rebase merge )
