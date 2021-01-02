# AI Pill Discriminator for Blind people
It provides a solution for the blind people to recognize pills.

--------------------------------------------------------------------------------------------
## 팀 소개
**팀명:** 시선

**팀장:** 황선일 (기획 / 디자인) 각 H/W의 부분 설계 및 3D 프린터를 활용한 제작.

**팀원:**

- 김영재 (S/W) 딥러닝을 사용하여 약품 판별 모델을 학습, 모델의 정확성과 속도 개선.
- 배한울 (S/W) 모델 학습 및 훈련 데이터를 위한 조명부 조절 및 설계, 이미지 전처리 프로세스 처리.
- 임영선 (H/W) STM32와 라즈베리파이의 통신 및 각 센서 제어, 전체 프로세스 설계 및 하드웨어 구축.

--------------------------------------------------------------------------------------------
## 프로젝트 명
시각장애인을 위한 인공지능 알약 판별기

## 프로젝트 배경 및 목적
: 약의 색상, 모양 등의 시각적 정보를 통해 약을 구별하여 복용하는 일반인들과 달리,
앞을 보기에 어려움을 갖고있는 시각장애인들은 약을 구별하지 못해 오남용하는 사례가 빈번히 일어나고 있다.
그들을 이러한 불편함에서 보호하고자, 시각장애인들이 약을 쉽게 구별하여 복용할 수 있도록 알약 판별이 가능한 판별기 서비스를 제공하고자 한다.

## 프로젝트 체계도
![](https://github.com/sight-bit/Pill_classification/blob/master/%EC%B2%B4%EA%B3%84%EB%8F%84.jpg)

## 프로젝트 소개 비디오
[프로젝트 소개](https://drive.google.com/file/d/1l8FyFvYxKbq2BUrAnfZMIuWi2pCM3Hy6/view?usp=sharing)
--------------------------------------------------------------------------------------------

## 파일 리스트
**Pill_list.csv**
- 판별할 알약의 정보 리스트 (이름, 성분, 복약 가이드 등)

**_camera.py**
- 카메라 모듈

**_serial.py**
- stm 과의 통신을 위한 모듈

**_ttsService.py**
- 판별된 약의 이름과 복약가이드를 음성으로 서비스

**frozen_graph.pb**
- 추론을 위한 네트워크 및 가중치 파일

**img_aug.py**
- 훈련 데이터 증식

**img_coord.py**
- Rotation ROI(원형) 를 찾기 위해 사용

**inference.py**
- 촬영된 이미지를 통해 약을 추론

**main.c**
- stm32cubeIDE 에서 작성한 코드

**readcsv.py**
- csv를 읽어 알약의 정보를 가져옴

**main.py**
- 실제 실행되는 main 코드
--------------------------------------------------------------------------------------------
## 사용된 부품

**보드 :** B-L4S5I-IOT01A - 위 아래 서보모터 구동, 포토 인터럽트센서로 알약 투입 인식

**보조 보드 :** RaspberryPi 4 - 조명 조절 및 카메라 촬영, DL을 통한 알약 판별, 안내 음성 출력

--------------------------------------------------------------------------------------------


