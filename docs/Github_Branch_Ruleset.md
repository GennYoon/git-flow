# Rulesets/New branch ruleset

### Bypass list

- Organization admin Role
- Deploy keys
- Repository admin Role
- Maintain Role
- Write Role
- Vercel App

### Branch rules

1. Restrict creations - 브랜치 생성을 제한합니다.
2. Restrict updates - 브랜치 업데이트를 제한합니다.
3. Restrict deletions - 브랜치 삭제를 제한합니다.
4. Require linear history - 브랜치의 히스토리가 선형적이어야 합니다.
5. Require deployments to succeed - 배포가 성공해야합니다.
6. Require signed commits - GitHub GPG Key를 등록되어 커밋들이 sign이 되어있어야 합니다.
7. Require a pull request before merging

```
- PR을 통해서만 merge 가능
- local에서 Direct Push 불가
```

- Required approvals - 필수 review 승인 수
- Dismiss stale pull request approvals when new commits are pushed - 새로운 커밋이 push 되면 이전 PR을 닫습니다.
- Require review from Code Owners - 코드 소유자의 리뷰가 필요
- Require approval of the most recent reviewable push - PR요청자가 아닌 사람이 승인을 해야합니다.
- Require conversation resolution before merging - comment가 존재하는 경우 모두 해결해야 PR이 가능합니다.

8. Require status checks to pass - 상태 체크가 필요합니다.
9. Block force pushes - Force Push (강제 푸시) 를 허용할 것인지 여부를 결정합니다.
10. Require code scanning results - 코드 스캔 결과가 필요합니다.
