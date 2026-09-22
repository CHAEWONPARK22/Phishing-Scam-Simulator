# 🛡️ Phishing Scam Prevention Simulator

> AI-based Interactive Phishing Scam Prevention Service

생성형 AI를 활용하여 실제 피싱·스캠 상황을 모사하고,  
사용자의 대화 행동을 분석하여 피싱 예방 교육과 맞춤형 피드백을 제공하는  
대화형 피싱 예방 시뮬레이션 서비스입니다.

---

## 📌 Project Overview

### Background

기존의 피싱 예방 교육은 주로 사례 소개나 영상 시청 등 이론 중심으로 이루어지는 경우가 많아, 사용자가 실제 상황에서 어떻게 대응해야 하는지를 직접 경험하기 어렵다는 점에 주목했습니다.

이에 실제 피싱 상황을 대화 형태로 체험하고, 사용자의 대응 행동을 분석하여 취약한 행동과 예방 방법을 확인할 수 있는 **대화형 피싱 예방 시뮬레이션 서비스**를 개발했습니다.

### Objective

사용자가 실제 피싱·스캠과 유사한 상황을 대화로 경험하면서

- 피싱 상황을 직접 체험
- 자신의 대응 행동 확인
- 위험 행동 분석
- 취약한 부분에 대한 피드백 제공
- 피싱 예방 방법 학습

을 할 수 있도록 하는 것을 목표로 했습니다.

---

## 🤖 AI System

본 프로젝트에서는 **OpenAI API 기반 생성형 AI**를 활용하여 실제 피싱 상황을 모사하는 대화형 시뮬레이션을 구현했습니다.

### AI-based Conversation Simulation

생성형 AI가 각 시나리오에 맞는 피싱범 역할을 수행하도록 **시나리오별 프롬프트를 설계**했습니다.


User
  ↓
Conversation Input
  ↓
OpenAI API
  ↓
Scenario-based Prompt
  ↓
AI Phishing Conversation
  ↓
User Behavior Analysis
  ↓
Risk Score & Feedback


### Prompt Engineering

각 피싱 상황에 따라

* 피싱범의 역할
* 상황 설정
* 시나리오의 목적
* 대화 진행 방식
* 사용자의 행동에 대한 판단 기준

등을 프롬프트에 반영하여 시나리오에 맞는 대화가 생성되도록 설계했습니다.

> 별도의 AI 모델을 직접 학습시키는 방식이 아니라 OpenAI API와 프롬프트 엔지니어링을 활용하여 서비스를 구현했습니다.

---

## 🎭 Simulation Scenarios

사용자가 다양한 피싱 상황을 경험할 수 있도록 여러 유형의 시나리오를 구성했습니다.

| Scenario        | Example Situation | Main Goal    |
| --------------- | ----------------- | ------------ |
| 📦 Delivery     | 택배회사 사칭           | 개인정보 및 주소 요구 |
| 🏢 Institution  | 기관 사칭             | 앱 설치 및 금전 요구 |
| 🛡️ Insurance   | 보험 관련 사칭          | 계좌 및 개인정보 요구 |
| 👨‍👩‍👧 Family | 가족 사칭             | 금전 및 개인정보 요구 |
| ❤️ Lover        | 연인 사칭             | 금전 및 개인정보 요구 |

각 시나리오마다 서로 다른 상황과 목표를 설정하여 사용자가 다양한 유형의 피싱 상황을 경험할 수 있도록 했습니다.

---

## 💬 Key Features

### 1. Interactive Phishing Simulation

메신저 형태의 UI에서 AI와 직접 대화하면서 실제 피싱 상황과 유사한 상황을 체험할 수 있습니다.


Scenario Selection
       ↓
Phishing Conversation
       ↓
User Response
       ↓
AI Response
       ↓
Simulation Result


### 2. User Behavior Analysis

대화 과정에서 사용자의 행동을 분석하여 피싱 위험 행동이 발생했는지를 확인합니다.

예를 들어,

* 개인정보 제공
* 주소 제공
* 금전 관련 행동
* 앱 설치
* 계좌 관련 정보 제공

등의 행동을 규칙으로 정의하고 대화 내용과 비교하여 위험 행동을 분석합니다.

### 3. Rule-based Evaluation

사용자의 행동을 일관된 기준으로 평가하기 위해 시나리오별 행동 규칙과 가중치를 JSON 형태로 구성했습니다.


Conversation
     ↓
Behavior Detection
     ↓
Rule Matching
     ↓
Weighted Score
     ↓
Final Result


이를 통해 대화 결과를 바탕으로 사용자의 피싱 대응 수준을 분석하고 주요 위험 행동을 확인할 수 있도록 했습니다.

