# Neuroverkkoprojekti

A collection of Jupyter notebooks used for teaching neural networks and machine learning — covering fundamentals, computer vision, large language models, and speech processing.

## Structure

```
.
├── mnist/
├── vision-transfer-learning/
├── llm/
├── speech/
├── demos/
└── README.md
```

### `mnist/`
MNIST digit classification implemented across different frameworks and levels of abstraction — useful for comparing raw NumPy, PyTorch (at varying levels of abstraction), and Keras approaches to the same problem.

- `MNIST_Numpy.ipynb` — a from-scratch implementation using only NumPy, for understanding the underlying mechanics.
- `MNIST_Torch.ipynb` / `MNIST_Torch_Module.ipynb` / `MNIST_Torch_easy.ipynb` — PyTorch versions showing progressively higher levels of abstraction.
- `MNIST_Keras.ipynb` — a fully-connected network baseline in Keras.
- `MNIST_Keras_CNN.ipynb` — the convolutional counterpart, for comparing FCN vs. CNN performance.

### `vision-transfer-learning/`
Image classification using transfer learning with VGG16, plus a baseline CNN example.

- `Dogs_vs_Cats_Keras.ipynb` — a CNN trained from scratch on the classic dogs-vs-cats dataset.
- `Feature_Extraction_VGG16.ipynb` — using a frozen pretrained VGG16 as a feature extractor.
- `Fine-tuned_VGG16.ipynb` — unfreezing and fine-tuning VGG16 layers, building on the feature-extraction notebook.

### `llm/`
Large language model work, spanning a from-scratch transformer and fine-tuning of an existing open model.

- `LLM_Keras_Kalevala.ipynb` — a transformer trained from scratch (Keras 3, SentencePiece tokenizer) on the Kalevala.
- `LLM_Keras_Kalevala_pieni.ipynb` — a smaller version of the same model, for faster training/demo purposes.
- `Gemma_LoRA_Finetuning.ipynb` — LoRA fine-tuning of a Gemma model.
- `Gemma_3_Finetune.ipynb` — fine-tuning Gemma 3.

### `speech/`
Speech recognition examples.

- `Puheentunnistus.ipynb` — Finnish-language speech recognition example.
- `Whisper_simple.ipynb` — a simple Whisper-based transcription example.

### `demos/`
Standalone class demonstrations of core concepts underlying the rest of the repo — useful background before diving into the model-building notebooks elsewhere.

- `Fourier.ipynb` — Fourier transform basics.
- `Konvoluutio.ipynb` — convolution operations explained and visualized.
- `cameraman.tif` — a standard test image used by the notebooks above.
- `Gradient_Descent.ipynb` — general-purpose gradient descent demo.

## Notes

- Notebook outputs are stripped automatically on commit via `nbstripout` to keep diffs clean — see `.gitattributes`.
- Some notebooks are intentionally kept in multiple versions (e.g. the MNIST PyTorch variants, or the two Kalevala models) to illustrate a progression — from a lower-level to a higher-level implementation, or from a larger to a smaller model — rather than being redundant duplicates.