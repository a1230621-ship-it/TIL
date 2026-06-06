# 파이썬 Matplotlib을 활용한 실험 데이터 시각화 (그래프 그리기)

## 오늘 배운 내용
- 파이썬의 대표적인 시각화 라이브러리 `matplotlib.pyplot` 사용법 학습
- 시간에 따른 특정 성분의 농도 변화 데이터를 선 그래프(Line Plot)로 구현하기
- 그래프에 제목(Title), 축 이름(Labels), 범례(Legend)를 추가하여 가독성 높이기

## 코드 연습
```python
import matplotlib.pyplot as plt

# 가상의 반응 시간에 따른 생성물 농도 데이터 (시간: 분, 농도: mol/L)
time = [0, 10, 20, 30, 40, 50, 60]
concentration = [0.0, 0.15, 0.32, 0.55, 0.72, 0.85, 0.92]

# 그래프 생성
plt.plot(time, concentration, marker='o', color='b', linestyle='-', label='Product A')

# 그래프 스타일 세팅 (제목 및 축 이름)
plt.title('Reaction Kinetics: Concentration over Time')
plt.xlabel('Time (min)')
plt.ylabel('Concentration (mol/L)')

# 범례 및 그리드(눈금선) 표시
plt.legend()
plt.grid(True)

# 그래프 출력 명령 (로컬 환경 실행 시 창이 뜸)
# plt.show()
