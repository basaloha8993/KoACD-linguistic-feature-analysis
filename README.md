# KoACD 언어적 특성 분석

본 저장소는 KoACD 공개자료를 활용하여 생성 방식과 LLM 생성 모델별 인지왜곡 유형 분포 및 언어 특성 차이를 분석한 Python 코드와 결과 파일을 포함합니다.

## 연구 개요

본 연구는 LLM 기반 한국어 청소년 인지왜곡 데이터셋인 KoACD를 대상으로, 데이터 생성 방식과 LLM 생성 모델에 따라 인지왜곡 유형 분포와 문장 수준 언어 특성이 달라지는지를 탐색적으로 분석하였습니다.

## 사용 데이터

- 데이터셋: KoACD public dataset
- 분석 대상: 108,717 text instances
- 생성 방식: Balancing, Clarification
- 생성 모델: Claude, GPT, Gemini
- 분석 텍스트 변수: Generated Story
- 라벨 변수: Cognitive Distortion

## 분석 변수

본 연구에서는 다음 문장 수준 언어 특성을 산출하였습니다.

- char_len: 글자 수
- word_len: 공백 기준 단어 수
- negative_count: 부정어 수
- emotion_count: 감정어 수
- extreme_count: 극단 표현 수

## 단어 목록

부정어, 감정어, 극단 표현 목록은 본 연구의 탐색적 분석 목적에 맞게 연구자가 직접 구성하였습니다. 해당 목록은 분석 코드 내에 포함되어 있습니다.

## 분석 방법

- 생성 방식별 인지왜곡 유형 분포 비교
- 카이제곱 검정 및 Cramer’s V 산출
- LLM 생성 모델별 언어 특성 비교
- Kruskal-Wallis 검정 및 epsilon squared 산출
- Random Forest를 활용한 생성 모델 예측 분석

## 파일 설명

- `Colab_시작하기의_사본.ipynb`: 분석 코드가 포함된 Colab 노트북
- `KoACD_analysis_results (1).zip`: 분석 결과 파일

## 논문 관련

본 저장소는 「KoACD 공개자료의 생성 방식 및 LLM 모델별 언어 특성 차이 분석」 논문의 재현성을 높이기 위해 공개되었습니다.
