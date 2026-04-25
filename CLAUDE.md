# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

정적 HTML 게임 모음 사이트. 빌드 도구, 패키지 매니저, 프레임워크 없이 순수 HTML/CSS/JS로 구성된다. 외부 라이브러리 의존성 없음.

배포: GitHub Pages → https://eastmannn.github.io/minigamegroup/
저장소: https://github.com/eastmannn/minigamegroup

## 파일 구조

```
index.html              # 홈 허브 — 5개 게임 카드 그리드
minesweeper.html        # 지뢰찾기 (기존 게임)
minesweeper_guide.html  # 지뢰찾기 규칙 가이드 페이지
snake.html              # 뱀 게임 (Canvas 기반)
game_2048.html          # 2048 타일 게임
memory_card.html        # 카드 뒤집기 (CSS 3D flip)
whack_a_mole.html       # 두더지 잡기
```

## 코드 규칙

**스타일 (모든 파일 공통)**
- 배경 `#1a1a2e`, surface `#16213e`, accent `#e94560`, 텍스트 `#eee`, muted `#aaa`
- 폰트: `'Segoe UI', sans-serif`
- 카드/버튼: `border-radius: 8px`, hover 시 `translateY(-4px)`, `transition: 0.2s`
- CSS/JS는 해당 HTML 파일 안에 인라인으로 작성 (외부 파일 분리 없음)
- UI 텍스트는 한국어

**네비게이션**
- 모든 게임 페이지 상단에 `← 홈으로` 링크(`href="index.html"`) 포함

## Git & 배포

변경이 생기면 관련 파일만 스테이징 후 커밋하고 push한다. push하면 GitHub Pages가 자동 재배포된다.

```bash
git add <변경된 파일>
git commit -m "..."
git push
```
