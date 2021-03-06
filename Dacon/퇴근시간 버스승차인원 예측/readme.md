## 퇴근시간 버스승차인원 예측

(회귀/RMSE/rf,xgb,lgbm/submission 간 앙상블/주소변환툴 Geocoder-Xr)

- 1. 변수 생성
    - 내부 변수 생성
        - 요일변수            
        - 요일별 평균탑승객 수            
        - 버스종류별 평균 탑승객 수   
        - 날짜별 오전시간에 탑승한 총 승객수

    - 도메인변수 생성
        - 배차간격
        - 배차간격 평균
        - 고수요 예상 정류장(학교/터미널/환승/공항)
        - 연휴            
        - 오전 시간(6시~12시)승차 승객 수의 합계    
        - 오전 시간(6시~12시)하차 승객 수의 합계
        - 카테고리별 승객 수의 합
        - 카테고리별 승객 수의 비율 
            
    - 외부 변수 생성
        - 좌표를 활용한 변수 # geopy.distance.geodesic((위도1, 경도1), (위도2, 경도2))
            import geopy.distance
            # 거리 구하기 : geopy.distance.geodesic((위도1, 경도1), (위도2, 경도2))
        - 비 (0,1)
        - 좌표, 동, 시 
        - 각 동(읍, 면별) 직업, 소득, 소비, 부동산 관련 변수의 평균, 합계, 비율
            
- 2. 라벨/원핫 인코딩
    
- 3. 모델(rf, xgb, lgbm)
    
- 4. 교차검증(scoring = 'neg_mean_squared_error')
    
- 5. 하이퍼파라미터 튜닝(GridSearchCV/RandomizedSearchCV)
    
- 6. 최종 모델 구축
    
- 7. submission 간 앙상블(결괏값 간 상관계수 확인)
