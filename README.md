
---

## 🎯 Demo Objectives

The goal of this demo is to demonstrate a **complete and practical computer vision pipeline**, including:

- Multi-object fashion detection
- Improved recall for small objects (rings, watches, accessories)
- Multi-label attribute prediction per detected object
- Clean, standardized output format for downstream usage

This demo is intended as a **proof-of-concept system**.

---

## 🚀 Features

### ✅ Object Detection
- YOLOv11-based detection
- Supports apparel and accessory categories
- GPU acceleration via CUDA when available

### ✅ SAHI Integration
- Optional SAHI inference for small objects
- Toggleable directly from the UI
- Helps recover tiny fashion items often missed by standard inference

### ✅ Attribute Recognition
- Each detected object is cropped and passed to an attribute head
- Multi-label prediction (one object → multiple attributes)
- Attribute IDs are mapped to human-readable names

### ✅ Output Formats
- Visual output with bounding boxes
- Tabular summary (class, confidence, attributes)
- JSON output matching submission format

<img width="711" height="888" alt="image" src="https://github.com/user-attachments/assets/6800722d-aa52-4d4f-980b-228365580773" />
<img width="692" height="859" alt="image" src="https://github.com/user-attachments/assets/9ef7a5e5-36db-4e48-9ebd-307863b2d4a8" />

Example JSON output:
```json
[
  {
    "label": "Cardigan",
    "confidence": 0.97,
    "box": [100, 175, 715, 971],
    "attributes": ["Plain pattern", "Short length", "Single breasted"]
  }
]


