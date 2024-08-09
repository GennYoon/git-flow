# Hotfix 버그수정 진행

출시 후 버그가 발생하여 신속한 대응이 필요할 때

### 진행 순서

1. `main` 브랜치를 기준으로 `hotfix` 브랜치를 생성합니다. (hotfix/Issue-Number)
2. `hotfix` 브랜치에서 작업을 진행합니다.
3. 작업이 완료되면 `main` 브랜치로 PR을 생성합니다.
4. PR이 승인되면 `main` 브랜치로 merge합니다. ( squash merge )
