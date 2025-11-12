Phase 4 — Comparative Analysis & Insights
* Classical models (HOG + Color Hist) achieved ≈ 0.90 accuracy (SVM = 0.89 RF = 0.90).
* CNN underperformed (≈ 0.30 test accuracy) because of limited training data and class imbalance.
* Most confusions occurred between visually similar classes such as “other-sign” vs “pedestrians-crossing”.
* Precision > recall across most categories → indicates conservative detections.
* Future work: expand dataset, augment minor classes, and fine-tune a pretrained ResNet-18 backbone.
