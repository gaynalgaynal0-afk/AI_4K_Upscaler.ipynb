# 🎬 AI 4K Upscaler — Real-ESRGAN + RIFE

> **Model 1 Pipeline:** Fastest + Sharpest Quality  
> Real-ESRGAN x4+ · RIFE v4.6 · FP16 Half Precision · Google Colab Ready

---

## 🚀 One-Click Colab Launch

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/ai-4k-upscaler/blob/main/AI_4K_Upscaler.ipynb)

> Replace `YOUR_USERNAME` with your GitHub username after uploading.

---

## 📦 What It Does

| Feature | Detail |
|---------|--------|
| 🔍 AI Upscaling | Real-ESRGAN x4+ → up to 4K |
| 🎞️ Frame Interpolation | RIFE v4.6 → up to 240fps |
| ⚡ Speed | FP16 half precision on GPU |
| 🧩 Tile Processing | Handles large frames without VRAM crash |
| 📥 Input | MP4, MKV, AVI, MOV |
| 📤 Output | H.264 MP4, 4K resolution |

---

## ⚙️ Pipeline

```
Input Video (low res, low fps)
        ↓
   RIFE v4.6          ← Multiplies FPS  (e.g. 30 → 120fps)
        ↓
Real-ESRGAN x4+       ← AI upscale to 4K
        ↓
   FFmpeg             ← Reassembles final video
        ↓
Output 4K MP4
```

---

## 📋 How To Use

1. **Open the notebook in Google Colab** (button above)
2. **Set Runtime to GPU:** Runtime → Change runtime type → T4 GPU
3. **Run cells top to bottom**
4. **Upload your video** when Cell 6 prompts you
5. **Adjust settings** in Cell 7 (fps multiplier, scale, mode)
6. **Download** your 4K video from Cell 10

---

## ⚡ Speed Reference (T4 GPU)

| Mode | Speed |
|------|-------|
| ESRGAN only (4K) | ~8–15 fps |
| RIFE only (fps boost) | ~60–120 fps |
| Both (full pipeline) | ~5–10 fps |

> For faster results, set `UPSCALE_FACTOR = 2` or `FPS_MULTIPLIER = 2`

---

## 🛠️ Troubleshooting

| Problem | Fix |
|---------|-----|
| `CUDA out of memory` | Lower `TILE_SIZE` to 256 |
| Very slow | Use `MODE = 'esrgan'` only |
| No GPU | Runtime → Change runtime type → T4 GPU |
| RIFE crash | Re-run Cell 3 to redownload weights |

---

## 📁 Repo Structure

```
ai-4k-upscaler/
├── AI_4K_Upscaler.ipynb   ← Main Colab notebook
├── requirements.txt        ← Python dependencies
└── README.md
```

---

*Built with ❤️ using Real-ESRGAN + RIFE + FFmpeg*
