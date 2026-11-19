# groundwork

`groundwork` 스킬을 담은 GitHub 템플릿 저장소입니다.
이 템플릿으로 새 저장소를 만들면 Claude Code에서 바로 `/groundwork`를 실행해 프로젝트를 세팅할 수 있습니다.

## 사용법

1. 이 저장소 페이지에서 **Use this template → Create a new repository**를 누릅니다.
2. 새 저장소로 웹 Claude Code 세션을 엽니다.
3. `/groundwork`를 실행하고 질문에 답합니다.
4. Claude가 올린 PR을 확인하고 머지합니다.

세팅이 끝나면 템플릿 전용 파일(`.template/`, `.github/workflows/skill-check.yml`)은 삭제되고, 이 README는 새 프로젝트용으로 바뀝니다.
`.claude/skills/groundwork/`은 나중에 다시 실행할 수 있도록 남습니다.

## 구성

| 경로 | 역할 |
|---|---|
| `.claude/skills/groundwork/SKILL.md` | 스킬 본문 |
| `.template/MANIFEST` | 새 저장소에서 정리할 템플릿 전용 파일 목록 |
| `.template/check.py` | 스킬 형식 검사 (Python 표준 라이브러리만 사용) |
| `.github/workflows/skill-check.yml` | 스킬이 바뀔 때 검사를 돌리는 CI. 이 원본 저장소에서만 실행 |

## 유지보수

- 스킬을 고친 뒤 `python3 .template/check.py`로 검사합니다. 성공하면 한 줄만 출력됩니다.
- 템플릿 전용 파일을 추가하면 `.template/MANIFEST`에도 적습니다.
- 이 저장소의 스킬과 claude.ai 계정에 저장된 스킬은 자동으로 동기화되지 않습니다. 한쪽을 고치면 다른 쪽도 맞춰 주세요. 둘 다 있으면 세션에 스킬이 두 번 보일 수 있으니 하나만 쓰는 편이 좋습니다.
