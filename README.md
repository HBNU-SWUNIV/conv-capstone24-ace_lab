# 한밭대학교 인공지능소프트웨어학과 ACE_Lab팀

**팀 구성**
- 20221079 최범영
- 20221077 조성환
- 20231080 한예린

## <u>Teamate</u> Project Background
- ### 필요성
  본 과제는 관찰하는 주파수 대역 내에 신호가 존재하는지 판단하는 감청기를 위한 인공지능 기반 스펙트럼 센싱 기술을 개발하는 것을 목표로 한다. 감청기는 다양한 주파수 대역에서 실시간으로 신호를 감지하고 분석하는 시스템으로, 신호의 유무를 판단할 수 있어야 한다. 이를 위해 본 과제에서는 딥러닝 알고리즘을 활용하여 다양한 신호 패턴을 학습하고, 잡음이나 간섭이 많은 환경에서도 신호를 정확하게 탐지할 수 있는 기술을 구현할 예정이다.
 본 연구에서는 MATLAB을 활용하여 수신 신호를 스펙트로그램으로 변환하고, 이를 오토인코더의 입력 데이터로 사용하여 신호의 노이즈를 제거한다. 생성된 이미지는 신호를 강조한 형태로 표현되며, 이후 원본 이미지, 생성된 이미지, 그리고 모델 구조의 각 스테이지에서 생성된 이미지를 채널 축으로 결합하여 하나의 입력 데이터로 구성한다.
 그리고 이를 CNN(Convolutional Neural Networks)의 입력 데이터로 사용하여 학습을 진행한다. CNN은 이미지 분석에 최적화된 딥러닝 기술로, 복잡한 신호 환경에서도 높은 정확도로 신호의 유무를 판별할 수 있는 능력을 갖추고 있다. 특히 본 과제에서는 다양한 관찰 길이와 FFT 크기에 따른 모델의 성능을 비교·분석하여 최적의 네트워크 구조 및 하이퍼파라미터를 도출하고자 한다.
 본 연구의 정량적 목표는 SNR = 0dB와 같이 잡음과 신호의 세기가 유사한 환경에서도 신호 유무 판단의 정확도를 95% 이상으로 달성하는 것이다.
  

## System Design
  - ### System Requirements
    <a href="https://velog.io/@seondal"><img src="https://img.shields.io/badge/Velog-3DDC84?style=flat-square&logo=Blogger&logoColor=white"/></a>
    <a href="https://velog.io/@seondal"><img src="https://img.shields.io/badge/Velog-3DDC84?style=flat-square&logo=Blogger&logoColor=white"/></a>
    <a href="https://velog.io/@seondal"><img src="https://img.shields.io/badge/Velog-3DDC84?style=flat-square&logo=Blogger&logoColor=white"/></a>
    
    - 모델 전체 구조
    - OOO
    
## Case Study
  - ### Description
  
  
## Conclusion
  - ### OOO
  - ### OOO
  
## Project Outcome
- ### 2025 년 한국통신학술대회 

