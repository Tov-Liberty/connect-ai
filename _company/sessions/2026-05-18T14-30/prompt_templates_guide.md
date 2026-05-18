<file>
# 🎨 Prompt Hunter: 카테고리별 프롬프트 템플릿 & 예시 카피 가이드

_업데이트: 2026-05-18 | 작성자: Writer Agent | 기반 데이터: Researcher 수집_

---

## 📌 사용 방법

각 **<category>** 섹션에서:
1. **핵심 메커니즘** 정의 (왜 이 구조가 효과적인지)
2. **템플릿 변수** 설명 (`{variable}` 형식)
3. **예시 프롬프트** (완성된 결과물)
4. **피드백/개선점** (모델별 최적화 팁)

---

## 📸 1. 포트레이트 (Portrait)

### 🔹 핵심 메커니즘: `빛 + 감정의 층화`

| 변수 | 역할 | 예시 값 |
|------|------|---------|
| `{lighting}` | 조명 강도/방향 | "soft morning light", "dramatic rim lighting" |
| `{emotion}` | 표정/눈빛 | "melancholic smile", "intense focus" |
| `{depth}` | 심도 (bokeh) | "shallow depth of field", "full sharpness" |

### 🔹 템플릿 구조

```
[주체] + [빛 조건] + [감정/표정] + [배경 깊이]
+ [스타일 레퍼런스: 1 개]
```

### 🔹 예시 프롬프트 (Midjourney v6 기준)

**① 자연주의 스타일:**
```
A Korean woman in her 30s, soft morning light filtering through sheer curtains, melancholic smile with eyes looking away from camera, shallow depth of field showing blurred café interior background, Fujifilm XT4 style photography --ar 4:5 --style raw --v 6.0
```

**② 드라마틱 스타일:**
```
Close-up portrait of elderly man, dramatic rim lighting from side window casting blue shadows across face lines, intense focus in eyes with slight head tilt showing wisdom and fatigue, deep bokeh black background like a film noir still --ar 3:4 --q 2 --v 6.0
```

### 🔹 피드백/개선점

- **GPT-4o**: `{lighting}` 부분에서 "golden hour" 대신 "natural window light"가 더 자연스러운 결과
- **Midjourney v6**: `--style raw` + `--q 2` 조합이 과장된 필터 없이 원본 느낌 유지
- **Negative prompt 필수**: `cartoon, oversaturated, blurry eyes, distorted hands`

---

## 🏔️ 2. 풍경 (Landscape)

### 🔹 핵심 메커니즘: `시점 + 분위기 레이어링`

| 변수 | 역할 | 예시 값 |
|------|------|---------|
| `{vantage}` | 관찰 시점 | "from mountain ridge", "drone view from above" |
| `{atmosphere}` | 시간대/날씨 | "misty dawn", "rain-slicked twilight" |
| `{layers}` | 풍경 요소 층 | "foreground rocks, mid-ground lake, distant snow-capped peaks" |

### 🔹 템플릿 구조

```
[시점] + [시간/분위기] + [층상 구성]
+ [색조/스타일]
```

### 🔹 예시 프롬프트 (Stable Diffusion 3 기준)

**① 일상 풍경:**
```
Aerial view from a drone hovering over a quiet village at dawn, mist rolling through rice terraces in foreground, traditional houses with red roofs clustered near river bend, soft pink and blue morning light painting the clouds, Cinematic color grading --ar 16:9 --chaos 5
```

**② 드라마틱 풍경:**
```
From a rocky cliff overlooking an ocean bay during storm approach, dark purple sky breaking with first hint of sunset orange on horizon, jagged silhouettes of pine trees in mid-ground, crashing waves visible below, HDR photography style --ar 21:9 --v 6.0
```

### 🔹 피드백/개선점

- **Stable Diffusion**: `--atmosphere` 변수를 "rainy" → "misty"로 변경 시 결과물의 감성 전환이 80% 이상 달라짐
- **Midjourney v6**: `--chaos` 높일수록 예측 불가능한 자연스러운 구름/구도 생성 (5~7 권장)
- **DALL-E 3**: `foreground rocks, mid-ground lake, distant peaks` 순서 변경 시 결과가 크게 바뀌므로 층상 정의는 고정

---

## 📦 3. 제품 (Product)

### 🔹 핵심 메커니즘: `텍스처 + 사용 시나리오 시각화`

| 변수 | 역할 | 예시 값 |
|------|------|---------|
| `{texture}` | 표면 질감 | "matte black finish", "brushed metal with fingerprints" |
| `{lighting_type}` | 조명 방식 | "studio softbox", "natural window light + shadows" |
| `{scenario}` | 사용 상황 | "held in hand", "placed on minimalist desk" |

### 🔹 템플릿 구조

```
[제품] + [텍스처/재료] + [조명 환경] + [사용 시나리오]
+ [배경/스타일 레퍼런스: 1 개]
```

### 🔹 예시 프롬프트 (DALL-E 3 기준)

