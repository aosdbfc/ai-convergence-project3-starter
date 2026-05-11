# AI Convergence Project 3 Starter

AI융합실전프로젝트3 과제

## 프로젝트 구조

```bash
project/
├── notebooks/
├── src/
├── data/
│   ├── raw/
│   └── processed/
├── reports/
├── README.md
└── .gitignore
```

실제 저장소에서는 아래와 같이 사용하는 것이 목적임

```bash
ai-convergence-project3-starter/
├── notebooks/          # EDA, 실험용 노트북
├── src/                # 재사용 가능한 Python 코드
├── data/
│   ├── raw/            # 원본 데이터
│   └── processed/      # 전처리 데이터
├── reports/            # 결과 보고서, 그림, 표
├── requirements.txt    # 패키지 목록
├── README.md
└── .gitignore
```

## 폴더 사용 원칙

- `notebooks/`: 실험, EDA, 아이디어 검증용 노트북 저장
- `src/`: 전처리, 학습, 평가 코드를 함수/모듈 형태로 정리
- `data/raw/`: 원본 데이터 저장
- `data/processed/`: 전처리 완료 데이터 저장
- `reports/`: 결과 이미지, 표, PDF 보고서 저장

## 시작 방법

```bash
git clone <your-repo-url>
cd ai-convergence-project3-starter
python -m venv .venv
```

### Windows

```bash
.venv\Scripts\activate
pip install -r requirements.txt
python src/main.py
```

### macOS / Linux

```bash
source .venv/bin/activate
pip install -r requirements.txt
python src/main.py
```

## README에 추가하면 좋은 항목

- 프로젝트 주제
- 문제 정의
- 사용 데이터셋
- 모델 구조
- 실험 방법
- 결과 요약
- 역할 분담

## 추천 브랜치 전략

- `main`: 제출용 안정 버전
- `dev`: 개발 통합 브랜치
- `feature/...`: 기능 단위 작업

예시:

```bash
feature/data-preprocessing
feature/model-training
feature/report-update
```

## 커밋 메시지 예시

```bash
feat: 데이터 전처리 코드 추가
fix: 학습 루프 오류 수정
docs: README 업데이트
refactor: 모델 학습 함수 정리
```

## 3~4주차 과제 

```
DVC는 코드가 아니라 데이터·모델·실험 결과의 버전 관리를 위해 쓰는 도구이고,
대용량 데이터나 재현성이 중요할 때 유용하지만, 작은 과제에서는 필수는 아니다.
```
## 5~6주차 과제 
Kaggle의 Titanic 및 Home Credit Default Risk 데이터를 활용하여 Random Forest, XGBoost, LightGBM의 성능을 비교하고, Bagging과 Boosting 계열의 차이 및 Early Stopping 효과를 검증한 Tabular 머신러닝 과제이다.
Validation 기반 실험 설계와 하이퍼파라미터 튜닝을 통해 단순 train 성능이 아닌 일반화 성능 중심으로 모델을 분석하였다.

## 7~8주차 과제 
중간고사 

## 9~10주차 과제 
이미지와 텍스트처럼 입력 데이터 구조가 다르면 적합한 딥러닝 모델 구조도 달라진다는 점을 실험으로 확인하는 것이다.
주요 쟁점은 이미지 Task에서 MLP가 이미지를 flatten하면서 공간 구조를 잃는 한계와, CNN이 지역 패턴과 위치 정보를 더 효과적으로 반영한다는 점이다.
텍스트 Task에서는 문장이 단순 단어 집합이 아니라 순서와 문맥을 가진 sequence 데이터이므로 RNN/LSTM 또는 Text CNN이 필요한 이유를 확인하는 것이 핵심이다.
결국 두 Task를 비교해 입력 구조의 차이가 모델 선택, 전처리 방식, 성능 해석에 어떤 영향을 주는지 설명하는 것이 과제의 중심이다.
