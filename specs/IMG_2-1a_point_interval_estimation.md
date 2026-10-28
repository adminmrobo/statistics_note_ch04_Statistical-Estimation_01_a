# 2.1.a 「점추정과 신뢰구간」 이미지 제작 명세서

| 항목 | 내용 |
|---|---|
| 페이지 | 2-1a_point_interval_estimation.html |
| 모드 / 주 앵커 | 교과서 / B 연구실: 밤의 연구실 계량 실험대 (보조 D 현장: 과자 공장 시료) |
| 시즌 | 기본 |
| 대결 | 같은 n = 100에서 신뢰수준 95%(초파리) vs 99%(Money-Robo), 판정 기준 "쓸모 있는 구간 비율"(모평균 포함 + 폭 5g 이하) → 결과 **F**, 0.925 vs 0.420, 차이 0.505 |
| 새로 그릴 그림 | P1 2장 · P2 3장 · P3 1장 |
| 제작 경로 | 직접 3장 (페이지에 넣음: 히어로·아웃트로 합성본, 행동 캔버스) · 외부 의뢰 3장 (받을 것) |
| 의뢰 도구 | Genspark (기본) |
| 진행 | 받음 0 / 의뢰 3 · 마지막 반영 아직 |
| 캐릭터 팩 표정 | 25장 (96px) + 13장 (192px 덮어쓰기) (팩 커밋 ea5da3f) |
| 재사용 | 0장 (시리즈 기존 장면 목록 없음) |
| 그림이 없을 때 | 페이지는 캐릭터 팩 표정과 픽셀 연구실 캔버스·CSS 배경으로 이미 완성 상태 |

## 1. 그림체와 고정 외형
- 스타일: SKILL 18-3 (16비트 SNES 시대 픽셀 아트, 굵은 외곽선, 디더링 음영)
- 캐릭터 고정 외형: SKILL 18-4 표 그대로 (공식 저장소 `CHARACTER_CORE_EN`)
- 이 페이지 장소: 밤의 연구실 전경. 시험관 선반, 칠판(글자 없음), 작은 서버 랙, 실험대 위 **전자저울**과 **과자 상자(같은 모양 과자가 줄지어 든 나무 상자)**, 실험 노트 더미. 빛은 저울 쪽으로 모인다.
- 장소 영어 묘사: *wide night laboratory with test tube racks, a blank chalkboard, a small server rack, stacks of lab notebooks, and on the workbench a digital weighing scale beside a wooden crate filled with rows of identical round cookies, purple lab light, cyan monitor glow, the light gathering on the scale*

## 2. 필요한 그림 전체

