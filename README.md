# 한밭대학교 인공지능소프트웨어학과 ACE_Lab팀

**팀 구성**
- 20221079 최범영
- 20221077 조성환
- 20231080 한예린

## <u>Teamate</u> Project Background
- ### 필요성
  - 본 연구의 필요성은 스텔스 무인기 간의 저피탐 통신 시스템의 실효성을 평가하고 이를 탐지할 수 있는 시스템을 개발하는 데 있다. 군사 작전에서 스텔스 무인기의 안전한 통신은 중요한 요소지만, 저피탐 통신 시스템이 실제로 외부 감청으로부터 안전한지 검증되지 않는다면 신뢰할 수 없다. 따라서, 적의 입장에서 저피탐 통신을 감청할 수 있는 시스템을 구축하여, 해당 통신 시스템의 탐지 가능성을 평가하고 분석하는 것이 필수적이다.
    
- ### 목적 및 기대효과
  - 본 과제를 통해 저피탐 통신 시스템을 모니터링하고 탐지할 수 있는 감청 시스템을 개발함으로써, 스텔스 무인기 간 통신의 취약점을 식별하고 개선 방안을 제시할 수 있다. 이를 통해 기존 저피탐 통신 시스템의 한계를 극복하고, 군사 통신의 보안성과 안전성을 강화하는 데 기여할 수 있을 것이다.
  - 감청기 기술은 군사 통신 시스템의 보안을 효과적으로 강화할 수 있는 핵심 요소이다. 인공지능을 활용한 스펙트럼 센싱 기술은 적의 감청 시도를 정확하게 탐지할 뿐만 아니라, 신호가 약하거나 잡음이 많은 낮은 SNR 환경에서도 인공지능 기반 분석을 통해 신호를 효과적으로 탐지할 수 있다. 또한, 기존의 에너지 탐지 방식에 비해 더 높은 정확도를 제공하여, 보다 신뢰할 수 있고 안정적인 통신 체계를 구축하는 데 기여할 수 있다는 기대효과가 있다.
  

## System Design
  - ### System Requirements
    <img src="https://img.shields.io/badge/python-3776AB?style=flat-square&logo=python&logoColor=white"/></a>
    <img src="https://img.shields.io/badge/pytorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/></a>
    <img src="https://img.shields.io/badge/scikitlearn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white"/></a>
    
   - ### 시스템 구조
      본 연구에서는 MATLAB을 활용하여 수신 신호를 스펙트로그램으로 변환하고, 이를 오토인코더의 입력 데이터로 사용하여 신호의 노이즈를 제거한다. 생성된 이미지는 신호를 강조한 형태로 표현되며, 이후 원본 이미지, 생성된 이미지, 그리고 모델 구조의 각 스테이지에서 생성된 이미지를 채널 축으로 결합하여 하나의 입력 데이터로 구성한다. 그리고 이를 CNN(Convolutional Neural Networks)의 입력 데이터로 사용하여 학습을 진행한다.
      
      ![스펙트럼 센싱 최종 시스템 구조](https://github.com/user-attachments/assets/fac0fd8a-0497-46ed-aab8-6d7b48872224)
      
      모델의 안정성을 높이기 위해 CNN에 3개의 이미지를 채널로 합쳐 입력한다. 이때 3개의 이미지는 원본 이미지, 중간 출력 이미지, 그리고 최종 출력 이미지로 구성된다.


   - ### 모델 네트워크 구조
      
      ![스펙트럼 센싱 모델의 네트워크 구조](https://github.com/user-attachments/assets/5ddfc9c6-11c0-4c4e-acf3-9bdb2c68f74d)


  
## Conclusion
  - ### 모델 성능
    ![모델 성능](https://github.com/user-attachments/assets/878a7d39-dd20-45a9-987a-9c6609fa93b2)

   위 그래프에 따르면, SNR이 -3 이상인 경우에는 항상 99% 이상의 높은 Accuracy를 유지하며 안정적인 성능을 보인다. 한편, SNR이 -4에서 -10 사이로 낮아질수록 성능이 점진적으로 감소하는 경향을 보이며 SNR이 -10에 이르면 노이즈와 신호를 잘 구분하지 못한다.
    
  - ### 모델 예측
    - ### Auto Encoder의 출력 이미지에 대한 CNN의 예측값
      ##### Noisy image: 원본 이미지
      ##### Space image: 중간 출력 이미지
      ##### DeNoisy image: 최종 출력 이미지
    
       ![image 1 CNN accuracy](https://github.com/user-attachments/assets/63187b3f-7485-4973-8a0c-08698d2a4ca9)
       [image 1]: [0.9849, 0.0238]
    
    
       ![image 2 CNN accuracy](https://github.com/user-attachments/assets/71c94777-d025-4c29-ab0e-13b3b04ce31e)
       [image 2]: [4.4819e-06, 1.0000e+00]
    
    
       ![image 3 CNN predict](https://github.com/user-attachments/assets/842da05b-600c-45a1-acd4-b8dcb01bd9d9)
       [image 3]: [9.1813e-12, 1.0000e+00]

    
      ![image 4 CNN predict](https://github.com/user-attachments/assets/517adfa8-de96-437e-a16b-f3cf603d337f)
       [image 4]: [4.5982e-08, 1.0000e+00]


  
## Project Outcome
- ### 2025년 한국통신학술대회 

