# Neuroverkkoprojekti

Jupyter notebooks for teaching neural networks: fully connected and convolutional
networks, transfer learning, transformers and language models, and speech recognition.

## Structure

```
.
├── mnist/                     MNIST in NumPy, PyTorch and Keras
├── pytorch/                   the same MNIST models in Keras and in pure PyTorch
├── vision-transfer-learning/  CNN from scratch, VGG16 feature extraction and fine-tuning
├── llm/                       transformer from scratch (Kalevala), Gemma fine-tuning
├── speech/                    speech recognition with Whisper
├── demos/                     convolution, Fourier transform, gradient descent
└── data/                      small data files used by the notebooks
```

### `mnist/`
MNIST digit classification at different levels of abstraction.

- `MNIST_Numpy.ipynb` — a fully connected network from scratch in NumPy (Keras only loads the data).
- `MNIST_Torch.ipynb`, `MNIST_Torch_Module.ipynb`, `MNIST_Torch_easy.ipynb` — PyTorch from manual tensor operations to `nn.Module` and `nn.Sequential`.
- `MNIST_Keras.ipynb` — a fully connected network in Keras.
- `MNIST_Keras_CNN.ipynb` — the convolutional counterpart, for comparing FCN and CNN.

### `pytorch/`
Short, parallel versions of the same models for comparing Keras and pure PyTorch.
Some overlap with `mnist/` is intentional.

- `MNIST_Torch.ipynb` — a fully connected network with manual forward and backward passes.
- `MNIST_Torch_simple.ipynb` — the same network with `nn.Sequential` and a `DataLoader`.
- `MNIST_Torch_CNN.ipynb` — a CNN with `nn.Sequential`.
- `MNIST_Torch_CNN_Functional.ipynb` — the same CNN as an `nn.Module` subclass.
- `MNIST_Keras_CNN.ipynb` — the same CNN in Keras.

The MNIST data is downloaded into `pytorch/mnist_data/` on the first run.

### `vision-transfer-learning/`
Image classification on dogs vs. cats.

- `Dogs_vs_Cats_Keras.ipynb` — a CNN trained from scratch, with data augmentation.
- `Feature_Extraction_VGG16.ipynb` — a frozen pretrained VGG16 as a feature extractor.
- `Fine-tuned_VGG16.ipynb` — fine-tuning the top layers of VGG16.

### `llm/`
- `LLM_Keras_Kalevala_pieni.ipynb` — a small transformer trained from scratch on the Kalevala (Keras 3, SentencePiece tokenizer). The starting point for project 3.
- `LLM_Keras_Kalevala.ipynb` — a larger version of the same model.
- `Gemma_3_Finetune.ipynb` — LoRA fine-tuning of Gemma 3 1B with Keras and KerasHub.
- `Gemma_LoRA_Finetuning.ipynb` — LoRA fine-tuning of Gemma with Hugging Face `transformers` and `peft`.

The text file `kalevala_puhdas.txt` is not in the repository; it is shared on the course page.

### `speech/`
- `Puheentunnistus.ipynb` — Finnish speech recognition with Whisper (Hugging Face `transformers`), waveform and mel spectrogram, and translation to English.
- `Whisper_simple.ipynb` — a Gradio interface for recording and transcribing speech.

### `demos/`
Class demonstrations of the ideas behind the other notebooks.

- `Konvoluutio.ipynb` — convolution of an image with different kernels.
- `Fourier.ipynb` — the discrete Fourier transform and the spectrogram.
- `Gradient_Descent.ipynb` — gradient descent.

### `data/`
- `cameraman.tif` — the standard test image used in `Konvoluutio.ipynb`.

## Notes

- Notebooks are committed with their outputs, so results and figures are visible without running them.
- Datasets, trained models (`*.keras`, `*.h5`), text files and audio recordings are not tracked; the notebooks download or create them.
