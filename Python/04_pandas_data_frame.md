# 파이썬 Pandas 라이브러리를 활용한 대량의 실험 데이터 핸들링

## 오늘 배운 내용
- `pandas` 라이브러리의 핵심 구조인 데이터프레임(DataFrame) 이해하기
- 딕셔너리 구조를 데이터프레임으로 변환하고, 표(Table) 형태로 다루기
- 특정 열(Column)의 최댓값, 최솟값, 평균값 등 요약 통계량(`describe()`) 한 번에 계산하기

## 코드 연습
```python
import pandas as pd

# 실험 샘플 데이터 생성 (샘플 번호, 첨부제 비율, 배터리 효율 %)
experiment_dict = {
    'Sample_ID': ['S-01', 'S-02', 'S-03', 'S-04', 'S-05'],
    'Additive_Ratio_%': [0.5, 1.0, 1.5, 2.0, 2.5],
    'Efficiency_%': [85.4, 88.2, 91.5, 89.1, 86.3]
}

# 1. 판다스 데이터프레임으로 변환
df = pd.DataFrame(experiment_dict)

# 2. 특정 조건 필터링: 효율이 88% 이상인 우수 샘플만 추출
high_efficiency_samples = df[df['Efficiency_%'] >= 88.0]

print("--- [전체 데이터프레임 구조] ---")
print(df)
print("\n--- [효율 88% 이상 샘플 필터링] ---")
print(high_efficiency_samples)

print("\n--- [실험 결과 데이터 요약 통계] ---")
# 평균, 표준편차, 최댓값 등을 자동으로 계산해 주는 기능
print(df['Efficiency_%'].describe())