### 4. Personalized Feedback

시뮬레이션이 종료되면 사용자의 대화 행동을 기반으로

* 잘 대처한 부분
* 개선이 필요한 부분
* 주요 위험 행동
* 피싱 예방 방법

등의 피드백을 제공합니다.

---

## 🏗️ System Architecture


┌──────────────────────┐
│      Frontend        │
│  HTML / CSS / JS     │
└──────────┬───────────┘
           │ REST API
           ↓
┌──────────────────────┐
│       Backend        │
│   API / Server       │
└──────────┬───────────┘
           │
           ↓
┌──────────────────────┐
│     OpenAI API       │
│ Generative AI Model  │
└──────────┬───────────┘
           │
           ↓
┌──────────────────────┐
│ Behavior Evaluation  │
│   Rule-based JSON    │
└──────────┬───────────┘
           │
           ↓
┌──────────────────────┐
│   Result & Feedback  │
└──────────────────────┘


---

## 🛠️ Tech Stack

| Category      | Technology            |
| ------------- | --------------------- |
| Frontend      | HTML, CSS, JavaScript |
| Backend       | Node.js, Express      |
| AI            | OpenAI API            |
| AI Method     | Prompt Engineering    |
| Evaluation    | Rule-based Evaluation |
| Data Format   | JSON                  |
| Database      | SQLite                |
| Communication | REST API              |

---

## 👩‍💻 My Contribution

### 🎨 Frontend Development

**프론트엔드 개발을 주로 담당했습니다.**

* HTML / CSS / JavaScript 기반 웹 UI 구현
* 모바일 메신저 형태의 채팅 인터페이스 구현
* 시나리오 선택 → 대화 → 결과 확인 전체 사용자 흐름 구현
* 사용자 메시지 입력 및 전송 기능 구현
* Enter / Shift + Enter 입력 처리
* AI 응답 대기 상태 및 채팅 인터랙션 구현
* 시뮬레이션 종료 후 결과 및 피드백 화면 구현

### 🤖 AI / API Integration

* OpenAI API를 활용한 생성형 AI 기반 대화 시스템 구현
* 피싱 시나리오에 따른 AI 대화 기능 API 연동
* 사용자 대화와 AI 응답 간의 API 통신 구현
* 대화 결과를 분석 및 피드백 화면으로 전달

### 🔗 Backend / API

* 프론트엔드와 백엔드 간 REST API 연동
* 채팅방 생성 및 대화 요청 처리
* OpenAI API와의 통신 구현
* 시뮬레이션 결과를 프론트엔드에 전달하는 API 연동

---

## 📊 Evaluation Process

사용자의 대화 내용을 시나리오별 행동 규칙과 비교하여 피싱 위험 행동을 분석합니다.


User Conversation
       ↓
Behavior Detection
       ↓
Scenario Rule Matching
       ↓
Risk Event Detection
       ↓
Weighted Score Calculation
       ↓
Final Result
       ↓
Educational Feedback


각 시나리오의 규칙을 별도로 관리하여 새로운 피싱 유형이나 행동 규칙을 추가할 수 있도록 구성했습니다.

---

## 🎯 Expected Impact

이 서비스는 단순히 피싱 사례를 학습하는 것이 아니라 사용자가 직접 대화에 참여하는 방식으로 피싱 상황에 대한 대응 경험을 제공하는 것을 목표로 합니다.

특히

* 청소년
* 성인
* 고령층

등 다양한 사용자가 실제 상황을 가정하여 피싱 대응 방법을 연습할 수 있도록 설계했습니다.

---

## 🚀 Future Work

* 더 다양한 피싱·스캠 시나리오 추가
* 실제 피싱 대화 데이터 기반 행동 분석 고도화
* 사용자별 취약 행동 패턴 분석
* 시나리오 난이도 및 개인화 기능 추가
* 충분한 데이터 확보 시 자체 NLP 모델 개발 검토
* 교육기관 및 공공기관과의 연계 가능성 확대

---

## 🎥 Demo

[▶️ View Demo Video](https://youtu.be/iHnhqh_V7Bw)

---

## 📄 Project Presentation

[📎 View Project Presentation](./docs/Phishing-Scam-Prevention-Service.pdf)

---

## 🏆 Competition

**피싱·스캠 예방을 위한 서비스 개발 경진대회**

**Team:** 안인지

### Team Members

* 박채원
* 김찬유
* 강유나
* 이채현

---

## 📚 Project Information

본 프로젝트는 피싱·스캠 예방을 목적으로 생성형 AI 기반 대화 시뮬레이션과 규칙 기반 사용자 행동 분석을 결합하여 구현한 서비스입니다.
