# 🌿 부부 주말 큐레이터

남편이 아내에게 먼저 새로운 주말 경험을 제안할 수 있도록, 매주 그 시기·계절·날씨에 맞는 데이트·여행·운동 아이디어 20개 내외를 골라 주는 AI 에이전트입니다.

| 파일 | 내용 |
| --- | --- |
| [`prompts/weekend-curator.md`](prompts/weekend-curator.md) | 에이전트 시스템 프롬프트 (역할·규칙·출력 형식) |
| [`profile.md`](profile.md) | 지역·예산·취향·기념일 등 개인화 정보 — **처음 한 번 채워 주세요** |
| [`history.md`](history.md) | 추천 이력 (4~6주 중복 방지용, 자동 갱신) |
| [`reports/`](reports/) | 주간 보고서 (`YYYY-MM-DD.md`) |
| [`CLAUDE.md`](CLAUDE.md) | Claude Code가 이 저장소에서 큐레이터로 동작하기 위한 절차 |

## 자동 실행

Claude Code 루틴(예약 트리거)이 **매주 수요일 오후 2시 무렵(한국 시간)** 실행되어 `CLAUDE.md`의 절차대로 보고서를 만들고 커밋합니다.

## 다른 AI에서 쓰려면

`prompts/weekend-curator.md` 전체를 해당 AI의 시스템 프롬프트/인스트럭션에 붙여 넣고, `profile.md` 내용을 함께 알려 주세요. 자동 실행(규칙 ③)은 그 서비스의 예약 기능으로 따로 설정해야 합니다.
