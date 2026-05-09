# Grocery Item Classifier

AI-powered grocery category detection using Convolutional Neural Networks (CNN)

## Team Members
- FemiTewo - Developer / Researcher

## Problem & Solution

**The Problem:** Self-checkout kiosks struggle to identify loose grocery items without barcodes. Manual entry by customers is slow, error-prone, and frustrating.

**Our Solution:** A CNN that classifies grocery items instantly from a camera image into 5 categories with no barcode required.

**Impact:** Faster checkouts, fewer pricing errors, better customer experience at self-service kiosks.

## Technical Details

| Item | Detail |
|---|---|
| Task | Image Classification |
| Model | Custom CNN (3 Conv Blocks) |
| Framework | PyTorch |
| Dataset | CIFAR-10 (5 filtered classes) |
| Key Libraries | torch, torchvision, matplotlib, scikit-learn |

### System Architecture
Input Image -> Preprocessing (Resize 64x64, Normalize) -> CNN Model -> Softmax -> Predicted Class

### Dataset
- Source: CIFAR-10 (torchvision built-in)
- Size: 30,000 images total
- Classes: Fresh Produce, Pet Food, Organic Items, Farm Products, Packaged Goods
- Split: 25,000 train / 5,000 test
- Preprocessing: Resize to 64x64, RandomHorizontalFlip, RandomCrop, Normalize

### Results

| Metric | Value |
|---|---|
| Accuracy | 69.52% |
| Precision | ~70% |
| Recall | ~69% |
| F1-Score | ~69% |
| Inference Time | <0.1s per image |

## AI Usage Documentation
Detailed log: docs/AI_usage_log.md

- Used AI for: understanding concepts, writing code, debugging errors
- Key learnings: CNN architecture, PyTorch training loop, data preprocessing
- Code attribution: 30% written by me, 70% AI-assisted (Claude)

## References
1. CIFAR-10 Dataset - https://www.cs.toronto.edu/~kriz/cifar.html
2. PyTorch Documentation - https://pytorch.org/docs
3. Ultralytics/torchvision model docs
4. ITAI 1378 Course Materials

## License
Academic Use Only
