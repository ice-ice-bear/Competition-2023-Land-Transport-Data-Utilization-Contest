# 🚗 장단 - 장기 주차 차량 단속 시스템

## 🖥️ 활용 언어 및 패키지
<p align="left">
  <a href="https://www.python.org/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="python"/> 
  </a>
  <a href="https://pytorch.org/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="pytorch"/> 
  </a>
  <a href="https://opencv.org/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="opencv"/> 
  </a>
  <a href="https://github.com/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="github"/> 
  </a>
  <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> 
    <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="pandas"/> 
  </a>
</p>

## 🧑 조 구성원
| 역할 | 이름 |
| ---- | ---- |
| 조장 | 홍길동 |
| 조원 | 김철수, 박영희, 이민호 |

## 📊 조 이름
- 장단

## 프로젝트 개요
### 프로젝트 명
장기 주차 차량 단속 시스템

### 프로젝트 주제
고속도로 및 시내 도로의 장기 주차 차량 단속 시스템 개발

### 주제 선정 배경
1. 고속도로 및 시내 도로에서 불법 주정차 및 장기 주차로 인한 교통사고 증가
2. 특수차량의 객체 검지 정확도 향상 필요성 대두
3. 기존 통행 차량 추적 시스템에 주차 차량 조회 기능 추가 필요

### 프로젝트 요약
- **객체 검출 및 추적:** YOLOv8과 DeepSORT를 활용하여 도로상의 차량과 보행자를 식별하고 실시간으로 교통 상황을 모니터링
- **주차 차량 분포 모니터링 및 알림:** 시내 도로 및 고속도로에서 주차 차량 분포를 모니터링하고, 혼잡 시간 알림 시스템 구축
- **합성이미지 생성:** 특수차량 검지율 향상을 위해 합성이미지 생성 기술을 사용하여 학습 데이터셋 증강

## 📈 활용 데이터 셋
| Dataset | 설명 | 출처 |
| ------- | ---- | ---- |
| Dataset1 | 판교제로시티 CCTV 데이터 (2D 바운딩박스) | [경기 마이데이터 드림](https://data.gg.go.kr) |
| Dataset2 | 판교제로시티 CCTV 데이터 제로셔틀 경로추적 | [경기 마이데이터 드림](https://data.gg.go.kr) |
| Dataset3 | 교통문제 해결을 위한 CCTV 교통 영상 (시내도로) | [AI 허브](https://www.aihub.or.kr) |

## 👨‍💻 데이터 전처리
1. **데이터셋 준비:**
   - CCTV 영상 데이터에서 객체 검출을 위한 바운딩 박스(annotation) 데이터 추출
   - 바운딩 박스 데이터를 YOLOv8 학습 형식에 맞게 변환
2. **데이터 증강:**
   - 특수차량 이미지 데이터를 합성이미지 생성 모델을 통해 증강

## 👩‍💻 기능 구현
### 객체 검출 및 추적
- YOLOv8을 이용한 차량 및 보행자 검출
- DeepSORT를 이용한 객체 추적
- 실시간 교통 상황 모니터링

### 장기 주차 차량 식별 및 알림 시스템
- 시내 도로 및 고속도로의 주차 차량 분포 모니터링
- 시간대별 혼잡도 측정 및 관련 당국에 알림 전송

### CCTV 지능형 교통관제 시스템 확장
- 기존 교통관제 시스템에 추가 기능 탑재

## 💪 모델 학습
### YOLOv8 모델 학습
- **데이터셋 준비:** CCTV 영상에서 추출한 이미지와 바운딩 박스 라벨 데이터
- **모델 학습:** YOLOv8 사전학습 모델을 기반으로 추가 학습 수행
- **성능 개선:** 특수차량 이미지 생성을 통해 검지율 향상

### 특수차량 이미지 생성
- **모델 활용:** Inpaint Anything 및 Stable Diffusion을 활용하여 특수차량 이미지 합성
- **학습 데이터 증강:** 특수차량 이미지 데이터를 생성하여 모델 성능 개선

## 🌟 기대효과 및 실효성
### 기대효과
- 도로 안전 및 교통 효율 개선
- 교통 통계 시계열 데이터 수집 및 분석
- 장기 주차 차량에 대한 실시간 모니터링 및 알림 시스템 구축

### 실효성
- 실시간 데이터 처리와 분석을 통해 교통 효율 증대
- 특수차량 검지율 향상을 통해 다양한 교통 문제 해결
- 지역사회 안전 및 편의성 증진

## 결론
본 프로젝트는 장기 주차 차량 문제를 해결하기 위해 첨단 객체 검출 및 이미지 합성 기술을 활용한 혁신적인 솔루션을 제공합니다. 교통 안전성과 효율성을 동시에 개선할 수 있는 장기 주차 차량 단속 시스템을 통해 실질적인 교통 문제 해결을 기대합니다.