| # | 키 | 판 | 크기 | 상태 | 제작 | 우선 | 들어가는 곳 | 대신 쓰는 그림 |
|---|---|---|---|---|---|---|---|---|
| 1 | bg_21a | F | 1920×720 | 의뢰 | 외부 | P1 | 히어로 배경 (`.hero-bg`) | CSS 그라데이션 + 벌집 무늬 |
| 2 | sc_21a_hero | E | 1200×800 | 넣음 (합성본) → 의뢰 | 직접 → 외부 | P1 | 히어로 무대 (`.stage`) | 픽셀 연구실 캔버스 + 팩 캐릭터 4명 합성 |
| 3 | sc_21a_outro | E | 1200×800 | 넣음 (합성본) | 직접 → 외부 선택 | P2 | 아웃트로 무대 | 픽셀 연구실(밤·달) + 팩 캐릭터, 초파리 앞·크게 |
| 4 | cut_21a_ringtoss | G | 960×540 | 의뢰 (선택) | 외부 | P2 | ④칸 고리 던지기 위 삽화 (현재 자리 없음, 받으면 c4b 위에 추가) | 없음 (캔버스 애니메이션으로 충분) |
| 5 | thumb_21a | I | 600×400 | 넣음 예정 | 직접 (bg_21a 3:2 자르기, 받기 전엔 히어로 합성본 캡처) | P2 | 목차 카드 | 색 카드 |
| 6 | og_21a | K | 1200×630 | 넣음 예정 | 직접 (합성) | P3 | 공유 미리보기 | 없음 |
| 7 | doc_think → doc_e09 | A | 팩 96·192 | 팩 | — | — | 히어로 대화창·무대 | — |
| 8 | doc_front → doc_e08 | A | 팩 96 | 팩 | — | — | 등장인물, 정리 말풍선 | — |
| 9 | doc_board → doc_e07 | A | 팩 96 | 팩 | — | — | 큰 그림 말풍선 | — |
| 10 | doc_magic → doc_e16 | A | 팩 96·192 | 팩 | — | — | ③ 말풍선, 아웃트로 | — |
| 11 | doc_judge → doc_e10 | A | 팩 96 | 팩 | — | — | 대결 판정 | — |
| 12 | asst_smile → asst_e13 | B | 팩 96·192 | 팩 | — | — | 히어로, 등장인물 | — |
| 13 | asst_e10 | B | 팩 96 | 팩 | — | — | ① 말풍선, 꾸러미 말풍선 | — |
| 14 | asst_firm → asst_e12 | B | 팩 96·192 | 팩 | — | — | 대결 결과 전, 아웃트로 | — |
| 15 | asst_spark → asst_e01 | B | 팩 96 | 팩 | — | — | 대결 결과 후 | — |
| 16 | asst_shock → asst_e24 | B | 팩 96 | 팩 | — | — | 실격 대비 (이번 결과에선 안 씀) | — |
| 17 | fly_point → fly_e08 | C | 팩 96·192 | 팩 | — | — | 히어로, 대결 전 | — |
| 18 | fly_clip → fly_e10 | C | 팩 96 | 팩 | — | — | 등장인물 | — |
| 19 | fly_magnify → fly_e07 | C | 팩 96 | 팩 | — | — | ② 말풍선 | — |
| 20 | fly_arms → fly_e16 | C | 팩 96·192 | 팩 | — | — | 대결 후 (F), 아웃트로 | — |
| 21 | fly_coffee → fly_e13 | C | 팩 192 | 팩 | — | — | 무승부·작은 패배 대비 | — |
| 22 | fly_cry → fly_e21 | C | 팩 192 | 팩 | — | — | 큰 패배 대비 | — |
| 23 | robo_coin → robo_e16 | D | 팩 96·192 | 팩 | — | — | 히어로, 대결 전 | — |
| 24 | robo_smile → robo_e13 | D | 팩 96 | 팩 | — | — | 등장인물 | — |
| 25 | robo_chart → robo_e07 | D | 팩 96 | 팩 | — | — | "왜" 말풍선 | — |
| 26 | robo_wow → robo_e04 | D | 팩 96 | 팩 | — | — | ④ 말풍선 | — |
| 27 | robo_sigh → robo_e20 | D | 팩 192 | 팩 | — | — | 대결 후 (F) | — |
| 28 | robo_blush → robo_e14 | D | 팩 96·192 | 팩 | — | — | 아웃트로, 실격 대비 | — |
| 29 | robo_happy → robo_e12 | D | 팩 192 | 팩 | — | — | R 결과 대비 | — |
| 30 | robo_meh → robo_e18 | D | 팩 192 | 팩 | — | — | D 결과 대비 | — |
| — | 행동으로 보기 (과자 상자·저울 바늘·노트 격자·고리 던지기) | — | — | 코드 | 직접 | — | 캔버스 | — |

상태 값: `팩` · `넣음`(직접 그림, 페이지에 있음) · `의뢰`(외부, 받을 것) · `받음`(검수 전) · `반영`(페이지에 넣음) · `다시 의뢰`(검수 탈락).

## 3. 새로 그릴 그림 상세

### 3-1. `bg_21a` — 밤의 연구실 계량 실험대 (배경)
| 항목 | 내용 |
|---|---|
| 판 · 크기 | F · 1920×720 (정수배 가능) |
| 제작 경로 | 외부: Genspark |
| 배경 | 그림 전체 |
| 구도 | 인물 없음. 왼쪽 45%는 어두운 벽과 빈 칠판 일부로 단순하게(제목 글자 자리). 오른쪽에 실험대, 저울, 과자 상자, 시험관 선반, 서버 랙 |
| 표정·몸짓 | 없음 |
| 소품 | 전자저울(표시창은 빈 초록 빛 칸), 과자 상자, 실험 노트 더미, 시험관 선반, 빈 칠판 (글자 없음) |
| 빛·분위기 | 남보라 어둠, 보라 조명, 모니터 청록, 시험관 속 분홍·초록 형광, 저울 위로 빛이 모임 |
| 피할 것 | 글자·숫자(저울 표시창 포함), 실존 브랜드 과자 포장, 현미경·초파리 해부 소품(생물 앵커 아님) |
| 대체 글 (alt) | 저울과 과자 상자가 놓인 밤의 연구실 실험대 |
| 대신 쓰는 그림 | CSS 그라데이션 + 벌집 무늬 |

