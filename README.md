# Deep Learning Foundations

An approachable course in deep learning, built from concrete problems, intuition, and worked examples. The first four topics are available; the remaining topics are planned.

Each topic has two matching notebooks:

- **Notes** explain ideas from first principles, with small worked examples, practical uses, limitations, and common misunderstandings.
- **Code** demonstrates those ideas in Python and PyTorch, with short explanations and locally generated examples that run on CPU.

Read the notes for understanding, then run the companion to inspect the calculations and results. Notebook titles and headings are unnumbered so lessons can be shared independently. Course numbering appears in filenames and the table below.

The two-notebook structure and teaching approach are inspired by [Machine Learning Foundations](https://github.com/avdhanda44/machine-learning-foundations). This is a separate project.

## Course order

| No. | Topic | Status | Notes | Code |
| --- | --- | --- | --- | --- |
| 01 | Why Deep Learning? | Available | [Notes](01_Why_Deep_Learning_Notes.ipynb) | [Code](01_Why_Deep_Learning.ipynb) |
| 02 | The Artificial Neuron | Available | [Notes](02_The_Artificial_Neuron_Notes.ipynb) | [Code](02_The_Artificial_Neuron.ipynb) |
| 03 | Activation Functions | Available | [Notes](03_Activation_Functions_Notes.ipynb) | [Code](03_Activation_Functions.ipynb) |
| 04 | ANN and MLP Architecture | Available | [Notes](04_ANN_and_MLP_Architecture_Notes.ipynb) | [Code](04_ANN_and_MLP_Architecture.ipynb) |
| 05 | Tensors and Forward Propagation | Planned | — | — |
| 06 | Loss Functions | Planned | — | — |
| 07 | Gradients and Backpropagation | Planned | — | — |
| 08 | Optimizers | Planned | — | — |
| 09 | The Complete Training Loop | Planned | — | — |
| 10 | Training Problems and Solutions | Planned | — | — |
| 11 | Build Your First Neural Network | Planned | — | — |
| 12 | Embeddings and Latent Space | Planned | — | — |
| 13 | Transfer Learning | Planned | — | — |
| 14 | Self-Supervised Learning | Planned | — | — |
| 15 | Images as Tensors and Why CNNs Work | Planned | — | — |
| 16 | Convolution by Hand | Planned | — | — |
| 17 | CNN Architecture and Training | Planned | — | — |
| 18 | Important CNN Designs | Planned | — | — |
| 19 | Beyond Image Classification | Planned | — | — |
| 20 | Sequence Data and RNNs | Planned | — | — |
| 21 | LSTMs and GRUs | Planned | — | — |
| 22 | Attention | Planned | — | — |
| 23 | Transformers from First Principles | Planned | — | — |
| 24 | Encoder and Decoder Architectures | Planned | — | — |
| 25 | Generative Modeling Foundations | Planned | — | — |
| 26 | Autoencoders and VAEs | Planned | — | — |
| 27 | GANs | Planned | — | — |
| 28 | Diffusion Models | Planned | — | — |
| 29 | Language Model Foundations | Planned | — | — |
| 30 | Deep Learning Foundations Review | Planned | — | — |

## Run locally

Use Python 3.9–3.12 for the pinned dependency set. Create an isolated environment in the repository directory:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m ipykernel install --prefix .venv --name deep-learning-foundations --display-name "Deep Learning Foundations"
python -m notebook
```

On Windows, create the environment with `py -m venv .venv` and activate it with `.venv\Scripts\activate`. Select the **Deep Learning Foundations** kernel, open a code notebook, and choose **Restart Kernel and Run All Cells**.

PyTorch, NumPy, and Matplotlib provide the computations and plots; Notebook and ipykernel provide the notebook interface and kernel. Installing dependencies requires internet access. Running the notebooks needs no credentials, dataset downloads, GPU, or external services.

The first companion compares logistic regression on raw coordinates, logistic regression on a designed distance feature, and a small neural network on the same circular classification task. It keeps training, validation, and test examples separate and reports accuracy alongside decision-boundary plots. The other companions inspect hand-set calculations rather than claim trained-model performance.

Random seeds are set in every code notebook. Saved outputs show a reference run; small numerical differences across platforms are possible. Exercises intentionally change the demonstrations, so restore the original code before reproducing the saved results.

## Verified reference run

All four code companions were executed from separate fresh kernels on CPU using Python 3.9.6 and the pinned dependencies. All code cells and embedded assertions passed.

For Why Deep Learning?, held-out accuracy was 52.1% for logistic regression on raw coordinates, 99.2% for the distance-feature model, and 99.2% for the neural network. The exact geometry rule reached 100%. The neural network learned a useful curved boundary, but matched a much simpler model given the right feature. This synthetic experiment demonstrates representation learning; it does not establish that deep learning is generally superior.
