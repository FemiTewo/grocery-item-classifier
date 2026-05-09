# Inference Report - Grocery Item Classifier

## Success Cases
The model performed well on clear, well-lit images with distinct features:
- Fresh Produce: correctly identified in 70% of test cases
- Packaged Goods: strong performance due to distinct shapes
- Farm Products: good accuracy on clear background images

## Failure Cases
The model struggled with:
- Poor lighting conditions
- Images where multiple categories overlap visually
- Small or partially visible objects

**Why it failed:** The model was trained on CIFAR-10 (32x32 upscaled to 64x64),
which lacks the fine detail of real grocery images.

## Comparison with Baseline

| Approach | Accuracy | Speed |
|---|---|---|
| Manual Entry (human) | ~95% | 5-10 seconds |
| Simple Threshold | ~20% | instant |
| Our CNN Model | 69.52% | <0.1s |

## Key Learnings

### What Worked Well
- CNN architecture with 3 conv blocks was effective
- BatchNorm and Dropout prevented overfitting
- Balanced dataset (5,000 per class) gave fair results
- GPU training completed in under 10 minutes

### Challenges Faced
- Colab session timeouts lost saved models
- Solution: Saved everything directly to Google Drive
- CIFAR-10 images are low resolution
- Solution: Resized to 64x64 with normalization

## What We Would Do Differently
1. Use a real grocery image dataset (higher resolution)
2. Apply transfer learning with MobileNetV2 or ResNet18
3. Train for 20+ epochs for better accuracy
4. Add data augmentation (brightness, contrast changes)
5. Deploy as a web app for real-time demo

## Acknowledgments
- Professor for guidance on project structure
- PyTorch and torchvision documentation
- CIFAR-10 dataset by University of Toronto
- Claude AI for code assistance and debugging
