# License Plate Detection and Cleaning

This project processes a video to detect license plates using a YOLOv8 model and PaddleOCR, then post-processes the OCR results to reconstruct fragmented plates and output a cleaned, deduplicated list.

---

## 📹 What It Does

1. **Detect license plates** using a trained YOLOv8 model.
2. **Apply OCR** to read text from detected plates using PaddleOCR.
3. **Clean OCR results**:
   - Remove special characters.
   - Merge split license plate numbers (e.g., `43` and `ABCDE` → `43ABCDE`).
   - Deduplicate plates based on confidence score.
4. **Output** a text file with the cleaned results.

---

## 🛠 Requirements

Install the required Python libraries:

```bash
pip install opencv-python numpy ultralytics paddleocr
