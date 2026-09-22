# Module 07: Efficient ML Persistence & Parallel Computing with Joblib

Welcome to **Module 07: Efficient ML Persistence & Parallel Computing with Joblib**. This module covers optimized disk serialization for NumPy-heavy machine learning models, multi-algorithm compression, operating system memory mapping (`mmap_mode`), persistent function call caching (`joblib.Memory`), and multi-core parallel execution engines (`joblib.Parallel` with `loky`).

---

## Pedagogical Progression

The curriculum spans **4 progressively structured interactive notebooks**:

```text
07_joblib/
├── 01_model_persistence_and_compression.ipynb
├── 02_memory_mapping_for_large_numpy_arrays.ipynb
├── 03_function_caching_with_memory.ipynb
├── 04_parallel_processing_for_machine_learning.ipynb
└── README.md
```

---

## Notebook Syllabus & Key Concepts

| Notebook | Focus Area | Foundational Concepts | Advanced & ML Applications |
| :--- | :--- | :--- | :--- |
| [**01_model_persistence_and_compression.ipynb**](01_model_persistence_and_compression.ipynb) | Persistence & Compression | • `joblib.dump()` and `joblib.load()` API<br>• Joblib internal array splitting vs. standard pickle serialization<br>• Compression engines: `zlib`, `gzip`, `bz2`, `lzma`, `lz4` | • **Scikit-Learn Pipeline Serialization**: Persisting end-to-end transformers with metadata envelopes<br>• **Multi-Codec Benchmark Suite**: Evaluating compression ratio, serialization speed, and deserialization latency |
| [**02_memory_mapping_for_large_numpy_arrays.ipynb**](02_memory_mapping_for_large_numpy_arrays.ipynb) | Zero-Copy Memory Mapping | • OS virtual memory, paging, and kernel page cache architecture<br>• Memory mapping read modes: `mmap_mode='r'` (read-only) vs. `mmap_mode='c'` (copy-on-write)<br>• Why memory mapping strictly requires uncompressed files (`compress=0`) | • **Sub-Millisecond Zero-Copy Deserialization**: Loading multi-gigabyte feature arrays without heap allocation<br>• **Out-of-Core Batch Processing**: Streaming inference on datasets exceeding available physical RAM |
| [**03_function_caching_with_memory.ipynb**](03_function_caching_with_memory.ipynb) | Persistent Function Caching | • `joblib.Memory(location=...)` persistent disk memoization<br>• Deterministic argument hashing and cache validation<br>• Selective cache eviction, cache invalidation, and directory inspection | • **Accelerating Heavy Feature Engineering**: Transparently caching polynomial expansions and text tokenization<br>• **Cached Model Training Pipelines**: Preventing redundant hyperparameter grid re-computation across notebook runs |
| [**04_parallel_processing_for_machine_learning.ipynb**](04_parallel_processing_for_machine_learning.ipynb) | Parallel Computing & Loky | • `joblib.Parallel` and `delayed` syntax<br>• Execution backends: `loky` (robust process pool), `threading` (GIL-constrained), and `multiprocessing`<br>• Chunking and `batch_size` tuning for worker throughput | • **Zero-Copy Shared Memory in Loky**: Fast IPC with automatic `max_nbytes` shared memory mapping<br>• **Custom Parallel Cross-Validation & Grid Search**: Scaling custom ensemble algorithms across all CPU cores |
