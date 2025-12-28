# Quick Prompts for Claude Code

## 1. 초기 사이트 생성
```
01-create-archive-site.md를 읽고 
React + Framer Motion으로 인터랙티브 스크롤 페이지를 만들어줘.

- 디자이너 포트폴리오 / Case Study 느낌
- Light theme, off-white 배경
- 넉넉한 여백, 세련된 타이포그래피
- 각 Phase의 3회 시도는 가로 슬라이드(캐러셀)로
- Scroll-triggered subtle animations
- 모든 이미지는 placeholder
- Insight 텍스트는 lorem ipsum으로
```

## 2. Phase 추가
```
새로운 Phase 섹션 추가:

Phase: [번호]
Title: "[Phase 이름]"
Description: "[1-2문장 설명 또는 lorem ipsum]"

Attempts (3개):
1. Prompt: "[프롬프트 또는 lorem ipsum]"
2. Prompt: "[프롬프트 또는 lorem ipsum]"  
3. Prompt: "[프롬프트 또는 lorem ipsum]"

Result는 모두 placeholder 이미지로.
```

## 3. Phase 전환 블록 추가
```
Phase [N] → Phase [N+1] 전환 블록 추가:

한계: "[lorem ipsum 또는 실제 내용]"
전환 이유: "[lorem ipsum 또는 실제 내용]"
```

## 4. Insight 업데이트
```
Phase [N]의 Insight를 다음으로 교체:

"[실제 인사이트 내용]"
```

## 5. Judgment 업데이트
```
Judgment 섹션 업데이트:

판단들:
1. [내용]
2. [내용]
3. [내용]

Open Questions:
• [질문]
• [질문]
```

## 6. 이미지 교체 (나중에)
```
"[placeholder 설명]" 위치의 placeholder를 
실제 이미지로 교체: ./images/[파일명]
```

## 7. 가로 슬라이더 수정
```
Phase [N]의 attempt 슬라이더에서:
- Attempt [번호]의 prompt를 "[새 프롬프트]"로 변경
- Result placeholder 텍스트를 "[설명]"으로 변경
```
