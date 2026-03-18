# Assignment Video Proof Guide (Advanced DL Customizations)

Use this document while recording to **prove coverage** of every requirement with explicit evidence.

## 1) Video Structure (recommended)

- **Part A (2–3 min): Repository + authenticity proof**
- **Part B (35–55 min): Notebook-by-notebook walkthrough (execute key cells live)**
- **Part C (3–5 min): Coverage matrix recap (show every requirement mapped)**

---

## 2) Open with Hard Proof (must show first)

1. Open the GitHub repository root and show folder organization:
   - `notebooks/part1_tensorflow`
   - `notebooks/part1_pytorch`
   - `notebooks/part2_tensorflow`
   - `notebooks/part2_pytorch`
   - `notebooks/extras`
   - `README.md`
2. Open `README.md` and scroll to:
   - project objective
   - notebook list
   - coverage mapping/table
3. State explicitly on video:
   - “All notebooks were written in my own words and structure.”
   - “I will execute key cells in each notebook to verify results, not just show static screenshots.”

---

## 3) Notebook Order for Recording

1. `notebooks/part1_tensorflow/Part1_TF_Generalization.ipynb`
2. `notebooks/part1_pytorch/Part1_PyTorch_Generalization.ipynb`
3. `notebooks/part1_tensorflow/Part1_TF_KerasTuner_KerasCV.ipynb`
4. `notebooks/extras/Part1_Multimodal_Augmentation.ipynb`
5. `notebooks/part2_tensorflow/Part2_TF_Custom_Objects.ipynb`
6. `notebooks/part2_tensorflow/Part2_TF_Advanced_Training.ipynb`
7. `notebooks/part2_pytorch/Part2_PyTorch_Advanced.ipynb`
8. `notebooks/extras/Part2_WandB_Tracking.ipynb`

---

## 4) What to Prove in Every Notebook (same pattern)

For each notebook, show these 8 items on screen:

1. **Objective cell** (what is being tested)
2. **Dataset + preprocessing cell**
3. **Model definition cell(s)**
4. **Training config cell** (epochs, optimizer, callbacks/schedulers)
5. **Execution of at least 1 training/eval cell**
6. **Metrics output** (accuracy/loss/other required metric)
7. **A/B comparison table** (control vs treatment)
8. **Conclusion cell** (interpretation in your own words)

---

## 5) Requirement-to-Notebook Proof Map

### Part 1 — Generalization + Augmentation

- **L1/L2 regularization**
  - TF: `Part1_TF_Generalization.ipynb`
  - PyTorch: `Part1_PyTorch_Generalization.ipynb` (weight decay for L2)
- **Dropout**
  - TF + PyTorch generalization notebooks
- **Early stopping**
  - TF callbacks + custom/standard early stop logic in PyTorch notebook
- **Monte Carlo dropout**
  - both TF and PyTorch generalization notebooks
- **Initializations**
  - compare at least 2 initializers and show metric change
- **Batch normalization**
  - shown in both frameworks
- **Custom dropout + custom regularization**
  - custom implementations in TF/PyTorch notebooks where present
- **Callbacks + TensorBoard**
  - TF notebooks with callback definitions and TensorBoard logs
- **Keras Tuner**
  - `Part1_TF_KerasTuner_KerasCV.ipynb`
- **KerasCV augmentation**
  - same notebook, show augmentation pipeline cell
- **Multimodal augmentation/classification**
  - `Part1_Multimodal_Augmentation.ipynb` for image/video/text/timeseries/tabular/speech/document

### Part 2 — Advanced Custom Constructs

- **Custom LR scheduler**
  - `Part2_TF_Advanced_Training.ipynb` and/or PyTorch advanced notebook
- **Custom dropout**
  - Part 2 PyTorch and/or dedicated custom section
- **Custom normalization**
  - Part 2 PyTorch advanced notebook
- **TensorBoard**
  - TF advanced training notebook
- **Custom loss**
  - `Part2_TF_Custom_Objects.ipynb` and PyTorch advanced notebook
- **Custom activation / initializer / regularizer / constraint**
  - `Part2_TF_Custom_Objects.ipynb`
- **Custom metric**
  - TF custom objects + PyTorch advanced
- **Custom layers + custom model**
  - both TF and PyTorch advanced notebooks
- **Custom optimizer**
  - `Part2_TF_Advanced_Training.ipynb` (or notebook where implemented)
- **Custom training loop**
  - TF advanced training + PyTorch advanced
- **Weights & Biases**
  - `Part2_WandB_Tracking.ipynb`

---

## 6) Verbal Template to Use While Recording

Use this short script repeatedly:

1. “This experiment’s objective is __.”
2. “Control model is __; treatment model is __.”
3. “I’m running this cell now to show reproducible output.”
4. “Primary metric is __, and the overfitting gap is __.”
5. “From the A/B table, treatment improves/worsens by __, so conclusion is __.”

This structure makes grading easy because your logic is explicit.

---

## 7) Minimal Evidence Checklist (grading-safe)

Before ending the video, confirm each item verbally:

- [ ] Repository is cleanly organized and README is shown
- [ ] Both TensorFlow and PyTorch notebooks are demonstrated
- [ ] Required Part 1 topics are each shown at least once
- [ ] Required Part 2 topics are each shown at least once
- [ ] At least one live run shown in every notebook
- [ ] TensorBoard logs displayed where required
- [ ] W&B run dashboard or logging output displayed
- [ ] A/B tables shown and interpreted in your own words

---

## 8) Common Mistakes to Avoid

