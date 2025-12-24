
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

<img width="711" height="888" alt="image" src="https://github.com/user-attachments/assets/9bfe9ee5-4770-49ce-a02d-8bbac20a92ec" />
<img width="692" height="859" alt="image" src="https://github.com/user-attachments/assets/4be54b91-89c1-43a5-8d8f-9480d8194b23" />

