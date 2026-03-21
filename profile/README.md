<div align="center">

![header](https://capsule-render.vercel.app/api?type=waving&color=0:0ea5e9,100:f97316&height=220&section=header&text=AI%20All%20In%20One%20Site&fontSize=42&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Create%20images%20and%20turn%20them%20into%20videos%20in%20one%20workflow&descAlignY=58)

# AI All In One Site

한글 프롬프트 기반 이미지 생성과 이미지-투-비디오 흐름을 한 서비스 안에서 연결하는 프로젝트입니다.  
Korean-first AI content workflow for image generation, upload, and image-to-video creation in one product.

<p>
  <img src="https://img.shields.io/badge/Frontend-React-61dafb?style=for-the-badge&logo=react&logoColor=061b2b" alt="React" />
  <img src="https://img.shields.io/badge/Language-TypeScript-3178c6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Build-Vite-646cff?style=for-the-badge&logo=vite&logoColor=white" alt="Vite" />
  <img src="https://img.shields.io/badge/UI-Korean%20First-0f172a?style=for-the-badge" alt="Korean First" />
</p>

</div>

---

## Preview

<div align="center">
  <img src="https://github.com/user-attachments/assets/73af567b-5790-4df7-aa4e-516e0ee32304" width="100%" alt="AI All In One Site main preview" />
</div>

<br />

<div align="center">
  <img src="https://github.com/user-attachments/assets/ce24f8e6-4a63-4c01-abff-2c23bbb44744" width="48.5%" alt="AI All In One Site preview image 1" />
  <img src="https://github.com/user-attachments/assets/75ce3d82-a8e1-4a05-a50a-33e06027e998" width="48.5%" alt="AI All In One Site preview image 2" />
</div>

---

## Korean

### 핵심 기능

- `guide_image.md` 기반 이미지 프롬프트 템플릿
- `guide_vedio.md` 기반 영상 프롬프트 템플릿
- `guide_plan.md` 기반 서비스 기획 포인트 반영
- 이미지 생성, 업로드, 영상 생성 흐름 연결
- 자동 확장 프롬프트 미리보기 제공

### 사용 흐름

1. 이미지 탭에서 한글 프롬프트 입력
2. 주체, 분위기, 배경, 조명, 디테일 템플릿 보완
3. 자동 확장 프롬프트 확인 후 이미지 생성
4. 생성 이미지 또는 업로드 이미지를 선택
5. 영상 탭에서 카메라 움직임, 객체 움직임, 환경 변화 입력
6. 자동 확장 영상 프롬프트 확인 후 영상 생성

### 실행 방법

```bash
cd C:\Users\ggg99\Desktop\ai\all-in-one-site
npm install
npm run dev
```

브라우저 접속:

```text
http://localhost:3000
```

---

## English

### Core Features

- Guided image prompting based on `guide_image.md`
- Guided video prompting based on `guide_vedio.md`
- Product framing based on `guide_plan.md`
- Unified image generation, upload, and video workflow
- Auto-expanded prompt previews before generation

### Workflow

1. Start with a Korean prompt in the image tab
2. Fill the structured template fields
3. Review the expanded prompt and generate images
4. Select a generated image or upload your own image
5. Move to the video tab and define motion details
6. Review the expanded video prompt and generate the result

### Run Locally

```bash
cd C:\Users\ggg99\Desktop\ai\all-in-one-site
npm install
npm run dev
```

Open:

```text
http://localhost:3000
```

---

## Repository Guides

- `guide_image.md`
- `guide_vedio.md`
- `guide_plan.md`

## Status

- UI and prompt flow are implemented
- Image and video generation are still mocked
- Real model APIs are the next integration step
