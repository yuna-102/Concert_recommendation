# 지방 공연장을 위한 공연 추천 시스템
> 공연장 별로 최적의 공연 유형 / 공연 시간 추천

## 분석 배경
- 2010년 이후 전국의 공연시설은 꾸준히 증가해옴.
- 그러나 지방의 경우 공연시설의 가동률이 매우 낮음.
- 지방 공연장에서 주민들이 만족할 만한 공연을 유치함으로써, 공연시설의 활성화를 유도.

## 사용 데이터
- 국민문화향수실태조사 데이터 (2016-2019)
  - 관람자별 공연 만족도 파악
  - 관람자 인구 특성 (성별, 연령대 등) 파악
  - 관람자 공연 관람 지역 파악
- 공연 DB (2015-2019)
- 공연장 등록 현황 (2019)
- 전국 인구 통계
  - 시군구동별 거주자 성별, 연령 데이터 파악

## 분석 방법
- 공연 만족도 예측
  - 관람자 인구 특성, 관람 지역, 공연 장르로 공연 만족도 예측
  - 로지스틱 회귀분석 모델 이용
  - Accuracy: 0.88 / F1-score: 0.94
- 최적화 모델 적용
  - 앞선 로지스틱 회귀분석 모델을 활용
  - 지역 인구특성을 바탕으로 만족도를 최적화 하는 공연 유형 / 시간대 반환
- 자동화
  - 공연장 DB, 전국 인구통계 데이터와 연동
  - 공연장 이름 입력시 근처의 인구 특성을 자동 추출

## Implications
- 대부분의 경우 평일과 주말에 권장되는 공연의 종류가 상이함
- 비슷한 성격의 공연장이어도 지역에 따라 권장되는 공연의 종류/시간이 매우 다름
 
