# tryagain

> 스케이트는 끊임없는 자기혐오

내 주변 스케이트보드 스팟 & 트릭 라이브러리

[→ 열어보기](https://currenjin.github.io/tryagain/)

---

## 기능

### Spots
- 전국 스케이트보드 스팟/파크/샵 지도
- 카테고리 필터 (공공파크, 사설파크, 스팟, 샵, 즐겨찾기)
- 검색, 내 위치 기반 거리순 정렬, 반경 필터
- 즐겨찾기, 네이버지도/카카오맵 길찾기 연동

### Tricks
- 스케이트보드 트릭 라이브러리
- 난이도 필터 (입문/초급/중급/고급)
- 카테고리 필터 (flat/ledge/rail/transition)
- 검색어 + 필터 동시 적용
- 정렬 옵션 (난이도순, 이름순)
- 트릭별 핵심 포인트, 자주 망하는 포인트, 연습 드릴, 선행 트릭 정보

## 구조

```
tryagain/
├── crawler/
│   └── ksbf.py        # ksbf.kr 크롤러
└── docs/              # GitHub Pages
    ├── index.html
    ├── app.js
    ├── style.css
    └── data/
        ├── spots.json
        └── tricks.json
```

## 데이터 업데이트

```bash
python crawler/ksbf.py
```

매주 월요일 자동 업데이트 (GitHub Actions).

## 로컬 실행

```bash
cd docs && python -m http.server 8000
```
