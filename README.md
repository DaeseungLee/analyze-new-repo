# analyze-new-repo

`analyze-new-repo`는 낯선 저장소를 처음 접한 개발자가, 과하지 않은 분량으로 핵심 구조와 판단 포인트를 빠르게 이해할 수 있게 해주는 저장소 분석 스킬입니다.

이 스킬은 가벼운 요약문보다 **짧고 읽기 쉬운 분석 보고서**를 목표로 합니다. 단순히 파일을 나열하는 대신, 저장소의 목적, 실행 구조, 핵심 설계 결정, 품질 신호와 리스크를 증거 기반으로 정리하도록 설계되어 있습니다.

## 이 프로젝트가 제공하는 것

현재 이 저장소는 하나의 스킬을 제공합니다.

- `analyze-new-repo`: 낯선 repository를 분석해서 다음 내용을 빠르게 파악하도록 돕는 스킬
  - 이 프로젝트가 실제로 무엇을 하려는지
  - 어떻게 실행되고 구성되는지
  - 어떤 설계 결정이 구조를 규정하는지
  - 어떤 리스크와 미지수가 중요한지
  - 구조상 어디가 진짜 중심인지

## 스킬 출력 성격

이 스킬은 다음과 같은 결과를 지향합니다.

- 개발자가 한 번에 읽을 수 있는 적당한 분량
- README 요약이 아니라 판단이 있는 분석
- 사실과 해석이 함께 들어간 bullet 중심 보고서
- 저장소 성격에 맞게 유연하게 구성된 섹션

즉, 목표는 "처음 repo를 열었을 때 바로 다음 판단을 할 수 있게 해주는 분석 보고서"입니다.

## 설치 방법

GitHub 저장소에서 직접 설치할 수 있습니다.

```bash
npx skills add DaeseungLee/analyze-new-repo
```

특정 스킬만 설치:

```bash
npx skills add DaeseungLee/analyze-new-repo --skill analyze-new-repo
```

특정 에이전트에 설치:

```bash
npx skills add DaeseungLee/analyze-new-repo -a claude-code
npx skills add DaeseungLee/analyze-new-repo -a codex
npx skills add DaeseungLee/analyze-new-repo -a opencode
npx skills add DaeseungLee/analyze-new-repo -a pi
```

또는 전체 GitHub URL을 사용할 수도 있습니다.

```bash
npx skills add https://github.com/DaeseungLee/analyze-new-repo
```

## 저장소 구조

```text
skills/
  analyze-new-repo/
    SKILL.md
    references/
      checklist.md
      report-template.md
examples/
  karpathy-autoresearch.md
LICENSE
README.md
```

## 주요 파일

- `skills/analyze-new-repo/SKILL.md`
  - 스킬의 본문 정의. 조사 순서, 출력 규칙, 증거 기준, 품질 기준이 들어 있습니다.
- `skills/analyze-new-repo/references/checklist.md`
  - 저장소 분석 시 빠르게 확인할 항목들입니다.
- `skills/analyze-new-repo/references/report-template.md`
  - 출력 보고서의 기본 구조 가이드입니다.
- `examples/karpathy-autoresearch.md`
  - 한 가지 예시 출력입니다. 대표적인 모든 케이스를 대변하진 않지만, 원하는 출력 톤과 밀도를 보여줍니다.

## 개발 및 로컬 확인

현재 디렉터리에서 발견되는 스킬 목록 확인:

```bash
npx skills add . --list
```

로컬 체크아웃에서 단일 스킬 설치 테스트:

```bash
npx skills add . --skill analyze-new-repo -a claude-code
```

## 라이선스

MIT License. 자세한 내용은 `LICENSE`를 참고하세요.
