# 🧠 Advanced Deep Learning Customizations
### Graduate-Level Assignment — TensorFlow & PyTorch

A comprehensive portfolio covering **regularization**, **data augmentation**, **custom training components**,
and **experiment tracking** across both major deep learning frameworks.

---

## 📚 Learning Objectives

- Apply L1/L2/Dropout/BatchNorm/EarlyStopping for generalization
- Build Monte Carlo Dropout for uncertainty estimation
- Implement custom activations, losses, layers, and optimizers from scratch
- Apply data augmentation across 6 modalities (image, text, timeseries, tabular, speech, documents)
- Use Keras Tuner for automated hyperparameter search
- Use KerasCV for modern image augmentation
- Write custom training loops with `GradientTape` (TF) and manual loops (PyTorch)
- Track experiments with TensorBoard and Weights & Biases

---

## 📁 Repository Structure

```
dl-assignment/
├── README.md
├── requirements/
├── notebooks/
│   ├── part1_tensorflow/
│   │   ├── Part1_TF_Generalization.ipynb      ← L1/L2, Dropout, BN, MC Dropout, TensorBoard
│   │   └── Part1_TF_KerasTuner_KerasCV.ipynb  ← Keras Tuner + KerasCV Augmentation
│   ├── part1_pytorch/
│   │   └── Part1_PyTorch_Generalization.ipynb ← Weight decay, Dropout, BN, Early Stopping
│   ├── part2_tensorflow/
│   │   ├── Part2_TF_Custom_Objects.ipynb      ← Custom Loss/Layer/Model/Metric etc.
│   │   └── Part2_TF_Advanced_Training.ipynb   ← Custom LR Scheduler + Training Loop
│   ├── part2_pytorch/
│   │   └── Part2_PyTorch_Advanced.ipynb       ← Custom Norm/Dropout/Loss/Scheduler
│   └── extras/
│       ├── Part1_Multimodal_Augmentation.ipynb
│       └── Part2_WandB_Tracking.ipynb         ← W&B for TF and PyTorch runs
├── assets/
│   ├── images/
│   ├── logs/
│   └── demo_scripts/
├── reports/
└── video_outline/
```

---

## 🗺️ Notebook Coverage Matrix

| Requirement | Notebook(s) |
|---|---|
| L1/L2 regularization | Part1_TF, Part1_PyTorch |
| Dropout | Part1_TF, Part1_PyTorch |
| Early stopping | Part1_TF, Part1_PyTorch |
| Monte Carlo dropout | Part1_TF, Part1_PyTorch |
| Weight initializers | Part1_TF, Part1_PyTorch |
| Batch normalization | Part1_TF, Part1_PyTorch |
| Custom dropout | Part1_TF, Part2_PyTorch |
| Custom regularizer | Part1_TF, Part2_TF_Objects |
| Callbacks + TensorBoard | Part1_TF, Part2_TF_Training |
| Keras Tuner | Part1_TF_KerasTuner_KerasCV |
| KerasCV augmentation | Part1_TF_KerasTuner_KerasCV |
| Image augmentation | Part1_Multimodal, Part1_KerasTuner |
| Text augmentation (nlpaug) | Part1_Multimodal |
| Timeseries augmentation | Part1_Multimodal |
| Tabular augmentation | Part1_Multimodal |
| Speech augmentation | Part1_Multimodal |
| Document image augmentation | Part1_Multimodal |
| Custom LR scheduler | Part2_TF_Training, Part2_PyTorch |
| Custom normalization | Part2_PyTorch |
| Custom loss | Part2_TF_Objects, Part2_PyTorch |
| Custom activation | Part2_TF_Objects |
| Custom initializer | Part2_TF_Objects |
| Custom constraint | Part2_TF_Objects |
| Custom metric | Part2_TF_Objects, Part2_PyTorch |
| Custom layer | Part2_TF_Objects, Part2_PyTorch |
| Custom model | Part2_TF_Objects, Part2_PyTorch |
| Custom optimizer | Part2_TF_Training |
| Custom training loop | Part2_TF_Training, Part2_PyTorch |
| Weights & Biases | Part2_WandB_Tracking |

---

## ⚙️ Setup

### Colab (Recommended)
Each notebook contains `!pip install` cells. Upload to Google Drive and open with Colab.
Set runtime to **GPU** for faster training.

### Local
```bash
pip install tensorflow keras-tuner keras-cv torch torchvision torchmetrics \
            wandb nlpaug albumentations audiomentations librosa \
            imbalanced-learn scikit-learn matplotlib pandas seaborn
```

---

## 📊 TensorBoard

After running `Part1_TF_Generalization` or `Part2_TF_Advanced_Training`:
```python
%load_ext tensorboard
%tensorboard --logdir /tmp/tb_logs
```

---

## 🪄 Weights & Biases

1. Create free account at https://wandb.ai
2. Get your API key from Settings
3. In `Part2_WandB_Tracking.ipynb`: `wandb.login(key="YOUR_KEY")`
4. View all runs at https://wandb.ai/YOUR_USERNAME/dl-assignment

---

## 🎬 Video Walkthrough Order

1. `Part1_TF_Generalization` — core regularization concepts
2. `Part1_PyTorch_Generalization` — same concepts in PyTorch
3. `Part1_TF_KerasTuner_KerasCV` — automated tuning
4. `Part1_Multimodal_Augmentation` — all 6 modalities
5. `Part2_TF_Custom_Objects` — building custom Keras components
6. `Part2_TF_Advanced_Training` — custom training loop
7. `Part2_PyTorch_Advanced` — custom PyTorch components
8. `Part2_WandB_Tracking` — experiment tracking

---

## 📝 Acknowledgements
Concepts drawn from: Keras documentation, PyTorch tutorials, Géron's *Hands-On ML*,
Goodfellow et al. *Deep Learning*, and original research papers referenced inline.
All code was written independently for educational purposes.
