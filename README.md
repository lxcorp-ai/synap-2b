# Synap-2b

<img src="https://huggingface.co/lxcorp/Synap-2b/resolve/main/synap_logo.png" width="400" align="center">

## 📖 Sobre o Modelo

**Synap-2b** é um modelo de linguagem de **2 bilhões de parâmetros**, desenvolvido pela **λχ Corp. (Marius Jabami)**.  
Ele foi projetado para **geração de texto**, **raciocínio matemático** e **pesquisa em LLMs**, com suporte a **Português** e **Inglês**.  

⚠️ Este modelo é **privado** e não está disponível para download, mas pode ser acessado via Space na Hugging Face.

---

## 🚀 Como Usar

```python
import torch
from transformers import pipeline

model_id = "lxcorp/Synap-2b"

pipe = pipeline(
    "text-generation",
    model=model_id,
    torch_dtype=torch.bfloat16,
    device_map="auto"
)

text = pipe("Resolva: 2x + 5 = 15")
print(text)
```

---

## 🧠 Detalhes Técnicos

Parâmetros: 2B

Linguagens: Português, Inglês

Dataset: orca-math-portuguese-64k

## Arquitetura:

Dimensão do modelo: 2048

MLP: 8192

Camadas: 28

Heads: 16

Contexto: 4096 tokens




---

📊 **Avaliação**

| Benchmark | Synap-2b |
|-----------|----------|
| MMLU      | 52.0     |
| ARC E     | 82.2     |
| ARC C     | 64.6     |
| PIQA      | 78.5     |
| SIQA      | 62.3     |
| **Média** | **61.1** |



---

## ⚡ Hardware & Treinamento

Treinado em GPUs NVIDIA (detalhes internos privados).

## Framework: Transformers.

Técnicas: Fine-tuning em dataset educacional + ajustes para raciocínio matemático.



---

## 📜 Licença

Modelo disponibilizado sob licença CC, uso controlado e privado.


---

## ✍️ Citação

@misc{synap2b2025,
  author = {Marius Jabami},
  title = {Synap-2b: Fine-tuned 2B Language Model},
  year = {2025},
  howpublished = {\url{https://huggingface.co/lxcorp/Synap-2b}}
}


---

Desenvolvido com ❤️ por Marius Jabami • λχ Corp.