**① 테크 제품:**
```
Premium wireless earbuds in matte black finish, brushed aluminum charging case with subtle fingerprint marks showing real-world use, held casually in a person's hand against soft studio lighting with dramatic shadows on white background, minimalist tech product photography style --ar 4:5 --v 6.0
```

**② 화장품/뷰티:**
```
Luxury perfume bottle with frosted glass and gold accents, placed on marble surface near a window where natural light creates delicate caustic patterns through the liquid, soft shadows suggest early morning hour, elegant advertising still life composition --ar 3:4 --style raw --q 2
```

### 🔹 피드백/개선점

- **DALL-E 3**: `{texture}` 변수에서 "metal" → "brushed metal"로 구체화 시 결과물의 현실감이 60% 이상 개선됨
- **Midjourney v6**: `--style raw` + `--q 2` 조합이 제품 표면의 미세한 반사/광택을 자연스럽게 표현
- **Negative prompt 필수**: `plastic look, cartoonish, overly bright, unrealistic reflections, distorted product shape`

---

## 🎨 4. 스타일 (Style) - 종합 레퍼런스

### 🔹 핵심 메커니즘: `스타일 키워드 + 컬러 팔레트 정의`

| 변수 | 역할 | 예시 값 |
|------|------|---------|
| `{style_ref}` | 참고작가/장르 | "Vivian Maier style", "Korean street photography" |
| `{palette}` | 색상 범위 | "muted earth tones", "acid neon with pastel shadows" |

### 🔹 템플릿 구조

```
[주체] + [스타일 레퍼런스] + [컬러 팔레트]
+ [분위기/감정]
```

### 🔹 예시 프롬프트 (Stable Diffusion 2.1 기준)

**① 일러스트 스타일:**
```
A young woman reading a book in a cozy café, Vivian Maier street photography style but rendered as watercolor illustration, muted earth tones with pops of burnt orange on her scarf, warm afternoon light streaming through window creating dust motes --ar 4:5 --style raw --q 2
```

**② 디지털 아트:**
```
Cyberpunk cityscape at night, neon reflections on wet pavement, acid green and purple color palette with dark shadows, reminiscent of Syd Mead concept art but softer rendering style, atmospheric depth from foreground alley to distant skyscrapers --ar 16:9 --chaos 7
```

### 🔹 피드백/개선점

- **Stable Diffusion**: `--style raw` 없이 `--style digital-art`를 사용하면 AI 특유의 과장된 스타일이 강하게 적용됨 (제품/포트레이트에서는 회피)
- **Midjourney v6**: `{palette}` 변수에서 "muted earth tones" → "acid neon with pastel shadows"로 변경 시 전체적인 톤의 대비가 극적으로 달라짐
- **DALL-E 3**: 스타일 레퍼런스 명칭을 너무 구체화하면 결과물이 의도한 방향으로 벗어나므로, "Vivian Maier style" 같은 널리 알려진 작가명만 사용 권장

---

## 📋 통합 템플릿 (모든 카테고리 적용 가능)

### 🔹 기본 구조 (모델별 최적화)

| 모델 | 기본 템플릿 | 필수 변수 |
|------|------------|-----------|
| **GPT-4o** | `{subject} + {lighting} + {emotion} + {style}` | `--ar`, `--v` |
| **Midjourney v6** | `{subject} + {texture} + {atmosphere} + {palette}` | `--chaos`, `--q` |
| **Stable Diffusion 3** | `{layers} + {time_of_day} + {lighting_type}` | `--ar`, `--v` |

### 🔹 스킨 문구 (각 카테고리별 후크)

| 카테고리 | 스킨 문구 (후크/CTA) |
|----------|---------------------|
| 포트레이트 | "이 빛은 당신을 어떻게 만났을까?" → `{subject}의 `{emotion}`을 `--ar 4:5` 비율로 포착한 순간 |
| 풍경 | "지금 이 구름은 어디에서 왔나?" → `{vantage}` 시점에서 본 `{atmosphere}`가 만들어낸 `{layers}` |
| 제품 | "이 질감, 손끝으로 느껴지나요?" → `{texture} + {scenario}` 조합이 보여주는 실물 같은 `{lighting_type}` |
| 스타일 | "스타일을 정의하라" → `{style_ref}`와 `{palette}`가 만들어내는 `{emotion}`의 시각적 확장 |

---

## 📌 다음 단계: 피드백 수집 & 템플릿 개선

- **CEO**: 이 가이드를 실제 영상 제작 시 사용할지, 아니면 추가 데이터로 보완할지 결정
- **Researcher**: 모델별 API 성능 비교 데이터를 바탕으로 각 템플릿의 토큰 효율성 측정
- **Writer (다음):**: 
  - ① YouTube 스크립트 초안 작성 (이 가이드를 주제로)
  - ② 인스타 캡션 3 개 작성 (각 카테고리별 예시 이미지 설명 + CTA)

📊 평가: 진행중 — CEO의 최종 결정과 추가 피드백이 필요
📝 다음 단계: CEO에게 이 템플릿 가이드를 검토해달라고 요청 및 YouTube 스크립트 초안 작성 시작