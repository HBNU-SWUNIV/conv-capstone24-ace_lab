# 한밭대학교 인공지능소프트웨어학과 ACE_Lab팀

**팀 구성**
- 20221079 최범영
- 20221077 조성환
- 20231080 한예린

## <u>Teamate</u> Project Background
- ### 필요성
  - (수정필요)본 연구의 필요성은 스텔스 무인기 간의 통신이 외부에 노출되지 않도록 저피탐 통신 시스템을 개발하는 데 있다. 군사 작전에서 스텔스 무인기 간의 통신 중 적에게 감지될 경우 작전의 실패로 이어질 수 있다. 따라서, 저피탐 통신 시스템을 통해 무인기 간의 통신을 은밀하게 수행하는 기술이 필수적이다.
    
- ### 목적 및 기대효과
  - (수정필요)본 연구의 정량적 목표는 SNR = 0dB와 같이 잡음과 신호의 세기가 유사한 환경에서도 신호 유무 판단의 정확도를 95% 이상으로 달성하는 것이다.
  - (수정필요)기존 스펙트럼 센싱 기술은 주로 에너지 탐지(Energy Detection)방식이 있으나 정확도가 낮고 복잡한 환경에서 한계가 있다. 따라서 인공지능을 적용하면 더 높은 정확도와 빠른 응답 속도를 통해 기존 기술의 한계를 극복할 수 있는 효과를 기대할 수 있다.
  

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

    위 그래프에 따르면, SNR이 -3 이상인 경우에 항상 99% 이상의 안정적인 Accuracy를 보인다. 반면, SNR이 -4에서 -10 사이일 때는 성능이 지수적으로 감소하며, SNR이 -10에 이르면 노이즈와 신호를 잘 구분하지 못한다.
    
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

