# AIFFEL_quest_rs

# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 정현우
- 리뷰어 : 강지수


# PRT(Peer Review Template)
- [x]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 네. 프로젝트 1, 2 모두 문제에서 요구한 핵심 절차가 포함되어 있습니다.
    - 프로젝트 1 최종 test 데이터에 대한 MSE는 약 `2864.53`으로, 프로젝트 기준인 `MSE 3000 이하`를 만족했습니다.
      <img width="730" height="827" alt="prj1_heatmap" src="https://github.com/user-attachments/assets/ff58c0ee-3e93-4b0d-a7c4-9275cfc5aefd" />
      <img width="624" height="672" alt="prj1_learningrate losses" src="https://github.com/user-attachments/assets/5c52c41b-43e4-49dc-a4ca-faf44c05ce92" />


    - 프로젝트 2 최종 RMSE는 약 `141.29`로, 프로젝트 기준인 `RMSE 150 이하`를 만족했습니다.
      <img width="567" height="210" alt="prj2_test metric" src="https://github.com/user-attachments/assets/5bacb1e0-c3f8-47b8-b24d-dc2dfdb89007" />

    - 시각화 요구사항도 충족했습니다. 프로젝트 1에서는 실제 target과 prediction을 scatter plot으로 비교했고, 프로젝트 2에서는 year/month/day/hour/minute/second별 데이터 개수 시각화와 temp/humidity 기준 실제값·예측값 비교 시각화를 수행했습니다.
      <img width="597" height="499" alt="prj1_show" src="https://github.com/user-attachments/assets/9b407eab-ac0f-4c38-84ec-b77d31d7ff02" />
      <img width="975" height="743" alt="prj2_show" src="https://github.com/user-attachments/assets/1bd5b02e-edcb-4cc3-9c28-7223ce494a4c" />


    
- [x]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - LMS 흐름에 따라 문제 해결을 해주셨기에 이해하는 데 어려움이 없었습니다.

- [x]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 명시적인 디버깅 기록은 없음
    - 프로젝트 1에서 기본 모델 구현 전 데이터 탐색 수행이 인상적임
    - Target 분포를 histogram으로 확인했고 feature별 Outlier 개수 확인 등을 수행함
    - feature 간 상관관계 heatmap을 작성함
        
- [ ]  **4. 회고를 잘 작성했나요?**
    - 아무래도 노드 과제 작성 시간이 부족해서 설명문 작성에 어려움이 있었을 듯 합니다. 
        
- [x]  **5. 코드가 간결하고 효율적인가요?**
    - 아직 리뷰어인 제가 간결하고 효율적인 코드의 형상을 잘 모르지만 읽기에 좋습니다!

# 회고(참고 링크 및 코드 개선)
```
EDA와 feature 분석 관점

현우님은 LMS에서 직접 요구하지 않았음에도 프로젝트 1에서 각 feature의 스케일링 전 raw data를 확인하고, 종속변수 target에 영향을 미칠 수 있는 feature를 탐색하기 위해 heatmap까지 시각화했습니다.

단순히 주어진 절차대로 모델을 학습시키고 MSE 기준을 맞추는 데서 끝나지 않고, 데이터의 원래 형태와 feature 간 관계를 먼저 이해하려는 접근이 좋았습니다. 특히 heatmap을 통해 어떤 변수가 target과 더 관련이 있는지 확인하려 한 점은 이후 feature 선택이나 모델 해석에도 도움이 되는 좋은 EDA 과정이라고 생각합니다.

```

