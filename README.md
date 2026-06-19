# 라즈베리파이5 - 라즈베리파이OS - Qt6
라즈베리파이5에 라즈베리파이 OS 64bit 데스크톱을 설치해서 Qt 6 개발환경을 구축한다

## 개발환경 만들기
```bash
#!/bin/bash

# 에러 발생 시 스크립트 중단
set -e

echo "=========================================="
# 현재 시간 정보(2026년 환경)를 반영한 로깅 및 시스템 업데이트 시작
echo "1. 시스템 패키지 목록 업데이트 및 업그레이드 중..."
echo "=========================================="
sudo apt update && sudo apt upgrade -y

echo "=========================================="
echo "2. 필수 빌드 도구 설치 중 (C++, CMake, Git)..."
echo "=========================================="
sudo apt install build-essential cmake git -y

echo "=========================================="
echo "3. Qt 6 라이브러리 및 개발 도구 설치 중..."
echo "=========================================="
sudo apt install qt6-base-dev qt6-base-dev-tools qt6-declarative-dev qt6-tools-dev-tools -y

echo "=========================================="
echo "4. 추가 Qt 6 모듈 설치 중 (Multimedia, Charts)..."
echo "=========================================="
sudo apt install qt6-multimedia-dev qt6-charts-dev -y

echo "=========================================="
echo "5. Qt Creator IDE 설치 중..."
echo "=========================================="
sudo apt install qtcreator -y

echo "=========================================="
echo "🎉 모든 Qt 6 개발 환경 설치가 완료되었습니다!"
echo "메뉴 -> 개발(Programming)에서 Qt Creator를 실행하세요."
echo "=========================================="
```
