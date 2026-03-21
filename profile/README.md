# All In One Site
<img width="1102" height="1470" alt="image" src="https://github.com/user-attachments/assets/73af567b-5790-4df7-aa4e-516e0ee32304" />
<img width="627" height="685" alt="image" src="https://github.com/user-attachments/assets/ce24f8e6-4a63-4c01-abff-2c23bbb44744" />
<img width="609" height="1387" alt="image" src="https://github.com/user-attachments/assets/75ce3d82-a8e1-4a05-a50a-33e06027e998" />

## 한국어 안내

### 개요

이 프로젝트는 `AI 이미지 생성 -> 이미지 선택 또는 업로드 -> AI 영상 생성` 흐름을 한 서비스 안에서 연결하는 데모입니다.

현재 버전은 다음 가이드 파일을 반영합니다.

- `guide_image.md`
  한글 이미지 프롬프트 작성 가이드
- `guide_vedio.md`
  영상 프롬프트 작성 가이드
- `guide_plan.md`
  서비스 기획 기준 가이드

사이트 안에서는 이 가이드 내용을 다음처럼 사용합니다.

- 이미지 탭에서 한글 프롬프트를 템플릿 구조로 보완
- 이미지 탭에서 자동 확장 이미지 프롬프트 생성
- 영상 탭에서 카메라 움직임/객체 움직임/환경 변화 기반 템플릿 제공
- 영상 탭에서 자동 확장 영상 프롬프트 생성
- 우측 패널에서 기획 기준 요약 표시

### 기술 스택

- React
- TypeScript
- Vite
- lucide-react

### 실행 방법

1. 프로젝트 폴더로 이동합니다.

```bash
cd C:\Users\ggg99\Desktop\ai\all-in-one-site
```

2. 패키지를 설치합니다.

```bash
npm install
```

3. 개발 서버를 실행합니다.

```bash
npm run dev
```

4. 브라우저에서 아래 주소로 접속합니다.

```text
http://localhost:3000
```

5. 배포용 빌드를 확인하려면 아래 명령을 실행합니다.

```bash
npm run build
```

### 사용 방법

#### 1. AI 이미지 생성 탭

이 탭은 `guide_image.md` 기반입니다.

사용 순서:

1. `한글 프롬프트`에 기본 설명을 입력합니다.
2. `스타일 프리셋`을 선택합니다.
3. 아래 템플릿 항목을 필요에 따라 채웁니다.

- 주체
- 분위기/감정
- 배경/장소
- 조명/색감
- 기술 디테일

4. 자동으로 생성되는 `자동 확장 프롬프트`를 확인합니다.
5. 필요하면 예시 칩을 눌러 가이드 예제를 바로 불러옵니다.
6. `가이드 기반 이미지 생성` 버튼을 눌러 목업 이미지를 생성합니다.
7. 생성된 이미지 중 하나를 골라 `영상에 사용` 버튼을 누르면 영상 탭으로 연결됩니다.

이미지 탭의 핵심 목적:

- 짧은 한국어 입력을 더 구체적인 생성 프롬프트로 확장
- 가이드의 5가지 핵심 요소를 빠뜨리지 않게 보조

#### 2. 이미지 업로드 탭

사용 순서:

1. 이미지를 드래그하거나 클릭해 업로드합니다.
2. 미리보기를 확인합니다.
3. `업로드 이미지를 영상에 사용` 버튼을 눌러 영상 탭으로 보냅니다.

#### 3. AI 영상 생성 탭

이 탭은 `guide_vedio.md` 기반입니다.

사용 순서:

1. 이미지 생성 탭 또는 업로드 탭에서 이미지를 먼저 선택합니다.
2. `영상 프롬프트`에 기본 설명을 입력합니다.
3. 아래 템플릿 항목을 채웁니다.

- 카메라 움직임
- 객체 움직임
- 환경 변화
- 조명/색상
- 분위기/톤

4. 영상 길이와 움직임 강도를 선택합니다.
5. 자동으로 생성되는 `자동 확장 영상 프롬프트`를 확인합니다.
6. 필요하면 예시 칩을 눌러 자연 풍경, 사이버 도시, 커피 오브젝트 예제를 불러옵니다.
7. `영상 생성` 버튼을 누르면 목업 영상 결과 상태가 생성됩니다.

영상 탭의 핵심 목적:

- 영상 생성에서 중요한 카메라 움직임과 객체 움직임을 분리해 입력
- 이미지보다 더 구체적인 모션 설명을 하도록 유도

#### 4. 우측 패널

이 영역은 `guide_plan.md` 기준을 반영합니다.

표시 내용:

- 현재 선택된 이미지
- 영상 길이
- 움직임 강도
- 생성 결과 상태
- 서비스 목표 / 대상 사용자 / 차별성 요약

### 현재 포함된 예시

이미지 예시:

- 판타지 성
- 사이버펑크 도시
- 한복 포트레이트
- 음식 사진
- 추상 미술

영상 예시:

- 자연 풍경
- 사이버 도시
- 커피 오브젝트

### 파일 구조

- `Ai_content_studio.tsx`
  메인 상태와 탭 흐름 관리
