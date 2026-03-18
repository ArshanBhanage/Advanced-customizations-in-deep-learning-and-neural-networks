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

1. `Part1_TF_Generalization` — core regularization concepts ([Video Link](https://youtu.be/UkoM-GY0FjQ))
2. `Part1_PyTorch_Generalization` — same concepts in PyTorch ([Video Link](https://youtu.be/px_i6F_I6jQ))
3. `Part1_TF_KerasTuner_KerasCV` — automated tuning ([Video Link](https://youtu.be/sF3uN5NToYw))
4. `Part1_Multimodal_Augmentation` — all 6 modalities ([Video Link](https://youtu.be/bugKFWSlABQ))
5. `Part2_TF_Custom_Objects` — building custom Keras components ([Video Link](https://youtu.be/CTXNq-3MsTA))
6. `Part2_TF_Advanced_Training` — custom training loop ([Video Link](https://youtu.be/71tTzVD7wQg))
7. `Part2_PyTorch_Advanced` — custom PyTorch components ([Video Link](https://youtu.be/w7c5AI9rkbQ))
8. `Part2_WandB_Tracking` — experiment tracking ([Video Link](https://youtu.be/pACfOIPafKs))

---

# Requirement Coverage Matrix

## Part 1

| Assignment Requirement | Notebook(s) to Show | Evidence to Point Out in Video |
|---|---|---|
| L1/L2 regularization | `notebooks/part1_tensorflow/Part1_TF_Generalization.ipynb`, `notebooks/part1_pytorch/Part1_PyTorch_Generalization.ipynb` | regularizer/weight_decay config + A/B metric rows |
| Dropout | same as above | dropout layer definitions + comparative results |
| Early stopping | same as above | callback/logic + stopped epoch evidence |
| Monte Carlo dropout | TF + PyTorch generalization notebooks | stochastic inference section + uncertainty output |
| Initializer comparison | TF + PyTorch generalization notebooks | different init cells + performance contrast |
| Batch normalization | TF + PyTorch generalization notebooks | BN layers + training stability discussion |
| Custom dropout | PyTorch generalization and/or custom sections | custom module code + behavior check |
| Custom regularization | TF generalization/custom object sections | custom regularizer class/function |
| Callbacks + TensorBoard | TF notebooks | callback setup + TensorBoard log visualization |
| Keras Tuner | `notebooks/part1_tensorflow/Part1_TF_KerasTuner_KerasCV.ipynb` | tuner search space + best hparams output |
| KerasCV augmentation | same notebook | augmentation pipeline cells + sample visual output |
| Image augmentation/classification | `notebooks/extras/Part1_Multimodal_Augmentation.ipynb` | image pipeline + metric output |
| Video augmentation/classification | same notebook | frame/clip processing + baseline/treatment comparison |
| Text augmentation (nlpaug) | same notebook | nlpaug transform examples + classifier result |
| Timeseries augmentation/classification | same notebook | perturbation strategy + eval result |
| Tabular augmentation/classification | same notebook | synthetic/noise/imbalance handling + metrics |
| Speech augmentation/classification | same notebook | audio/spectrogram augmentation + model result |
| Document image augmentation/classification | same notebook | transform examples (rotation/blur/etc.) + classifier/OCR-oriented output |

## Part 2

| Assignment Requirement | Notebook(s) to Show | Evidence to Point Out in Video |
|---|---|---|
| Custom learning rate scheduler | `notebooks/part2_tensorflow/Part2_TF_Advanced_Training.ipynb`, `notebooks/part2_pytorch/Part2_PyTorch_Advanced.ipynb` | scheduler definition + LR progression |
| Custom dropout | `notebooks/part2_pytorch/Part2_PyTorch_Advanced.ipynb` and/or TF custom sections | custom dropout module/layer |
| Custom normalization | `notebooks/part2_pytorch/Part2_PyTorch_Advanced.ipynb` | custom norm layer/module |
| TensorBoard | `notebooks/part2_tensorflow/Part2_TF_Advanced_Training.ipynb` | logs + scalar curves |
| Custom loss function | `notebooks/part2_tensorflow/Part2_TF_Custom_Objects.ipynb`, `notebooks/part2_pytorch/Part2_PyTorch_Advanced.ipynb` | custom loss code + compile/train usage |
| Custom activation | `notebooks/part2_tensorflow/Part2_TF_Custom_Objects.ipynb` | activation function/class + model usage |
| Custom initializer | same notebook | initializer class/function + layer init output |
| Custom regularizer | same notebook | regularizer class/function + effect note |
| Kernel weight constraint | same notebook | constraint function/class in layer definition |
| Custom metric | TF custom objects + PyTorch advanced | metric implementation + logged values |
| Custom layers | TF custom objects + PyTorch advanced | custom layer forward/call implementation |
| Custom model | TF custom objects + PyTorch advanced | subclassed model/module |
| Custom optimizer | `notebooks/part2_tensorflow/Part2_TF_Advanced_Training.ipynb` (or notebook where implemented) | optimizer class + train step usage |
| Custom training loop | TF advanced training + PyTorch advanced | gradient step loop cells |
| Weights & Biases tracking | `notebooks/extras/Part2_WandB_Tracking.ipynb` | wandb init/log calls + run dashboard/output |


