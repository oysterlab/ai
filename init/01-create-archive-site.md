# AX Prototyping Experiment Archive

## Context
디자이너가 AI에게 디자인 이미지와 설명을 전달하면 프로토타입에 정확히 반영되는지 실험하는 과정을 아카이빙하는 인터랙티브 스크롤 페이지.

## Purpose
- 실험 과정의 스토리텔링
- 각 시도에서 얻은 인사이트 정리

## Aesthetic Direction
- **Tone**: 디자이너 포트폴리오 / Case Study 스타일. 세련되고 여백이 충분한.
- **Color**: Light theme with subtle warm tones. 순백이 아닌 off-white (#FAFAFA or #F5F5F0). Accent는 차분한 색상 (muted blue, warm gray).
- **Typography**: Elegant sans-serif (Söhne, Lausanne, Suisse Intl 등). 본문은 가독성 좋게, 제목은 큼직하게.
- **Motion**: Subtle, smooth. Scroll-triggered fade-in. 과하지 않게.
- **Layout**: 넉넉한 여백, 비대칭 그리드, 이미지 중심

---

## Page Structure

### 1. Hero Section
크고 임팩트 있게. 미니멀하게.

```
[큰 여백]

Exploration #001

AX Prototyping
디자인 → AI → 구현

[작은 서브텍스트]
디자인 이미지와 설명만으로 
복잡한 UI를 정확히 반영할 수 있는가?

[큰 여백]
```

### 2. Context Section
Before / Target 이미지를 크게 보여줌

```
┌──────────────────────────────────────────────────────────┐
│                                                          │
│    Before                          Target                │
│    ┌────────────────┐              ┌────────────────┐    │
│    │                │              │                │    │
│    │  placeholder   │      →       │  placeholder   │    │
│    │  16:9          │              │  16:9          │    │
│    │                │              │                │    │
│    └────────────────┘              └────────────────┘    │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

### 3. Phase Section
각 Phase는 세로 스크롤의 큰 섹션으로.

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Phase 01
Pure UI

[Phase 설명 - 1-2문장]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 4. Attempts Block (핵심 - 가로 슬라이드)

**3회 시도를 가로 캐러셀/슬라이더로 표현**

메인 스크롤은 세로로 유지하되, 각 Phase 안의 시도들은 **가로로 넘기는 방식**.

```
Phase 01: Pure UI
─────────────────────────────────────────────────────────

  ┌─ Attempt 1/3 ────────────────────────────────────┐
  │                                                   │
  │  Prompt                                          │
  │  ─────────────────────────────────────────────   │
  │  "메인 배너의 그라데이션을 타겟 이미지처럼         │
  │   변경해줘. 좌상단에서 우하단으로."                │
  │                                                   │
  │  Result                                          │
  │  ┌─────────────────────────────────────────┐     │
  │  │                                         │     │
  │  │           [placeholder 16:9]            │     │
  │  │                                         │     │
  │  └─────────────────────────────────────────┘     │
  │                                                   │
  └───────────────────────────────────────────────────┘
  
         ○ ● ○   ← dot indicator
         
      [← prev]  [next →]  또는 swipe gesture

─────────────────────────────────────────────────────────
```

**Alternative: 가로 스크롤 스냅**
- 3개의 attempt 카드가 가로로 나열
- 스크롤 스냅으로 한 장씩 넘김
- 모바일에서 자연스러운 swipe

### 5. Insight Block
Phase 끝에 해당 Phase의 인사이트 정리

```
─────────────────────────────────────────────────────────

Insight

Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
Sed do eiusmod tempor incididunt ut labore et dolore 
magna aliqua. Ut enim ad minim veniam, quis nostrud 
exercitation ullamco laboris.

─────────────────────────────────────────────────────────
```

### 6. Phase Transition
다음 Phase로 넘어갈 때 전환 이유

```
[충분한 여백]

Phase 01의 한계
───────────────
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Sed do eiusmod tempor incididunt.

↓

Phase 02로 전환
───────────────
Lorem ipsum dolor sit amet.

[충분한 여백]
```

### 7. Judgment Point (마지막)

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Judgment

이 실험에서 내린 판단들

01  Lorem ipsum dolor sit amet, consectetur 
    adipiscing elit sed do eiusmod.

02  Ut enim ad minim veniam, quis nostrud 
    exercitation ullamco laboris.

03  Duis aute irure dolor in reprehenderit 
    in voluptate velit esse cillum.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Open Questions

• Lorem ipsum dolor sit amet?
• Consectetur adipiscing elit?

[Footer 여백]
```

---

## Technical Requirements
- React + Framer Motion
- 가로 슬라이더: Embla Carousel 또는 CSS scroll-snap
- Scroll animations: Framer Motion의 whileInView
- 모든 이미지는 placeholder (subtle gray gradient background)

## Placeholder Style
```css
.placeholder {
  background: linear-gradient(135deg, #E8E8E8 0%, #D0D0D0 100%);
  aspect-ratio: 16/9;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #888;
  font-size: 14px;
}
```

## Typography
- 제목: 48-72px, weight 500
- 섹션 헤더: 24-32px, weight 500
- 본문: 16-18px, weight 400, line-height 1.6
- 프롬프트: 16px, slightly different style (italic or different weight)

## Color Palette
```css
--bg: #FAFAF8;
--text: #1A1A1A;
--text-muted: #666666;
--accent: #4A5568;
--border: #E2E2E0;
```

## Sample Data
Phase 1: 3 attempts
Phase 2: 3 attempts  
Phase 3: 3 attempts (또는 2개)

각 attempt의 prompt와 insight는 lorem ipsum으로 채움.