**프롬프트 (복사해서 사용)**
```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, wide 8:3 background, left side simple and calm for title text, details on the right, wide night laboratory with test tube racks, a blank chalkboard, a small server rack, stacks of lab notebooks, and on the workbench a digital weighing scale with a blank glowing green display beside a wooden crate filled with rows of identical round cookies, purple lab light, cyan monitor glow, the light gathering on the scale, no characters, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-2. `sc_21a_hero` — 저울 앞에 모인 네 사람 (히어로 무대)
| 항목 | 내용 |
|---|---|
| 판 · 크기 | E · 1200×800 |
| 제작 경로 | 직접 합성본 페이지에 있음 → 외부: Genspark (P1) |
| 배경 | 그림 전체 |
| 구도 | 가운데 실험대 위 저울과 과자 상자. 왼쪽 초파리(오른쪽을 봄, 저울 위 과자 하나를 의심스럽게 가리킴), 가운데 뒤 박사(턱에 손, 생각), 오른쪽 옆 하루(과자 상자에서 과자를 집어 쟁반에 담음), 오른쪽 Money-Robo(왼쪽을 봄, 금화 하나를 반짝이며 자신만만). 중요한 것은 위쪽 62% 안 |
| 표정·몸짓 | 박사 `doc_think`, 하루 `asst_smile`, 초파리 `fly_point`, 로봇 `robo_coin` |
| 소품 | 저울(빈 표시창), 과자 상자, 쟁반, 금화 하나 (글자 없음) |
| 빛·분위기 | 저울에 빛이 모임, 중간 밝기 |
| 피할 것 | 승패 암시(결과 전 장면), 저울·노트 위 숫자, 금화의 "B" 표시 |
| 대체 글 (alt) | 밤의 연구실 실험대 위 저울과 과자 상자 앞에 네 캐릭터가 선 장면 |
| 대신 쓰는 그림 | 픽셀 연구실 캔버스 + 팩 캐릭터 4명 합성 (`#heroArt`) |

**프롬프트 (복사해서 사용)**
```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 3:2 landscape scene, medium brightness, a night laboratory workbench with a digital weighing scale with a blank glowing display and a wooden crate of identical round cookies, the light gathering on the scale; the Professor, a chibi male scientist with a big head, dark charcoal spiky hair with a white streak at the front, a small low ponytail at the back, very thick bold black eyebrows, teal-framed rectangular glasses, light peach skin, white lab coat over a black vest, black tie and black slacks, standing at the back center with a hand on his chin, thinking; the Fruit Fly, a tiny expressive cartoon fruit fly researcher with a dark charcoal-black segmented insect body, large glossy red compound eyes, a retro dark blue helmet with a yellow-white center stripe and small round side bolts, colorful dangling cables in magenta, purple and blue curving from the back of the helmet, a tiny white lab coat over a black vest, translucent veined wings, six thin black legs with the front pair used like hands, on the left facing right, pointing doubtfully at a cookie on the scale; Haru, a cute anime girl lab assistant, long straight pink hair with navy blue streaks including a thick navy streak down the center of the bangs, two round messy hair buns on top of the head, a small ahoge, big bright blue eyes, light peach skin, wearing a lavender hoodie with white drawstrings over a white t-shirt, under an open white knee-length lab coat, at the right side calmly picking cookies from the crate onto a small tray; MONEY-ROBO, a cute small floating chibi robot with a large glossy rounded-square white head and a small rounded white body with thick black outlines, a black pill-shaped screen face showing golden-yellow pixel eyes and mouth, a small round knob antenna on a short stem, stubby rounded fingerless arms, no legs, a black oval chest panel with a bright cyan pill-shaped core light, hovering above a small dark oval shadow, on the right facing left with half-closed confident eyes beside one shiny plain gold coin, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-3. `sc_21a_outro` — 실험이 끝난 밤 (아웃트로)
| 항목 | 내용 |
|---|---|
| 판 · 크기 | E · 1200×800 |
| 제작 경로 | 직접 합성본 페이지에 있음 → 외부 선택 (P2) |
| 배경 | 그림 전체 |
| 구도 | 승자 초파리가 앞·크게 팔짱(뿌듯), 옆에 넓은 고리와 좁은 고리가 말뚝에 걸린 작은 장난감 고리 던지기 세트. 박사는 가운데 뒤에서 손바닥 위 보라 불꽃, Money-Robo는 머쓱하게 볼에 분홍 빗금(조롱 아님, 인정하는 몸짓), 하루는 한쪽에서 주먹 쥐고 응원. 창밖에 달 |
| 표정·몸짓 | `fly_arms`, `doc_magic`, `robo_blush`, `asst_firm` |
| 소품 | 고리 던지기 말뚝과 고리 2개(넓은 것·좁은 것), 저울, 과자 쟁반 (글자 없음) |
| 빛·분위기 | 늦은 밤, 보라 조명, 달빛 |
| 피할 것 | 패자 조롱, 숫자·글자, 금화 "B" 표시 |
| 대체 글 (alt) | 실험이 끝난 밤의 연구실에서 초파리 연구원이 앞에 서고 Money-Robo가 머쓱해하는 장면 |
| 대신 쓰는 그림 | 픽셀 연구실(밤·달) + 팩 캐릭터 합성 (`#outroArt`) |

