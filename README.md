# gene-parfum

## 프로젝트 개요

본 프로젝트는 딥러닝 및 머신러닝 기술을 활용하여, 사용자 맞춤형 향수 처방전을 생성하는 프로그램을 개발하는 것을 목표로 합니다.

## 목표

-   800가지의 향료 데이터와 130가지의 향수 처방전 데이터를 기반으로, 새로운 향 조합을 생성하는 VAE 모델을 개발합니다.
-   GAN, 연관 규칙 학습, NLP 모델을 VAE와 결합하여, 생성된 향수 처방전의 품질을 향상시킵니다.
-   사용자 친화적인 인터페이스를 통해, 사용자가 선호하는 향, 특징, 상황 등을 입력하면, 그에 맞는 향수 처방전을 추천합니다.

## 사용 기술

-   Python
-   TensorFlow/PyTorch
-   scikit-learn
-   Pandas
-   NLTK/SpaCy/KoNLPy (자연어 처리)
-   mlxtend (연관 규칙 학습)
-   Jupyter Notebook

## 데이터

-   **원료 데이터 (`ingredients_data.csv`)**: 800가지 향료에 대한 정보 (이름, 코드, 계열, 7개의 묘사, 3개의 사용법, 볼륨감, 향세기, 잔향성)
-   **처방전 데이터 (`recipes_data.csv`)**: 130가지 향수 처방전 정보 (이름, 계열, 7개의 묘사, 출시년도, 조향사, 브랜드)

## TODO

-   [ ] 데이터 전처리 (결측치 처리, 이상치 탐지, 스케일링, 인코딩 등)
-   [ ] VAE 모델 구현
-   [ ] GAN 모델 구현
-   [ ] 연관 규칙 학습 모델 구현
-   [ ] NLP 모델 구현
-   [ ] 사용자 인터페이스 개발
-   [ ] 모델 평가 및 개선

## 협업 방식

-   본 저장소는 p-arfum님이 주도적으로 관리합니다.

-   ## recipes_data.json

This file contains the perfume recipes data in JSON format. Each object in the JSON array represents a single perfume recipe.

**Fields:**

*   `recipe_name` (string): The name of the perfume recipe.
*   `family` (string): The fragrance family of the perfume.
*   `desc1` - `desc7` (string): Descriptors of the perfume.
*   `year` (number): The year the perfume was launched.
*   `perfumer` (string): The perfumer who created the perfume.
*   `brand` (string): The brand of the perfume.
*   `ingredients` (array): An array of objects, each representing an ingredient used in the perfume.
    *   `code` (string): The unique code of the ingredient.
    *   `concentration` (number): The concentration of the ingredient in the perfume.

**Example:**

```json
{
  "recipe_name": "Eternity",
  "family": "Floral",
  "desc1": "fresh",
  "desc2": "clean",
  "desc3": "floral",
  "desc4": "elegant",
  "desc5": "timeless",
  "desc6": "classic",
  "desc7": "romantic",
  "year": 1988,
  "perfumer": "Sophia Grojsman",
  "brand": "Calvin Klein",
  "ingredients": [
    { "code": "B001", "concentration": 10 },
    { "code": "R001", "concentration": 5 },
    { "code": "S001", "concentration": 2 }
  ]
}
-   github-gk는 코드 리뷰, 개선 제안, 질문 답변, 자료 제공 등을 통해 p-arfum님을 지원합니다.
-   GitHub Issues, Pull Request 댓글, 이메일 등을 통해 적극적으로 소통합니다.

## 향후 계획
- VAE, GAN, 연관 규칙, NLP 모델을 활용한 향수 생성 프로그램 개발