- `components/ImageGenerationTab.tsx`
  이미지 가이드 기반 입력 UI
- `components/ImageUploadTab.tsx`
  업로드 UI
- `components/VideoGenerationTab.tsx`
  영상 가이드 기반 입력 UI
- `components/StudioSidebar.tsx`
  상태 및 기획 요약 패널
- `components/studioStyles.ts`
  전체 스타일 정의
- `types.ts`
  공통 타입
- `guide_image.md`
  이미지 프롬프트 가이드
- `guide_vedio.md`
  영상 프롬프트 가이드
- `guide_plan.md`
  서비스 기획 가이드

### 현재 구현 범위

- 한글 중심 UI
- 이미지 프롬프트 템플릿
- 영상 프롬프트 템플릿
- 자동 확장 프롬프트 미리보기
- 목업 이미지 생성
- 이미지 업로드
- 영상 생성 결과 목업 상태
- 선택 이미지 다운로드

### 아직 목업인 부분

- 실제 이미지 생성 모델 API 미연결
- 실제 영상 생성 모델 API 미연결
- 실제 영상 파일 출력 없음
- DB 저장 없음
- 사용자 인증 없음
- 결제/크레딧 시스템 없음

### 다음 단계 추천

1. 이미지 생성 API 연결
2. 영상 생성 API 연결
3. 확장 프롬프트를 서버에서 저장
4. 작업 히스토리 저장
5. 실제 영상 재생 컴포넌트 추가
6. 프롬프트 복사 기능 추가

---

## English Guide

### Overview

This project is a demo for a unified workflow:

`AI image generation -> image selection or upload -> AI video generation`

The current version reflects these local guide files:

- `guide_image.md`
  Korean image prompt writing guide
- `guide_vedio.md`
  Video prompt writing guide
- `guide_plan.md`
  Product planning guide

These guides are applied in the app as follows:

- The image tab expands short Korean prompts into a more structured image prompt
- The video tab provides a guided motion template for video prompts
- The sidebar shows product-planning highlights derived from the planning guide

### Tech Stack

- React
- TypeScript
- Vite
- lucide-react

### How To Run

1. Move into the project folder.

```bash
cd C:\Users\ggg99\Desktop\ai\all-in-one-site
```

2. Install dependencies.

```bash
npm install
```

3. Start the development server.

```bash
npm run dev
```

4. Open the app in your browser.

```text
http://localhost:3000
```

5. Run a production build check if needed.

```bash
npm run build
```

### How To Use

#### 1. AI Image Tab

This tab is based on `guide_image.md`.

Flow:

1. Write a short Korean prompt in the main text area.
2. Choose an image style preset.
3. Fill the guided template fields:

- Subject
- Mood / Emotion
- Background / Place
- Lighting / Color
- Technical Details

4. Review the automatically expanded image prompt.
5. Use one of the example chips if you want a prefilled guide example.
6. Click the generate button.
7. Pick one generated image and send it to the video tab.

#### 2. Upload Tab

Flow:

1. Upload an image file.
2. Review the preview.
3. Send the uploaded image to the video tab.

#### 3. AI Video Tab

This tab is based on `guide_vedio.md`.

Flow:

1. Select an image first.
2. Write a base Korean video prompt.
3. Fill the guided motion template fields:

- Camera Movement
- Subject Movement
- Environment Change
- Lighting / Color
- Atmosphere / Tone

4. Select duration and motion intensity.
5. Review the automatically expanded video prompt.
6. Use example chips if needed.
7. Generate the mock video result.

#### 4. Right Sidebar

This section reflects `guide_plan.md`.

It shows:

- The currently selected image
- Current video settings
- Result status
- Product goal, audience, and differentiation summary

### Included Examples

Image examples:

- Fantasy castle
- Cyberpunk city
- Hanbok portrait
- Food photography
- Abstract art

Video examples:

- Nature landscape
- Cyber city
- Coffee object scene

### File Structure

- `Ai_content_studio.tsx`
  Main state and flow controller
- `components/ImageGenerationTab.tsx`
  Guide-driven image prompt UI
- `components/ImageUploadTab.tsx`
  Upload UI
- `components/VideoGenerationTab.tsx`
  Guide-driven video prompt UI
- `components/StudioSidebar.tsx`
  Status and planning summary panel
- `components/studioStyles.ts`
  Shared styling
- `types.ts`
  Shared types
- `guide_image.md`
  Image prompt guide
- `guide_vedio.md`
  Video prompt guide
- `guide_plan.md`
  Product planning guide

### Current Scope

- Korean-first UI
- Guided image prompt template
- Guided video prompt template
- Auto-expanded prompt previews
- Mock image generation
- Image upload
- Mock video generation result
- Selected image download

### Still Mocked

- No real image model API yet
- No real video model API yet
- No real video output file yet
- No database storage yet
- No authentication yet
- No billing or credit logic yet

### Recommended Next Steps

1. Connect a real image generation API
2. Connect a real video generation API
3. Save expanded prompts on the backend
4. Add generation history
5. Add a real video playback component
6. Add prompt copy/export actions
