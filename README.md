# QA Plugin

Claude Code용 QA(Quality Assurance) 테스트 플러그인입니다.

## Overview

이 플러그인은 Claude Code 플러그인 시스템의 동작을 검증하기 위한 테스트 도구입니다. 플러그인이 올바르게 설치되고 동작하는지 확인할 수 있는 간단한 테스트 명령어를 제공합니다.

## Features

- **테스트 명령어**: 플러그인 동작 확인용 `/test` 슬래시 명령어
- **Marketplace 호환**: 공식 Claude Code 플러그인 마켓플레이스 형식 지원
- **간단한 구조**: 최소한의 파일로 구성된 경량 플러그인

## Plugin Structure

```
QA-plugin/
├── .claude-plugin/
│   └── marketplace.json      # 마켓플레이스 등록 정보
├── plugins/
│   └── qa-plugin/
│       ├── .claude-plugin/
│       │   └── plugin.json   # 플러그인 메타데이터
│       └── commands/
│           └── test.md       # /test 명령어 정의
└── README.md
```

## Installation

### Method 1: Via Marketplace (Recommended)

1. Claude Code에서 `/plugin` 명령어 실행
2. **Add Marketplace** 선택
3. 다음 입력:
   ```
   k984530/QA-plugin
   ```
4. **Install Plugin** 선택 후 `qa-plugin` 설치

### Method 2: Via Local Path

```bash
claude --plugin-dir /path/to/QA-plugin/plugins/qa-plugin
```

## Commands

| Command | Description | Output |
|---------|-------------|--------|
| `/test` | 플러그인 동작 테스트 | `Hello QA World` |

## Use Cases

1. **플러그인 시스템 검증**: Claude Code 플러그인이 정상적으로 로드되는지 확인
2. **Marketplace 연동 테스트**: 커스텀 마켓플레이스 등록 및 설치 프로세스 검증
3. **플러그인 개발 참고**: 새 플러그인 개발 시 기본 구조 참고용 템플릿

## Technical Details

- **Plugin Name**: `qa-plugin`
- **Version**: `0.1.0`
- **Category**: `testing`
- **License**: MIT
- **Author**: choiwon

## Repository

- **GitHub**: https://github.com/k984530/QA-plugin
- **Marketplace Source**: `k984530/QA-plugin`

## License

MIT License - 자유롭게 사용, 수정, 배포할 수 있습니다.
