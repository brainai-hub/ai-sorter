# BrainAI Sorter - Python 환경 설정 요구사항

## 🐍 Python 버전
- **Python 3.12.2**
- 가상환경: `python -m venv vbrainai`

---

## 📦 필수 라이브러리 설치 순서

### 1️⃣ pip 업그레이드
```명령 프롬프트
python.exe -m pip install --upgrade pip
```

### 2️⃣ 핵심 라이브러리 설치
```명령 프롬프트
pip install tensorflow==2.19.0
pip install keras==3.11.2
pip install openvino==2025.2.0
pip install ultralytics>=8.0.0
pip install pyserial>=3.5
```

### 3️⃣ 컴퓨터 비전
```명령 프롬프트
pip install opencv-python>=4.8.0
pip install opencv-contrib-python>=4.8.0
```

### 4️⃣ 이미지 처리 & 게임 컨트롤러
```명령 프롬프트
pip install pillow>=10.0.0
pip install pygame>=2.5.0
```

### 5️⃣ 데이터 처리 & 시각화
```명령 프롬프트
pip install numpy>=1.24.0
pip install pandas>=2.0.0
pip install matplotlib>=3.7.0
```

### 6️⃣ 유틸리티
```명령 프롬프트
pip install tqdm>=4.65.0
pip install python-dateutil>=2.8.2
```

---

## 📋 전체 requirements.txt

```txt
# Deep Learning Framework
tensorflow==2.19.0
keras==3.11.2

# OpenVINO for Inference
openvino==2025.2.0

# Object Detection
ultralytics>=8.0.0

# Computer Vision
opencv-python>=4.8.0
opencv-contrib-python>=4.8.0

# Image Processing
pillow>=10.0.0

# PS4 Controller Support
pygame>=2.5.0

# Serial Communication
pyserial>=3.5

# Data Processing
numpy>=1.24.0
pandas>=2.0.0

# Visualization
matplotlib>=3.7.0

# Utilities
tqdm>=4.65.0
python-dateutil>=2.8.2
```

---

## 🚀 한 번에 설치하기

```bash
# 가상환경 생성 및 활성화
python -m venv vbrainai
vbrainai\Scripts\activate  # Windows
# source vbrainai/bin/activate  # Linux/Mac

# pip 업그레이드
python -m pip install --upgrade pip

# requirements.txt로 일괄 설치
pip install -r requirements.txt
```

---

## ✅ 설치 확인

```bash
pip list
pip show pygame
pip show opencv-python
pip show ultralytics
pip show openvino
```

---

## 📊 주요 라이브러리 버전 정보

| 라이브러리 | 버전 | 용도 |
|-----------|------|------|
| Python | 3.12.2 | 기본 런타임 |
| TensorFlow | 2.19.0 | 딥러닝 프레임워크 |
| Keras | 3.11.2 | 고수준 신경망 API |
| OpenVINO | 2025.2.0 | 모델 최적화/추론 |
| Ultralytics | ≥8.0.0 | YOLO 객체 검출 |
| OpenCV | ≥4.8.0 | 컴퓨터 비전 |
| NumPy | 2.2.6 | 수치 연산 |
| PySerial | 3.5 | 시리얼 통신 |
| Pygame | ≥2.5.0 | PS4 컨트롤러 지원 |

이렇게 정리하면 설치와 관리가 훨씬 쉬워집니다! 🎯
