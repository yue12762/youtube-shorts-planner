---
name: youtube-shorts-planner
description: Create short-form YouTube Shorts concepts, character-consistent storyboards, shot designs, and scene-by-scene AI image/video prompts from a simple idea.
metadata:
  version: "3.0.0"
---

# YouTube Shorts Planner V3

## Purpose

將使用者提供的簡單故事想法，發展成可以實際製作的 YouTube Shorts 短影音企劃。

預設影片長度約 20 秒，比例為 9:16。

目標是讓使用者快速得到一致的角色設定、短影音劇情、時間軸、逐鏡頭攝影設計，以及每個分鏡各自獨立的 AI 圖像與影片生成 Prompt。

## When to Use

當使用者希望：

- 製作 YouTube Shorts
- 設計 AI 短影音
- 發想短影音劇情
- 製作短影音分鏡或攝影設計
- 產生逐鏡頭 AI 圖像 Prompt
- 產生逐鏡頭 AI 影片 Prompt
- 將簡單故事轉換成短影音企劃

時使用此 Skill。

## Workflow

收到使用者的短影音想法後：

1. 找出故事的主要角色。
2. 建立 Character Reference，固定每個角色的外觀、顏色、體型、服裝或配件、個性與辨識特徵。
3. 將固定角色設定視為所有分鏡 Prompt 的一致性基準；後續不得省略或改變關鍵特徵。
4. 設計一個簡單、容易理解的核心劇情。
5. 將劇情控制在約 20 秒，並設計前 1–3 秒的 Hook。
6. 將影片拆成約 4–6 個時間段。
7. 為每個分鏡設計畫面、劇情、Shot Size、Camera Angle、Camera Movement、Character Action 與 Emotion。
8. 在影片後段安排笑點、反轉、可愛或有記憶點的收尾。
9. 為每個分鏡分別產生獨立的英文 AI Image Prompt。
10. 為每個分鏡分別產生獨立的英文 AI Video Prompt。
11. 產生整體 Storyboard Image Prompt。
12. 產生統一 Negative Prompt，供所有分鏡使用。
13. 產生適合 YouTube Shorts 的英文標題。
14. 產生簡短片尾字幕。

## Output Format

依照以下順序輸出：

### 影片設定

- 主題
- 風格
- 長度
- 比例

除非使用者另有指定，長度約 20 秒，比例為 9:16。

### Hook

提供前 1–3 秒的視覺或劇情 Hook，快速建立情境並吸引觀眾繼續觀看。

### Character Reference

為每個主要角色提供固定設定：

- 外觀
- 顏色
- 體型
- 服裝或配件
- 個性
- 辨識特徵

設定應簡潔、具體且可重複使用。若某項不適用，明確標示「無」，不要任意新增。後續所有分鏡、Image Prompt、Video Prompt 與 Storyboard Image Prompt 必須維持相同角色設定。

### 20 秒時間軸與 Shot Design

通常拆成 4–6 個分鏡。每個時間區間提供：

- 時間
- 畫面與劇情
- Shot Size
- Camera Angle
- Camera Movement
- Character Action
- Emotion

每個分鏡盡量只安排一個主要動作，讓畫面容易生成並保持清楚。

### Scene-by-Scene Image Prompts

為每個分鏡分別提供一個獨立的英文 AI Image Prompt，不得只提供整體或共用 Image Prompt。

每個 Prompt 必須描述：

- 完整且一致的 Character Reference 關鍵特徵
- Environment
- Character Action
- Emotion
- Shot Size
- Camera Angle
- Visual Style
- 9:16 composition

即使角色已在前文定義，也要在每個 Prompt 中重述會影響視覺一致性的外觀、顏色、體型、服裝或配件及辨識特徵。

### Scene-by-Scene Video Prompts

為每個分鏡分別提供一個獨立的英文 AI Video Prompt，不得只提供整體或共用 Video Prompt。

每個 Prompt 必須描述：

- 完整且一致的角色設定
- Character Action
- Environment dynamics
- Camera Movement
- Emotion
- Visual Style
- 動作節奏
- 9:16 composition

避免在單一 Prompt 中要求過多複雜動作。角色動作、環境動態和鏡頭運動應能在該分鏡時間內自然完成。

### Storyboard Image Prompt

提供一個英文 Prompt，用來產生完整故事的分鏡概念圖。分鏡圖應：

- 包含主要故事節點
- 清楚呈現角色互動
- 維持固定角色設定
- 依照故事時間順序排列
- 反映各鏡頭的 Shot Size 與 Camera Angle
- 適合作為後續 AI 圖像與影片製作參考

### Negative Prompt

最後提供一個可套用於所有圖像與影片分鏡的統一英文 Negative Prompt，至少包含：

```text
extra characters, duplicated characters, extra limbs, deformed anatomy, inconsistent character design, changing fur or hair color, changing clothes or accessories, inconsistent environment
```

可依故事內容補充必要限制，但不得移除上述項目。

### YouTube Shorts Title

提供一個簡短、有吸引力的英文標題。標題應容易理解、不過度冗長，並表達影片最有趣的核心情境。

### Ending Text

提供一句簡短片尾字幕。

## Rules

- 預設影片比例為 9:16。
- 預設長度約 20 秒。
- 保留使用者指定的角色、劇情、台詞、聲音、風格、長度與比例，不得擅自改變核心設定。
- 劇情不要過度複雜，也不要為了增加戲劇性而加入使用者沒有要求的重要角色或事件。
- 前 1–3 秒必須快速建立情境或吸引觀眾。
- 優先使用容易透過 AI 生成的場景與動作。
- Character Reference 是全片的一致性基準；所有分鏡 Prompt 必須維持相同的外觀、顏色、體型、服裝或配件與辨識特徵。
- 每個分鏡必須包含 Shot Size、Camera Angle、Camera Movement、Character Action 與 Emotion。
- 每個分鏡盡量只包含一個主要動作。
- 每個分鏡必須各自提供獨立的英文 Image Prompt 與 Video Prompt。
- Image Prompt 與 Video Prompt 必須描述角色、場景、動作、情緒、鏡頭設計與視覺風格。
- Video Prompt 還必須描述環境動態、Camera Movement 與動作節奏。
- 所有 Prompt 必須適用於 9:16 直式構圖，除非使用者另有指定。
- 輸出結尾必須包含統一 Negative Prompt。
