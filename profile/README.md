<div align="center">
<img alt="rock" title="rock" src="asset/logo.png" width="450">

# 🎸 희로애 rock (Huiroae-rock)
**음악에 맞는 앨범 커버 생성 서비스**

> "사람들은 음악을 들을 때, 소리만을 소비하지 않습니다. 노래는 개인의 기억, 감정, 상황과 결합되며 하나의 이미지로 각인됩니다."

<br/>

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/>
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=PyTorch&logoColor=white"/>
<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=React&logoColor=black"/>
<img src="https://img.shields.io/badge/Suno_AI-000000?style=flat-square&logo=audio&logoColor=white"/>

</div>

<br/>

## 📅 Project Duration
**2025.09 ~ 2026.02.07**

<br/>

## 📝 Introduction
**희로애 rock**은 AI가 생성한 음악을 해석하여, 그 곡의 분위기와 가사에 딱 맞는 앨범 커버를 사용자와 함께 만들어가는 서비스입니다.
청각적인 경험을 시각적으로 집약하여, 청자가 노래를 떠올릴 수 있도록 돕습니다.

<br/>

## 🚀 Key Features & Pipeline

전체 파이프라인은 **음악 생성 (Suno)** -> **음악/가사 분석** -> **이미지 생성 (SDXL)** 과정으로 이루어집니다.

### 1️⃣ Music Analysis: Music2emo
AI가 생성한 음악의 오디오 신호를 분석하여 곡의 감정(Mood), 긍정/부정(Valence), 흥분도(Arousal)를 추출합니다.
* **Multi-Task Learning**: MERT 임베딩을 활용하여 Categorical Label(Mood)과 Dimensional Label(VA)을 동시에 학습.

### 2️⃣ Lyrics Understanding: Customized SliSum
LLM을 활용하여 노래 가사의 핵심 주제를 요약하고, 프롬프트에 최적화된 형태로 변환합니다.
* **4가지 해석 모드**: 사실적 / 상징적 / 균형적 / 정서적 해석 모드를 제공하여 사용자가 원하는 느낌으로 가사를 재해석합니다.
* **Sliding Generation & Self-Consistency**: 긴 가사도 문맥을 잃지 않고 정확하게 요약하는 기법 적용.

### 3️⃣ Image Generation: SDXL (Fine-tuned)
분석된 음악의 감정 데이터와 요약된 가사 정보를 결합하여 고해상도 앨범 커버를 생성합니다.
* **Fine-tuning**: 앨범 커버 데이터셋을 구축하여 LoRA 기법으로 학습, 앨범 커버 특유의 스타일을 반영.

<br/>

## 🎨 Design System
창의적인 느낌의 **Vivid Color**와 유기적이고 볼드한 **Font**를 사용하여, 영감을 불러일으키는 서비스를 지향합니다.

<br/>

## 👥 Contributors

<table align="center">
  <tr>
    <td align="center" width="150px">
      <a href="https://github.com/hyun-jin891">
        <img src="https://github.com/user-attachments/assets/020634e2-dacc-42e1-9872-9abf83413c4d" width="100px" style="border-radius:50%"/>
      </a>
      <br />
      <b>조현진(팀장)</b>
    </td>
    <td align="center" width="150px">
      <a href="https://github.com/HYU-KDK">
        <img src="https://github.com/user-attachments/assets/adc42753-09de-4202-8cff-3fba401761be" width="100px" style="border-radius:50%"/>
      </a>
      <br />
      <b>김동기(개발)</b>
    </td>
    <td align="center" width="150px">
      <a href="https://github.com/lee-yeonseo">
        <img src="https://github.com/user-attachments/assets/985a02c7-760c-465a-b466-91defb02d5b4" width="100px" style="border-radius:50%"/>
      </a>
      <br />
      <b>이연서(개발)</b>
    </td>
    <td align="center" width="150px">
      <img src="https://github.com/user-attachments/assets/b07f5a8d-9982-4269-8a98-1911cf756c78" width="100px" style="border-radius:50%"/>
      <br />
      <b>정수현(디자이너)</b>
    </td>
</table>

<br/>
<div align="center">
  © 2026 Huiroae-rock. All Rights Reserved.
</div>
