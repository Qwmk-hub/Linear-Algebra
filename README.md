# PCA를 활용한 얼굴 인식 기술 분석

## 05. PCA (Principal Component Analysis, 주성분 분석)

### 핵심 요약

- 고차원의 이미지 데이터를 PCA를 통해 **주성분 벡터들로 차원 축소**하고, 데이터를 효과적으로 표현할 수 있습니다.  
- 본 프로젝트에서는 약 276,033차원의 이미지 벡터를 분석하여, 그 중 **9개의 주요 주성분(basis)** 을 추출해 데이터의 본질적인 특성을 파악했습니다.  
- 이를 통해 입력 이미지와 가장 유사한 이미지를 **유클리디안 거리 기준으로 탐색**할 수 있습니다.

### 수학적 개념

- 각 이미지 벡터 **p**는 평균 벡터 **m**과 주성분 벡터들의 선형 조합으로 표현됩니다.  

  → `p = m + f₁·e₁ + f₂·e₂ + ... + fₖ·eₖ`  

  여기서  
  - **e₁, e₂, ..., eₖ**: 주성분 벡터 (PCA 고유벡터)  
  - **f₁, f₂, ..., fₖ**: 이미지의 주성분 계수들 (feature 벡터)

- 즉, `feature 벡터 f = [f₁, f₂, ..., fₖ]`는 각 이미지의 고유한 특성을 압축해 표현하는 방식입니다.

- 새로운 입력 이미지의 feature 벡터 `f_input`과 데이터셋의 feature 벡터 `f_dataset` 간의 거리 계산을 통해 가장 가까운 이미지를 찾습니다:

  → `|| f_dataset - f_input || < ε`  

  이때, `|| · ||`는 유클리디안 거리(norm), ε는 임계값입니다.

---

## 06. 기술의 응용 및 전망

### 보안 및 감시  
- 얼굴 인식 기술은 출입 통제 시스템에 활용되어 보안을 강화할 수 있습니다.  
- 공공 장소에서 실시간 신원 확인 및 감시 기능으로 활용 가능합니다.

### 금융  
- 얼굴 인증을 통한 본인 확인으로 절차가 간소화되며,  
- 사기나 부정 행위를 효과적으로 방지할 수 있습니다.

### 마케팅 및 소매업  
- 얼굴을 통해 고객의 성별, 연령대를 분석하고,  
- 맞춤형 광고 및 개인화된 서비스를 제공할 수 있습니다.

### 건강 관리  
- 얼굴 표정이나 근육의 변화로부터  
  정신 건강 상태(스트레스, 우울 등)를 분석하는 기술로 응용될 수 있습니다.

### 엔터테인먼트  
- VR/AR 환경에서 사용자 인식을 통해  
  몰입형, 맞춤형 인터랙션을 제공하는 데 활용됩니다.

### 교육  
- 온라인 수업에서 학생의 출석 여부를 확인하거나,  
- 시험 중 부정 행위를 방지하고 통제하는 데 응용할 수 있습니다.
