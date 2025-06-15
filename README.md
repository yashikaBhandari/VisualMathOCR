# 🧠 LaTeX Equation Reader using Vision Language Models

This project fine-tunes a 4-bit Qwen2-VL model to generate LaTeX code from images of mathematical expressions.

## 🔍 Objective
To build a model that understands handwritten or printed math images and converts them into correct LaTeX format.

## 🧰 Tech Stack
- 🤗 Transformers (`Qwen2-VL-7B-Instruct`)
- 🧵 Unsloth (efficient LoRA fine-tuning)
- 🧠 PEFT (Parameter Efficient Fine-Tuning)
- 🖼️ PIL for image handling
- 📦 HuggingFace `datasets` for LaTeX_OCR

## 🚀 Features
- Vision + Text Input using Chat Templates
- Fine-tuning using LoRA on GPU
- Generates accurate LaTeX expressions

## 📦 Dataset
[`unsloth/Latex_OCR`](https://huggingface.co/datasets/unsloth/Latex_OCR)

Example:
```json
{
  "image": "<PIL Image>",
  "text": "\\frac{N}{M} \\in \\mathbb{Z}"
}

```
## 📸 Sample Inference
Input:
example image contains like this :
          ( a/b )+ √x

Output:

latex
```
\frac{a}{b} + \sqrt{x}
```
## 📈 Training Configuration

Batch size: 2

Accumulation steps: 4

Max steps: 30

Learning rate: 2e-4

Optimizer: AdamW (8-bit)

## 💡 Future Scope

Handle handwritten math expressions

Deploy as a web service for real-time inference

Add speech-to-LaTeX capability

## ✨ Acknowledgements

Thanks to Unsloth, TRL, and HuggingFace Datasets for enabling efficient multimodal fine-tuning.

yaml


---

## 💼 Will Recruiters See the Code?

✅ **Yes**, **GitHub repositories** are often reviewed by recruiters and hiring managers, especially for:
- Internships
- Research positions
- AI/Machine Learning roles

### Tips:
- Include a clear `README.md` (like above)
- Push your `train.py` or `finetune_latex_ocr.py`
- Include a few `sample_outputs/` images with generated LaTeX

---

