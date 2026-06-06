# 파이썬을 활용한 공학 데이터 필터링 및 통계 분석

## 오늘 배운 내용
- 리스트 컴프리헨션(List Comprehension)을 활용한 특정 조건 데이터 필터링
- 특정 임계치(Threshold)를 넘는 실험 데이터만 추출하고 평균값 계산하기

## 코드 연습
```python
# 화학 반응 실험에서 수집된 온도 데이터 (단위: °C)
raw_temperatures = [180, 220, 195, 240, 175, 210, 255, 190, 230]

# 200°C 이상의 고온 반응 데이터만 필터링
high_temp_data = [temp for temp in raw_temperatures if temp >= 200]

# 결과 계산
average_high_temp = sum(high_temp_data) / len(high_temp_data)

print(f"전체 실험 횟수: {len(raw_temperatures)}회")
print(f"200°C 이상 고온 데이터: {high_temp_data}")
print(f"고온 반응의 평균 온도: {average_high_temp:.2f}°C")
