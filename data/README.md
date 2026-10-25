# 데이터 배치 방법

대회 제공 데이터와 가공 데이터는 대회 규정에 따라 이 저장소에 포함하지 않습니다.
아래 위치에 파일을 넣은 뒤 노트북을 00번부터 순서대로 실행하세요. `data/processed/`는 노트북이 자동으로 만듭니다.

```
data/
├── raw/                         ← 대회 제공 데이터 (저장소 미포함)
│   ├── card/
│   │   ├── 신한카드_빅콘테스트2026_데이터1.txt
│   │   └── 신한카드_빅콘테스트2026_데이터2.txt
│   ├── sk/                      SK 유동인구 원본
│   ├── flow_time_gangnam_chuncheon_202507_202512.csv
│   └── flow_age_gangnam_chuncheon_202507_202512.csv
├── processed/                   ← 노트북 실행 결과 (저장소 미포함)
└── external/
    ├── OBS_ASOS_TIM_20261001145432.csv          기상청 ASOS 시간자료 (포함)
    ├── chuncheon_golf_legoland_coordinates_v3.csv  골프장·레고랜드 좌표 (포함)
    ├── adm/adm_gangnam_chuncheon_2025.geojson   행정동 경계 (포함)
    └── store/                   ← 상가정보 (용량 초과로 미포함)
        ├── 소상공인시장진흥공단_상가(상권)정보_서울_202506.csv
        └── 소상공인시장진흥공단_상가(상권)정보_강원_202506.csv
```

- 상가정보: 공공데이터포털에서 '소상공인시장진흥공단_상가(상권)정보' 2025년 6월 기준 서울·강원 파일을 내려받아 `data/external/store/`에 넣습니다.
- 골프장·레고랜드 좌표 파일은 09b 노트북이 `data/processed/`에서 읽으므로, 실행 전 `data/processed/`에도 복사해 둡니다.
