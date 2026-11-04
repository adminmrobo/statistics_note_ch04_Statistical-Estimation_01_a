# 점추정과 신뢰구간 — 연구실 저울로 모평균 잡기

**2. 통계적 추정 · 2.1.a** 해설 페이지

> 과자 100개만 재고, 1만 개의 평균 무게를 어디까지 말할 수 있을까?

페이지 주소: https://adminmrobo.github.io/statistics_note_ch04_Statistical-Estimation_01_a/

박사·하루·초파리 연구원·주판봇 네 캐릭터와 함께 표본을 직접 뽑아 보면서 점추정, 표본평균의 분포, 신뢰구간을 배우는 인터랙티브 해설 페이지입니다.

## 이 페이지에서 하는 것

| 칸 | 내용 | 직접 돌려 보는 실험 |
|---|---|---|
| ① 모집단·표본·통계량 | 모수는 모르는 값, 통계량은 계산한 값 | 과자 1만 개 히스토그램 위에 표본 올리기 |
| ② 점추정 | 모평균 ≈ 표본평균, 표본분산은 n − 1로 나누는 이유 | 반복 점추정, 분산 나누기 비교 (2,000번) |
| ③ 표본평균의 분포 | 표준오차 σ/√n | 표본평균 100개 쌓기 |
| ④ 신뢰구간 | x̄ ± z·σ/√n, 신뢰수준 90·95·99% | 구간 100개 만들기, 고리 던지기 |
| 대결 | 신뢰수준은 높을수록 좋을까? (95% vs 99%) | 200번 반복 계산으로 승패 결정 |

확인 퀴즈 10문항, 용어 말풍선, 지식 색인, 온톨로지·서지 꾸러미(JSON-LD·Turtle·CSV·CSL-JSON·BibTeX·RIS ZIP)가 들어 있습니다.

## 파일

```
.
├── index.html   # 해설 페이지 (HTML 파일 하나, 그림·데이터 모두 포함)
├── .nojekyll    # Jekyll 처리 끄기
└── README.md
```

- 서버, 설치, 외부 라이브러리가 필요 없습니다. 외부 요청은 글꼴(IBM Plex Sans KR) 하나뿐입니다.
- `index.html`을 내려받아 더블클릭해도 그대로 열립니다.

## GitHub Pages로 공개하기

1. 저장소 `statistics_note_ch04_Statistical-Estimation_01_a`에 이 폴더의 파일을 모두 올립니다. `.nojekyll`(숨김 파일)도 함께 올립니다.
   ```bash
   git init
   git add .
   git commit -m "2.1.a 점추정과 신뢰구간 공개"
   git branch -M main
   git remote add origin https://github.com/adminmrobo/statistics_note_ch04_Statistical-Estimation_01_a.git
   git push -u origin main
   ```
2. 저장소 **Settings → Pages**에서 Source를 **Deploy from a branch**, Branch를 **main / (root)**로 고르고 Save를 누릅니다.
3. 1~2분 뒤 위 페이지 주소에서 열립니다.

## 이 페이지 인용하기

안상선 (2026). 점추정과 신뢰구간 — 연구실 저울로 모평균 잡기. AI 연구실 해설 대시보드 2.1.a, v1.0. https://adminmrobo.github.io/statistics_note_ch04_Statistical-Estimation_01_a/

## 출처와 표시

- 주 자료: 강의 노트 「2.1.a 통계적 추정 : 점추정과 신뢰구간」 (Notion, mrobo2016)
- 신뢰구간 해석: Neyman, J. (1937). *Philosophical Transactions of the Royal Society of London. Series A*. DOI [10.1098/rsta.1937.0005](https://doi.org/10.1098/rsta.1937.0005)
- 캐릭터 그림: adminmrobo/fruitfly-lab-expressions (커밋 ea5da3f). 페이지 안에 넣었으므로 외부에서 불러오지 않습니다.
- 과자 무게 등 시뮬레이션 데이터는 설명용 모형입니다. 실제 데이터가 아닙니다.

저자: 안상선 · AI 보조 제작

라이선스: _정해지면 적어 넣을 것_