**프롬프트 (복사해서 사용)**
```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 3:2 landscape scene, medium brightness, late night in the laboratory with a moon in the window, a workbench with a weighing scale and a small tray of cookies, a toy ring toss peg on the bench with one wide ring and one narrow ring around it; the Fruit Fly, a tiny expressive cartoon fruit fly researcher with a dark charcoal-black segmented insect body, large glossy red compound eyes, a retro dark blue helmet with a yellow-white center stripe and small round side bolts, colorful dangling cables in magenta, purple and blue curving from the back of the helmet, a tiny white lab coat over a black vest, translucent veined wings, six thin black legs with the front pair used like hands, in the front and larger, arms crossed with a proud sparkle; the Professor, a chibi male scientist with a big head, dark charcoal spiky hair with a white streak at the front, a small low ponytail at the back, very thick bold black eyebrows, teal-framed rectangular glasses, light peach skin, white lab coat over a black vest, black tie and black slacks, at the back center laughing with small purple flames above both palms; MONEY-ROBO, a cute small floating chibi robot with a large glossy rounded-square white head and a small rounded white body with thick black outlines, a black pill-shaped screen face showing golden-yellow pixel eyes and mouth, a small round knob antenna on a short stem, stubby rounded fingerless arms, no legs, a black oval chest panel with a bright cyan pill-shaped core light, hovering above a small dark oval shadow, on the right with drooping eyes and pink blush lines, sheepish but accepting; Haru, a cute anime girl lab assistant, long straight pink hair with navy blue streaks including a thick navy streak down the center of the bangs, two round messy hair buns on top of the head, a small ahoge, big bright blue eyes, light peach skin, wearing a lavender hoodie with white drawstrings over a white t-shirt, under an open white knee-length lab coat, at the side with a determined cheering fist, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-4. `cut_21a_ringtoss` — 말뚝은 그대로, 고리가 날아간다 (④칸 컷, 선택)
| 항목 | 내용 |
|---|---|
| 판 · 크기 | G · 960×540 |
| 제작 경로 | 외부: Genspark (P2, 선택) |
| 배경 | 그림 전체 |
| 구도 | 가운데 빛나는 금색 말뚝 하나(모평균). 하루가 왼쪽에서 고리를 던지고, 여러 고리가 공중에 떠 있다. 대부분은 말뚝에 걸리고(초록 빛 테두리) 한두 개는 바닥에 떨어진다(빨간 빛 테두리). 초파리가 오른쪽 아래에서 클립보드에 표시 |
| 표정·몸짓 | 하루: 집중한 눈으로 던지는 자세 / 초파리 `fly_clip` |
| 소품 | 말뚝, 고리 여러 개, 클립보드 (글자 없음) |
| 빛·분위기 | 말뚝에 빛이 모임 |
| 피할 것 | 말뚝이 움직이는 듯한 표현(말뚝은 고정), 숫자 |
| 대체 글 (alt) | 고정된 말뚝에 고리를 던져 대부분 걸리고 일부가 빗나가는 장면 |
| 대신 쓰는 그림 | 없음 (`#c4b` 캔버스가 같은 역할) |

