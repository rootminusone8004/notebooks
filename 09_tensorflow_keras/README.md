# Module 09: TensorFlow & Keras for Deep Learning

Welcome to **Module 09: TensorFlow & Keras for Deep Learning**. This module covers deep learning foundations, computation graphs, automatic differentiation, neural network architectures, high-performance data engineering with `tf.data`, convolutional visual processing, and custom research training dynamics.

---

## Pedagogical Progression

The curriculum spans **6 progressively structured interactive notebooks** designed to take students from low-level tensor mathematics to production-grade deep learning systems:

```text
09_tensorflow_keras/
├── 01_tensors_operations_and_autodiff.ipynb
├── 02_keras_model_architectures.ipynb
├── 03_training_monitoring_and_callbacks.ipynb
├── 04_data_pipelines_with_tf_data.ipynb
├── 05_convolutional_neural_networks.ipynb
├── 06_advanced_keras_and_custom_training.ipynb
└── README.md
```

---

## Notebook Syllabus & Key Concepts

| Notebook | Focus Area | Foundational Concepts | Advanced & ML Applications |
| :--- | :--- | :--- | :--- |
| [**01_tensors_operations_and_autodiff.ipynb**](01_tensors_operations_and_autodiff.ipynb) | Tensors, Autodiff & Graphs | • Tensors vs. NumPy arrays: rank, shape, dtype, device placement (`CPU`/`GPU`)<br>• `tf.constant` vs. mutable `tf.Variable`<br>• Tensor algebra, matrix multiplication (`tf.matmul`, `@`), broadcasting<br>• Automatic Differentiation with `tf.GradientTape()` | • Multi-variable gradients & persistent tapes (`persistent=True`)<br>• Second-order derivatives (Hessian diagonal)<br>• **Custom Gradient Descent Optimization Loop from Scratch** without high-level Keras APIs<br>• High-performance graph compilation with **`@tf.function`** and AutoGraph |
| [**02_keras_model_architectures.ipynb**](02_keras_model_architectures.ipynb) | Keras Authoring Paradigms | • Sequential API (`keras.Sequential`) vs. Functional API vs. Model Subclassing<br>• Core layers: `Dense`, `Dropout`, `BatchNormalization`<br>• Activations: `relu`, `gelu`, `swish`, `sigmoid`, `softmax`<br>• Model compilation (`compile`), loss functions, optimizers (`AdamW`, `Adam`, `SGD`) | • **Multi-Branch Deep Residual Network (ResNet-style)** with skip connections and multi-task heads via Functional API<br>• **Custom Keras Layer Subclassing** with dynamic weight allocation (`build`) and tensor transformations (`call`) with learnable scale parameters |
| [**03_training_monitoring_and_callbacks.ipynb**](03_training_monitoring_and_callbacks.ipynb) | Training Dynamics & Callbacks | • Model training lifecycle: `model.fit()` and the `History` dictionary<br>• Diagnosing underfitting, healthy convergence, and overfitting via learning curves<br>• Essential callbacks: `EarlyStopping`, `ModelCheckpoint`, `ReduceLROnPlateau` | • **Cosine Decay Learning Rate Schedules with Warmup** (`optimizers.schedules.CosineDecay`)<br>• **Custom Keras Callback Engineering** (`callbacks.Callback`) for real-time validation telemetry and numerical explosion detection<br>• Modern model serialization in the unified `.keras` zipped format |
| [**04_data_pipelines_with_tf_data.ipynb**](04_data_pipelines_with_tf_data.ipynb) | High-Throughput Input Pipelines | • ETL paradigm: Extract, Transform, Load<br>• `tf.data.Dataset.from_tensor_slices()`<br>• Transformations: `.shuffle()`, `.batch()`, `.map()`, `.filter()`<br>• Preventing GPU starvation with `.prefetch(tf.data.AUTOTUNE)` | • Parallel mapping (`num_parallel_calls=tf.data.AUTOTUNE`)<br>• **End-to-End Tabular Feature Processing Pipeline**: loading `data_files/housing_market.csv` with Keras preprocessing layers (`Normalization`, `StringLookup`, `CategoryEncoding`) directly inside the model graph to prevent training/serving skew |
| [**05_convolutional_neural_networks.ipynb**](05_convolutional_neural_networks.ipynb) | CNNs & Transfer Learning | • Principles of 2D Convolution: receptive fields, filters, strides, and padding (`valid` vs `same`)<br>• Spatial pooling: `MaxPooling2D` and `GlobalAveragePooling2D`<br>• Modern modular CNN constructed from scratch with in-graph data augmentations | • **Two-Stage Transfer Learning & Fine-Tuning**: freezing deep pretrained backbones (MobileNetV2), training classification heads, and unfreezing top blocks with reduced learning rates ($\eta = 10^{-5}$)<br>• **Feature Activation Map Visualization**: inspecting learned low-level edge and corner filters |
| [**06_advanced_keras_and_custom_training.ipynb**](06_advanced_keras_and_custom_training.ipynb) | Custom Loops & Autoencoders | • Custom loss functions: subclassing `keras.losses.Loss` (Focal Loss for class imbalance)<br>• Custom streaming metrics with `keras.metrics.Metric`<br>• Overriding `train_step()` in `keras.Model` for custom gradient clipping | • **Pure Low-Level Training Loop** with `tf.GradientTape` and `tf.data.Dataset`<br>• **Convolutional Denoising Autoencoder**: encoder-decoder bottleneck architecture trained to reconstruct clean visual signals from corrupted sensory inputs |

---

## Shared Asset Integration

All notebooks dynamically locate shared tabular datasets from [`data_files/`](../data_files) and visual benchmarks from [`images/`](../images):

```python
import os
import tensorflow as tf

# Dynamic path resolution
data_dir = "data_files" if os.path.exists("data_files") else "../data_files"
img_dir = "images" if os.path.exists("images") else "../images"
```
