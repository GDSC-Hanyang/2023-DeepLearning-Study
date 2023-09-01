![GDSC Hanyang](https://media.discordapp.net/attachments/802076592825827332/1146391171879420004/GDSC_Hanyang_University_Vertical_color_cropped.png)

<div align='center'>
    <h1>23-24 GDSC HYU 1차 스터디 : Deep Learning</h1>

```
  Deep Learning 스터디 레포지토리 🙌
  (2023.09.07 - 2023.12.31)
```

</div>

# 🚀 참여 인원

```bash
# Core
황동욱(장), 김남호, 조선빈, 조현진

# General
안태영, 이지환, 이재승, 서지현, 강용진, 송성근, 김예림, 한유진, 권도혁, 김찬원
```

<br>
<br>
<br>

# 🥛 목차

1. [🙋‍♂️ 스터디 소개](#%EF%B8%8F-스터디-소개)
2. [🎖️ 핵심 스케쥴](#%EF%B8%8F-핵심-스케쥴)
3. [📚 팀 구조 및 학습 주제](#-팀-구조-및-학습-주제)
4. [📖 디렉토리 구조](#-디렉토리-구조)
5. [🙏 Git Flow / Rules](#-git-flow--rules)

---


<br>
<br>
<br>

# 🙋‍♂️ 스터디 소개

### 1️⃣ Machine Learning (Regression 등)

Regression 과정을 이해하고, 코드로 작성해보기

### 2️⃣ DNN (Activation function & Dropout)

ReLU, Dropout 같은 기법에 대해 이해하기

### 3️⃣ CNN & RNN

CNN, RNN 등의 인공신경망에 대해 알아보기

### ⭐ Kaggle 공모전 코드 리뷰 ⭐

실제 데이터셋을 다뤄보고, 직접 코드 성능 개선해보기

<br>
<br>

# 🎖️ 핵심 스케쥴

```bash
# 추후 공개 예정입니다!
```

<br>
<br>
<br>

# 📚 팀 구조 및 학습 주제

## 🙌 팀 구조

> 팀은 어떻게 어떻게 나뉘어져서 스터디가 진행됩니다!

<br>

## 📃 Languages / Libraries

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pytorch](https://img.shields.io/badge/Pytorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)


<br>
<br>
<br>

# 📖 디렉토리 구조

```bash
# 이하 내용은 예시입니다. 실제로 정해지면 수정할 계획입니다.

|-- DeepLearning-Study
    |
    |-- Week 1
    |       |-- Presentation
    |       |-- WIL
    |
    |-- Week 2
    |       |-- Presentation
    |       |-- WIL
    |
        ...
    |
    |-- Week 9
    |       |-- Presentation
    |       |-- WIL
    |
    |-- ...
```

<br>
<br>
<br>

# 🙏 Git Flow / Rules

## 1️⃣ Commit Convention

-   Commit Type만 영어로 작성합니다.

```Markdown
[{commit_type}] {목적}
(여러줄로 다는 경우) dash로 각 줄별로 수정 내역을 넣기

# example) [add] 0주차 김득수 과제 제출
# example) [fix] 2주차 김득수 과제 일부 수정

# long example)
[add] 0주차 김득수 과제 제출
 - README 추가
 - 이후 가이드라인 추가 예정
```

<br>

## 2️⃣ Branch Convention

### (1) master

-   작업한 내용들이 최종적으로 합쳐지는 Branch
-   Branch 에 모든 과제/발표자료를 Commit 했을 시, `rebase` 및 `PR` 로 Merge

### (2) 개인 제출용 Branch

-   과제 제출/수정 시 브랜치를 생성하고 작업합니다.

```Markdown
{목적}/{주차}_{본인 github ID}

목적
- add : 과제를 제출하려고 파일을 등록하는 경우
- fix : 잘못 제출했거나, 내용을 보충하기 위해 이미 제출한 내역을 수정하는 경우.

# example : VYWL라는 이름의 유저가 0주차 과제를 제출하는 경우.
-> add/VYWL_0
```

<br>

## 3️⃣ Weekly 과제/발표자료 제출

### (1) Branch 생성

-   Branch Convention을 지켜서 생성해주세요! 🙏

### (2) 과제/발표자료 Commit 하기

-   위에 디렉토리 구조를 확인 후, 구조에 맞춰서 제출해주세요!
-   제출 직전에 `git pull`을 했었는지 확인해주세요!
-   Commit Convention을 지켜주세요!

### (3) PR 생성 및

-   아래 Convention을 지켜서 PR을 만들어 주세요.
-   담당자(파트장, Core)가 Review를 남기면, 이후에 `master`로 Merge 해주세요!

```Markdown
<!-- 제목 : [N주차] 과제 제출_이름 -->
<!-- ex) [1주차] 과제 제출_표지원 -->

## 제출 내용
<!-- 상세 설명 관련이미지 캡쳐 혹은 설명 관련 글 첨부 -->

## 느낀점
- (간단히 두줄 정도 작성)
- (간단히 두줄 정도 작성)
```

<br>