**프롬프트 (복사해서 사용)**
```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 16:9 illustration panel, a single glowing golden peg fixed upright in the center of the lab floor, several rings flying through the air toward it, most rings landing around the peg with a soft green glow and one or two rings falling on the floor beside it with a soft red glow; Haru, a cute anime girl lab assistant, long straight pink hair with navy blue streaks including a thick navy streak down the center of the bangs, two round messy hair buns on top of the head, a small ahoge, big bright blue eyes, light peach skin, wearing a lavender hoodie with white drawstrings over a white t-shirt, under an open white knee-length lab coat, on the left throwing a ring with a focused look; the Fruit Fly, a tiny expressive cartoon fruit fly researcher with a dark charcoal-black segmented insect body, large glossy red compound eyes, a retro dark blue helmet with a yellow-white center stripe and small round side bolts, colorful dangling cables in magenta, purple and blue curving from the back of the helmet, a tiny white lab coat over a black vest, translucent veined wings, six thin black legs with the front pair used like hands, at the lower right writing on a blank clipboard, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-5. `thumb_21a` — 목차 카드 썸네일
| 항목 | 내용 |
|---|---|
| 판 · 크기 | I · 600×400 |
| 제작 경로 | 직접: `bg_21a`를 3:2로 오른쪽 기준 자르기. 받기 전에는 히어로 합성 무대를 600×400으로 캡처 |
| 대체 글 (alt) | 저울과 과자 상자가 있는 연구실 — 2.1.a 점추정과 신뢰구간 |

### 3-6. `og_21a` — 공유 미리보기
| 항목 | 내용 |
|---|---|
| 판 · 크기 | K · 1200×630 |
| 제작 경로 | 직접: 배경(bg_21a 또는 CSS) + 팩 `fly_e08`, `robo_e16` + 제목 "점추정과 신뢰구간"을 HTML/SVG로 얹어 합성 |
| 대체 글 (alt) | 2.1.a 점추정과 신뢰구간 페이지 미리보기 |

## 4. 일관성 지침
- 참고 이미지: 공식 저장소 `refs/original/keyart_rivals.png`(넷이 함께) + 장면에 나오는 캐릭터의 팩 표정 원본 PNG (`images/doctor/E09_thinking.png`, `images/haru/E13_neutral.png`, `images/fruitfly/E08_guiding.png`, `images/money_robo/E16_proud.png`, 아웃트로는 `images/fruitfly/E16_proud.png`, `images/money_robo/E14_*.png`, `images/doctor/E16_proud.png`, `images/haru/E12_*.png`)
- 같은 캐릭터는 같은 세션에서, 시드 고정 가능하면 고정: 박사 2101, 조수 2102, 초파리 2103, 로봇 2104
- 표정만 바꿀 때 추가 문장: *same character, same size and position, only change the facial expression and pose to ...*
- 투명 배경이 안 되면: *solid flat #00ff00 background*

## 5. 넘겨받은 뒤 처리
SKILL 18-15 절차 그대로 (키 맞추기 → 눈으로 검수 → `--ingest` → 페이지에 넣기 → 상태 갱신 → 점검 → 전달).
```bash
python3 build_character_pack.py --ingest 받은폴더/ --plates bg_21a=F,sc_21a_hero=E,sc_21a_outro=E,cut_21a_ringtoss=G --out received_21a
```
- `bg_21a`는 `.hero-bg`의 CSS 배경 위에, `sc_21a_hero`·`sc_21a_outro`는 `.stage` 안 캔버스 대신 `<img>`로 넣는다. 합성본(캔버스·팩 캐릭터)은 지우지 말고 `SPRITE`에 키가 없을 때만 보이게 둔다.

## 6. 체크리스트
- [x] HTML의 모든 `data-img` 키가 이 명세서에 있음 (bg_21a, sc_21a_hero, sc_21a_outro, 표정 팩 키)
- [x] 대결 결과 후 표정이 5-8절 표와 일치 (F: fly_arms, robo_sigh, asst_spark, doc_judge)
- [x] 결과 전 그림에 승패 암시 없음 (fly_point, robo_coin, asst_firm)
- [x] 모든 외부 프롬프트에 18-4 고정 외형 영어 묘사와 금지 구절
- [x] 팩에 있는 표정을 "새로 그림"에 넣지 않음
- [x] 장소가 B 연구실 앵커와 일치, 현미경·초파리 해부 소품 없음
- [x] P1 2장 (6장 이하)
- [x] 페이지 그림 합계: 팩 96px 114 KB + 192px 약 160 KB(원본) → 400 KB 이하

## 8. 외부 의뢰 묶음 (Genspark에 그대로 붙여 넣기)

같은 페이지 그림은 **한 세션에서 이 순서대로** 의뢰한다(배경 → 장면 → 컷).

### 의뢰 1/3 · `bg_21a`
- **올릴 참고 이미지:** 없음 (배경만)
- **크기·비율:** 1920×720 (8:3) 이상
- **배경:** 그림 전체
- **받을 파일 이름:** `bg_21a.png`
- **프롬프트:** 3-1의 프롬프트 그대로
- **네거티브 (넣을 칸이 있으면):** `blurry, smooth vector art, 3D render, photorealistic, anti-aliased painting, inconsistent character, off-model, text, letters, watermark`
- **확인할 것:** 저울 표시창에 숫자가 나오면 다시. 과자 상자에 상표가 그려지면 다시.

### 의뢰 2/3 · `sc_21a_hero`
- **올릴 참고 이미지:** `refs/original/keyart_rivals.png`, `images/fruitfly/E08_guiding.png`, `images/money_robo/E16_proud.png`, `images/doctor/E09_thinking.png`
- **크기·비율:** 1200×800 (3:2) 이상
- **배경:** 그림 전체
- **받을 파일 이름:** `sc_21a_hero.png`
- **프롬프트:** 3-2의 프롬프트 그대로
- **네거티브:** 위와 같음
- **확인할 것:** 박사 안경이 둥글게 나오면 다시(청록 사각 테). 초파리와 로봇이 서로 마주 보는지. 금화에 "B"가 있으면 다시.

### 의뢰 3/3 · `sc_21a_outro` (선택) · `cut_21a_ringtoss` (선택)
- **올릴 참고 이미지:** `refs/original/keyart_rivals.png`, `images/fruitfly/E16_proud.png`, `images/money_robo/E14_*.png` / 컷은 `images/haru/E13_neutral.png`, `images/fruitfly/E10_*.png`
- **크기·비율:** 1200×800 (3:2) / 960×540 (16:9) 이상
- **배경:** 그림 전체
- **받을 파일 이름:** `sc_21a_outro.png`, `cut_21a_ringtoss.png`
- **프롬프트:** 3-3, 3-4의 프롬프트 그대로
- **확인할 것:** 아웃트로에서 Money-Robo가 우스꽝스럽게 망가지거나 조롱당하지 않는지. 컷에서 말뚝이 움직이는 것처럼 보이지 않는지.

## 7. 매니페스트
```json
{
  "page": "2-1a_point_interval_estimation",
  "anchor": "B:night-lab-weighing-bench",
  "season": "default",
  "duel": {"result": "F", "gap": 0.505, "metric": "useful-interval-rate", "fly": 0.925, "robo": 0.420},
  "images": [
    {"key":"bg_21a","plate":"F","size":[1920,720],"maker":"external","tool":"genspark","status":"requested","priority":"P1","slot":"hero-bg","fallback":"css","alt":"저울과 과자 상자가 놓인 밤의 연구실 실험대"},
    {"key":"sc_21a_hero","plate":"E","size":[1200,800],"maker":"external","tool":"genspark","status":"requested","priority":"P1","slot":"hero-stage","fallback":"composite","alt":"밤의 연구실 실험대 위 저울과 과자 상자 앞에 네 캐릭터가 선 장면"},
    {"key":"sc_21a_outro","plate":"E","size":[1200,800],"maker":"claude","status":"placed","priority":"P2","slot":"outro-stage","fallback":"composite","alt":"실험이 끝난 밤의 연구실에서 초파리 연구원이 앞에 서고 Money-Robo가 머쓱해하는 장면","external_optional":true},
    {"key":"cut_21a_ringtoss","plate":"G","size":[960,540],"maker":"external","tool":"genspark","status":"requested","priority":"P2","slot":"lv4-cut","fallback":"none","alt":"고정된 말뚝에 고리를 던져 대부분 걸리고 일부가 빗나가는 장면","optional":true},
    {"key":"thumb_21a","plate":"I","size":[600,400],"maker":"claude","status":"planned","priority":"P2","slot":"index-card","alt":"저울과 과자 상자가 있는 연구실 — 2.1.a 점추정과 신뢰구간"},
    {"key":"og_21a","plate":"K","size":[1200,630],"maker":"claude","status":"planned","priority":"P3","slot":"og","alt":"2.1.a 점추정과 신뢰구간 페이지 미리보기"},
    {"key":"doc_think","pack":"doc_e09","plate":"A","size":[96,192],"status":"pack","slot":"hero","alt":""},
    {"key":"doc_front","pack":"doc_e08","plate":"A","size":96,"status":"pack","slot":"cast,summary","alt":""},
    {"key":"doc_board","pack":"doc_e07","plate":"A","size":96,"status":"pack","slot":"big","alt":""},
    {"key":"doc_magic","pack":"doc_e16","plate":"A","size":[96,192],"status":"pack","slot":"lv3,outro","alt":""},
    {"key":"doc_judge","pack":"doc_e10","plate":"A","size":96,"status":"pack","slot":"duel-verdict","alt":""},
    {"key":"asst_smile","pack":"asst_e13","plate":"B","size":[96,192],"status":"pack","slot":"hero,cast","alt":""},
    {"key":"asst_e10","pack":"asst_e10","plate":"B","size":96,"status":"pack","slot":"lv1,export","alt":""},
    {"key":"asst_firm","pack":"asst_e12","plate":"B","size":[96,192],"status":"pack","slot":"duel-before,outro","alt":""},
    {"key":"asst_spark","pack":"asst_e01","plate":"B","size":96,"status":"pack","slot":"duel-after","alt":""},
    {"key":"asst_shock","pack":"asst_e24","plate":"B","size":96,"status":"pack","slot":"duel-foul-reserve","alt":""},
    {"key":"fly_point","pack":"fly_e08","plate":"C","size":[96,192],"status":"pack","slot":"hero,duel-before","alt":""},
    {"key":"fly_clip","pack":"fly_e10","plate":"C","size":96,"status":"pack","slot":"cast","alt":""},
    {"key":"fly_magnify","pack":"fly_e07","plate":"C","size":96,"status":"pack","slot":"lv2","alt":""},
    {"key":"fly_arms","pack":"fly_e16","plate":"C","size":[96,192],"status":"pack","slot":"duel-after,outro","alt":""},
    {"key":"fly_coffee","pack":"fly_e13","plate":"C","size":192,"status":"pack","slot":"duel-reserve","alt":""},
    {"key":"fly_cry","pack":"fly_e21","plate":"C","size":192,"status":"pack","slot":"duel-reserve","alt":""},
    {"key":"robo_coin","pack":"robo_e16","plate":"D","size":[96,192],"status":"pack","slot":"hero,duel-before","alt":""},
    {"key":"robo_smile","pack":"robo_e13","plate":"D","size":96,"status":"pack","slot":"cast","alt":""},
    {"key":"robo_chart","pack":"robo_e07","plate":"D","size":96,"status":"pack","slot":"why","alt":""},
    {"key":"robo_wow","pack":"robo_e04","plate":"D","size":96,"status":"pack","slot":"lv4","alt":""},
    {"key":"robo_sigh","pack":"robo_e20","plate":"D","size":192,"status":"pack","slot":"duel-after","alt":""},
    {"key":"robo_blush","pack":"robo_e14","plate":"D","size":[96,192],"status":"pack","slot":"outro","alt":""},
    {"key":"robo_happy","pack":"robo_e12","plate":"D","size":192,"status":"pack","slot":"duel-reserve","alt":""},
    {"key":"robo_meh","pack":"robo_e18","plate":"D","size":192,"status":"pack","slot":"duel-reserve","alt":""}
  ],
  "character_pack": {"repo":"adminmrobo/fruitfly-lab-expressions","commit":"ea5da3f"},
  "status_values": "pack | placed(직접, 넣음) | planned(직접, 만들 예정) | requested(의뢰) | received(받음) | applied(반영) | rejected(다시 의뢰)"
}
```
