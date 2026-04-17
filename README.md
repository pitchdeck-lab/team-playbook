# Pitchdeck Lab — Team Playbook

> 우리 팀이 일하는 방식, 쓰는 도구, 지키는 약속.

---

## 📍 pitchdeck-lab이란

**Pitchdeck Lab**은 [Pitchdeck Corp.](https://pdeck.co.kr)의 데이터 인텔리전스 조직입니다.
비상장 기업 데이터, 뉴스, 시장 분석을 기반으로 인사이트를 생산합니다.

## 👥 팀 멤버

자기소개는 [`members/`](./members/) 폴더에 각자 파일로.

## 🛠️ 기술 스택

- **Language:** Python (주), SQL
- **Database:** Supabase (PostgreSQL)
- **Version Control:** Git + GitHub
- **CI/CD:** GitHub Actions
- **Editor:** VSCode

## 🤝 협업 규칙

### Git 워크플로우
- `main` 브랜치는 직접 push 금지 (protected)
- 모든 변경은 **feature branch → PR → review → merge**
- PR은 최소 1명 이상 Approve 필요

### 브랜치 네이밍
```
feature/기능명       — 새 기능
fix/버그설명         — 버그 수정
docs/문서설명        — 문서 변경
chore/잡일설명       — 설정, 의존성
refactor/대상        — 리팩토링
```

### 커밋 메시지 컨벤션 (Conventional Commits)
```
<type>: <설명>

type: feat | fix | docs | refactor | test | chore | ci
```

예시:
- `feat: DART 공시 수집기 추가`
- `fix: 토큰 만료 시 재시도 로직 수정`
- `docs: API 엔드포인트 설명 추가`

### PR 템플릿
```markdown
## Summary
- 변경 요약 (불릿)

## Why
- 왜 이 변경이 필요한지

## Test
- [ ] 테스트 항목 1
- [ ] 테스트 항목 2

## Related
Closes #<이슈번호>
```

### 코드 리뷰 원칙
- 명령이 아닌 질문/제안으로
- 좋은 점도 언급 (균형)
- 컨벤션 기반, 개인 스타일 강요 금지
- 리뷰는 24시간 내 응답 목표

## 🔐 보안 규칙

### 절대 커밋 금지
- `.env` 파일
- API key, token, password
- 개인정보 (이메일, 전화번호)
- 회사 기밀 데이터

### 시크릿 관리
- 로컬: `.env` 파일 (gitignore 됨)
- 공유: Bitwarden Organization (추후)
- CI: GitHub Actions Secrets

### 실수 발견 시
시크릿이 커밋/푸시 된 경우 **즉시**:
1. 해당 키/토큰 재발급
2. `.gitignore` 업데이트
3. `git rm --cached` + 커밋
4. 이력 정리 (필요시 BFG Repo-Cleaner)

## 📚 참고 자료

- [[Git과 GitHub 완전정리]] — Git/GitHub 종합 가이드
- [Conventional Commits](https://www.conventionalcommits.org/)
- [GitHub Docs](https://docs.github.com/)

## 🎯 현재 Repo 목록

- **pitchdeck-corp-website** — 회사 공식 홈페이지
- **team-playbook** — 이 문서 (팀 운영 규칙)
- (추가 예정)

---

## 📝 이 플레이북 업데이트 방법

1. 브랜치 생성 (`docs/update-xxx`)
2. 변경
3. PR 생성
4. 리뷰 받고 머지

**이 플레이북은 살아있는 문서입니다.** 규칙이 바뀌면 같이 바꿉니다.
