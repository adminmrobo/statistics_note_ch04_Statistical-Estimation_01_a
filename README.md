# 통계적 추정 연구실 — AI 연구실 해설 대시보드 2장

표본 몇 개로 전체를 얼마나 말할 수 있을까?
박사·하루·초파리 연구원·Money-Robo 네 캐릭터와 함께 **점추정 → 정규분포 → t-분포 → 신뢰구간 실습**을 직접 돌려 보며 배우는 인터랙티브 해설 페이지 모음입니다.

- 모든 페이지는 **HTML 파일 하나**입니다. 서버, 설치, 외부 라이브러리가 필요 없습니다(외부 요청은 글꼴 하나뿐).
- 시뮬레이션은 시드를 고정했으므로 누가 열어도 같은 결과가 나옵니다.
- 페이지 끝의 "온톨로지·서지 꾸러미"에서 지식 그래프(JSON-LD·Turtle·CSV)와 참고문헌(CSL-JSON·BibTeX·RIS)을 ZIP으로 내려받을 수 있습니다.

## 목차

| 번호 | 제목 | 종류 | 상태 |
|---|---|---|---|
| 2.1.a | [통계적 추정 : 점추정과 신뢰구간](pages/2-1a_point_interval_estimation.html) | 개념 | 공개 |
| 2.1.b | (실습) 통계적 추정 : 점추정과 신뢰구간 | 실습 | 준비 중 |
| 2.2.a | 통계적 추정 : 정규분포 (1) | 개념 | 준비 중 |
| 2.2.b | (실습) 정규분포의 사례 | 실습 | 준비 중 |
| 2.2.c | (참고) 중심극한 정리 | 참고 | 준비 중 |
| 2.2.d | (사례 학습) 신뢰구간의 추정 사례 | 사례 학습 | 준비 중 |
| 2.3 | 확률분포와 통계적 추론 : t-분포 외 (1) | 개념 | 준비 중 |
| 2.4 | 표본의 분포와 모수 추정 (1) | 개념 | 준비 중 |
| 2.5 | (참고) 표본의 크기와 자유도 (1) | 참고 | 준비 중 |
| 2.6 | 신뢰구간의 추정 : 코드 실습 (복습) | 실습 | 준비 중 |
| 2.7 | (실습) t-분포 : "맥주"효모 추정 | 실습 | 준비 중 |
| 2.8 | (실습) 의료 데이터 | 실습 (추가) | 준비 중 |
| 2.9 | (실습) 신뢰구간 추정 종합 | 실습 (추가) | 준비 중 |

## 폴더 구조

```
.
├── index.html              # 시리즈 목차 (GitHub Pages 첫 화면)
├── .nojekyll               # Jekyll 처리 끄기 (파일을 그대로 내보냄)
├── README.md
├── pages/                  # 해설 페이지 (페이지마다 HTML 하나)
│   └── 2-1a_point_interval_estimation.html
├── specs/                  # 이미지 제작 명세서 (그림 의뢰용)
│   └── IMG_2-1a_point_interval_estimation.md
└── data/
    └── KG_00_registry.json # 시리즈 등록부: 개념·문헌 ID 목록
```

## GitHub Pages로 공개하기

1. GitHub에서 새 저장소를 만들고 이 폴더의 파일을 모두 올립니다. `.nojekyll`(점으로 시작하는 숨김 파일)도 함께 올려야 합니다.
   ```bash
   git init
   git add .
   git commit -m "통계적 추정 2.1.a 공개"
   git branch -M main
   git remote add origin https://github.com/{계정}/{저장소}.git
   git push -u origin main
   ```
2. 저장소 **Settings → Pages**로 갑니다.
3. **Build and deployment**의 Source를 **Deploy from a branch**로, Branch를 **main / (root)**로 고르고 Save를 누릅니다.
4. 1~2분 뒤 `https://{계정}.github.io/{저장소}/`에서 목차가 열립니다.

공개 주소가 정해지면 각 페이지의 `page-meta` 블록과 `<meta name="citation_*">`의 `url` 칸을 채우면 인용 정보가 완성됩니다(지금은 빈칸).

## 새 페이지를 추가할 때

1. 새 페이지 HTML을 `pages/`에 넣습니다. 파일 이름은 `{번호}_{영문 슬러그}.html` (예: `2-1b_estimation_lab.html`).
2. 그 페이지의 이미지 명세서는 `specs/`에 넣습니다.
3. `index.html` 안의 `PAGES` 목록에서 해당 줄의 `file`에 경로를 적습니다. 대결이 있으면 `duel` 항목도 채웁니다. 목차·진행 막대·대결 기록이 자동으로 바뀝니다.
   ```js
   {no:'2.1.b', title:'(실습) 통계적 추정 : 점추정과 신뢰구간', kind:'lab', file:'pages/2-1b_estimation_lab.html',
    summary:'한 줄 소개', duel:{q:'…', fly:'…', robo:'…', metric:'…', res:'R', score:'0.00 : 0.00'}},
   ```
4. 새 페이지에서 생긴 개념·문헌 ID는 `data/KG_00_registry.json`에 더합니다(같은 개념은 같은 ID).
5. 이 README의 목차 표에서 상태를 "공개"로 바꾸고 링크를 겁니다.
6. 새 페이지의 바닥글 "다음 페이지"와, 앞 페이지의 "다음 페이지" 칸을 서로 링크로 잇습니다.

## 대결 기록

| 페이지 | 대결 질문 | 초파리 | Money-Robo | 결과 |
|---|---|---|---|---|
| 2.1.a | 신뢰수준은 높을수록 좋을까? (같은 n=100, 폭 5g 요청) | 95% | 99% | 초파리 승 (0.925 : 0.420) |

시리즈 전체에서 한쪽만 이기지 않도록 균형을 맞춥니다. 복잡하거나 데이터가 충분한 주제에서는 Money-Robo가 이기는 편이 있어야 합니다.

## 출처와 표시

- 주 자료: 강의 노트 「2.1.a 통계적 추정 : 점추정과 신뢰구간」 (Notion, mrobo2016)
- 신뢰구간 해석: Neyman, J. (1937). *Philosophical Transactions of the Royal Society of London. Series A*. DOI [10.1098/rsta.1937.0005](https://doi.org/10.1098/rsta.1937.0005)
- 캐릭터 그림: [adminmrobo/fruitfly-lab-expressions](https://github.com/adminmrobo/fruitfly-lab-expressions) (커밋 ea5da3f). 페이지 안에 base64로 넣었으므로 외부에서 불러오지 않습니다.
- 페이지 속 과자 무게 등 시뮬레이션 데이터는 설명용 모형입니다. 실제 데이터가 아닙니다.

저자: 안상선 · AI 보조 제작 (AI 연구실 해설 대시보드 스킬 v1.7)

라이선스: _정해지면 적어 넣을 것_
