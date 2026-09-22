# Module 06: Object Serialization with Pickle

Welcome to **Module 06: Object Serialization with Pickle**. This module covers the theoretical and practical foundations of Python object serialization, bytecode protocols, custom state hooks, security vulnerabilities, whitelisted safe unpickling, cryptographic HMAC authentication, and distributed closure serialization with `cloudpickle`.

---

## Pedagogical Progression

The curriculum spans **4 progressively structured interactive notebooks**:

```text
06_pickle/
├── 01_pickle_fundamentals_and_protocols.ipynb
├── 02_custom_class_serialization_and_hooks.ipynb
├── 03_pickle_security_and_safe_unpickling.ipynb
├── 04_advanced_serialization_and_cloudpickle.ipynb
└── README.md
```

---

## Notebook Syllabus & Key Concepts

| Notebook | Focus Area | Foundational Concepts | Advanced & ML Applications |
| :--- | :--- | :--- | :--- |
| [**01_pickle_fundamentals_and_protocols.ipynb**](01_pickle_fundamentals_and_protocols.ipynb) | Byte Streams & Protocols | • In-memory (`dumps`/`loads`) vs. disk stream (`dump`/`load`) API<br>• Picklable types vs. unpicklable limitations (lambdas, open handles)<br>• Protocol evolution from Protocol 0 (ASCII) to Protocol 4 (64-bit objects) | • **Protocol 5 Out-of-Band Buffers (`PickleBuffer`)**: Zero-copy memory transfers of massive contiguous NumPy arrays without duplicating heap memory<br>• Packaging Scikit-Learn pipelines with metadata envelopes |
| [**02_custom_class_serialization_and_hooks.ipynb**](02_custom_class_serialization_and_hooks.ipynb) | State Hooks & Evolution | • How `pickle.load()` bypasses `__init__()`<br>• Custom state interception with **`__getstate__()`** and **`__setstate__()`**<br>• Safely excluding transient resources (file handles, database connections, locks) | • **Class Schema Evolution & Version Migration**: Handling backwards compatibility when model attributes change across software versions<br>• The **`__reduce__()` protocol** for factory-controlled instantiation and bounds-checked reconstruction |
| [**03_pickle_security_and_safe_unpickling.ipynb**](03_pickle_security_and_safe_unpickling.ipynb) | Security & Cryptography | • Why pickle is an insecure stack machine<br>• Constructing arbitrary code execution payloads using `__reduce__` | • **Whitelisted `RestrictedUnpickler`**: Subclassing `pickle.Unpickler` and overriding `find_class` to allowlist safe modules and block dangerous builtins (`os`, `sys`, `eval`, `subprocess`)<br>• **Cryptographic HMAC-SHA256 Signing**: Ensuring model payload authenticity and tamper detection prior to deserialization |
| [**04_advanced_serialization_and_cloudpickle.ipynb**](04_advanced_serialization_and_cloudpickle.ipynb) | Cloudpickle & Format Matrix | • Why standard pickle fails on closures and lambdas (serialization by reference vs. bytecode)<br>• Distributed computing serialization with **`cloudpickle`**<br>• Serializing dynamic classes and closure environments | • Serializing custom loss functions and dynamic ML transformers<br>• **Comprehensive Serialization Comparison Matrix**: Pickle vs. JSON vs. Parquet vs. Safetensors across security, language interoperability, and throughput |