- Do **not** only scroll notebooks; execute key cells live.
- Do **not** skip failed cells silently; explain fix briefly.
- Do **not** state “better” without reading the metric table.
- Do **not** rely only on screenshots for TensorBoard/W&B proof.
- Do **not** skip the final coverage recap; that is what proves full requirement completion.

---

## 9) End with a Final Coverage Slide (on-screen)

At the end, show a simple statement:

> “Every assignment requirement from Part 1 and Part 2 has been mapped to at least one notebook and demonstrated through objective, code, execution, metrics, and A/B interpretation.”

Then briefly show the matrix file: `reports/requirement_coverage_matrix.md`.



Script 1 — Part1_TF_Generalization.ipynb (45–60 sec)
“In this notebook, I’ll walk through the **L1/L2 regularization**, **Dropout**, and **Batch Normalization** sections. I start by showing the **Dataset and preprocessing** cell, followed by the **Model definition** where these techniques are applied. During the **Training execution** cell, you can see **Early Stopping** triggered early around **Epoch 15**, stopping with a **validation accuracy of 0.8915**. Finally, I cover **Monte Carlo Dropout** for uncertainty estimation. By comparing the baseline to these techniques in the **A/B comparison table** at the end, I prove how each method actively reduces the overfitting gap.”

Script 2 — Part1_PyTorch_Generalization.ipynb (45–60 sec)
“Next is the PyTorch generalization notebook. I mirror the TensorFlow experiments by walking through the **Model definition cells** for **Weight Decay (L2)**, **Dropout**, and **Batch Normalization**. I also demonstrate a custom **Early Stopping logic** inside the manual training loop since PyTorch doesn't have it built-in. I will execute the **Training and Evaluation cells** live to show the metrics updating per epoch. We then look at the **Initializations** section to compare weight initializers, and finish with **Monte Carlo Dropout**. The **Conclusion cell** ties all these PyTorch validation metrics together to prove parity with the TensorFlow results.”

Script 3 — Part1_TF_KerasTuner_KerasCV.ipynb (45–60 sec)
“For automation, this notebook covers **Keras Tuner** and **KerasCV**. First, I show the **Objective cell** and the Tuner search space definition. I'll execute the search cell so you can see it actively finding the best hyperparameters. Then, in the **KerasCV augmentation** section, I show the augmented image pipeline cell. When running the final **Execution cell**, you'll see the model achieves a **Test accuracy of 0.4367** on the augmented data. The **Conclusion cell** explicitly explains how automated tuning and KerasCV layers make the pipeline more robust compared to our manual baselines.”

Script 4 — Part1_Multimodal_Augmentation.ipynb (45–60 sec)
“This is the **Multimodal Augmentation** notebook. I will go through the **Dataset cells** for each modality one by one. I'll show how we apply **Jitter and TimeWarp** for Timeseries, **SMOTE and FeatureNoise** for Tabular data, **Noise and Stretch** for Speech, and **Rotation and Blur** for Document images. For each section, I execute the **Augmentation cell** and the corresponding **Metrics output** to show the before-and-after effect on the classification baseline. The **Conclusion cell** proves that tailored augmentation strategies work across diverse data types without distorting the underlying labels.”

Script 5 — Part2_TF_Custom_Objects.ipynb (45–60 sec)
“Moving to Part 2, this notebook proves I can build custom TensorFlow internals. I will walk through the specific **Model definition cells** where I implement a **custom activation, initializer, regularizer, and constraint**. I also show a **custom loss function** and a **custom metric**. In the **Execution cell**, I run the training live. You can look at the **Metrics output** here at Epoch 12, where it hits a **val_accuracy of 0.8235** and our custom **top3_acc metric reaches 0.9929**. The **A/B comparison table** at the bottom clearly demonstrates that these custom abstractions compile and train successfully alongside standard Keras layers.”

Script 6 — Part2_TF_Advanced_Training.ipynb (45–60 sec)
“In this notebook, I demonstrate custom training control. I will show the **Training config cells** defining a **custom Learning Rate Scheduler** and a **custom Optimizer**. More importantly, I walk through the **Custom Training Loop** using `tf.GradientTape` instead of `model.fit`. I also show the **TensorBoard integration** tied to this loop. When I execute the training cell, you'll see the logs being written directly to the `/tmp/tb_custom_loop` directory. The **Conclusion cell** explains why we need this level of control for advanced research and how it successfully stabilizes the loss.”

Script 7 — Part2_PyTorch_Advanced.ipynb (45–60 sec)
“Here is the advanced PyTorch counterpart. I will highlight the **Model definition cells** where I've built **custom modules**, including **custom normalization and dropout layers**. I also walk through the **custom loss and metric** definitions. During the **Execution cell** for the full manual training loop, I will point out how the **custom LR scheduler** adjusts the learning rate dynamically. By comparing the **Metrics output** of the baseline with this custom architecture, the notebook proves I can engineer framework-independent deep learning constructs from scratch and validate them with real test metrics.”

Script 8 — Part2_WandB_Tracking.ipynb (45–60 sec)
“Finally, I use this notebook to demonstrate professional experiment tracking with **Weights & Biases**. I'll show the **Objective cell** and how the W&B runs are initialized and synced. Then, I will execute the cells that log our models and open the W&B dashboard. In the generated **Metrics output** table, you can explicitly see our cross-framework comparison: the **TensorFlow baseline achieved a Test Acc of 0.8446**, while the **PyTorch baseline achieved 0.8277**. The **Conclusion cell** wraps up the assignment by proving that we can track, compare, and reproduce metrics across entirely different frameworks in a centralized dashboard.”
