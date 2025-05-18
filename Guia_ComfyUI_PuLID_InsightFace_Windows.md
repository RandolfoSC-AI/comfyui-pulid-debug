# Guia Completo: Instalação do ComfyUI, PuLID, InsightFace, Flux e StD no Windows (Ambiente Virtual)

---

## 1. Instalação do ComfyUI (Tradicional, em Ambiente Virtual)

### 1.1. Instalar o Python

- Baixe o Python 3.10.x (recomendado para máxima compatibilidade):
  - [Download Python 3.10.x para Windows](https://www.python.org/downloads/windows/)
- Marque a opção **“Add Python to PATH”** na instalação.

### 1.2. Criar uma pasta para o projeto

```bash
mkdir C:\ComfyUI
cd C:\ComfyUI
```

### 1.3. Criar e ativar o ambiente virtual

```bash
python -m venv venv
venv\Scripts\activate
```
> Você saberá que está ativado quando aparecer `(venv)` antes do caminho no prompt.

### 1.4. Baixar o ComfyUI (versão tradicional)

```bash
git clone https://github.com/comfyanonymous/ComfyUI.git .
```
- Ou baixe o ZIP de [https://github.com/comfyanonymous/ComfyUI](https://github.com/comfyanonymous/ComfyUI) e extraia na pasta do projeto.

### 1.5. Instalar as dependências do ComfyUI

```bash
pip install -r requirements.txt
```

### 1.6. Testar o ComfyUI

```bash
python main.py
```
- Acesse: http://127.0.0.1:8188 no navegador.  
- Feche com Ctrl+C para seguir para as próximas instalações.

---

## 2. Instalação do PuLID

### 2.1. Baixar o node PuLID

- Na pasta `ComfyUI/custom_nodes`:
  ```bash
  git clone https://github.com/cubiq/PuLID_ComfyUI.git
  ```
  - Ou baixe o ZIP em: [https://github.com/cubiq/PuLID_ComfyUI](https://github.com/cubiq/PuLID_ComfyUI) e extraia.

### 2.2. Instalar dependências obrigatórias

```bash
pip install facexlib
```

### 2.3. Baixar os modelos do PuLID

- Os arquivos `.pth` (modelos) devem ir em `ComfyUI/models/pulid/`.
- Veja instruções detalhadas no README:  
  [PuLID no GitHub](https://github.com/cubiq/PuLID_ComfyUI)
- O modelo EVA CLIP normalmente será baixado automaticamente na primeira execução.
- O facexlib também baixa modelos automaticamente, mas pode ser necessário baixar manualmente se houver erro.

### 2.4. Reinicie o ComfyUI

---

## 3. Instalação do InsightFace

### 3.1. Baixar o node InsightFace

- Na pasta `ComfyUI/custom_nodes`:
  ```bash
  git clone https://github.com/ltdrdata/ComfyUI-InsightFace.git
  ```
  - Ou baixe o ZIP em: [https://github.com/ltdrdata/ComfyUI-InsightFace](https://github.com/ltdrdata/ComfyUI-InsightFace) e extraia.

### 3.2. Instalar dependências obrigatórias

```bash
pip install insightface onnxruntime
```
- Se der erro de compilação, pode ser necessário instalar uma versão `.whl` específica para seu Python.
- Veja dicas aqui: [https://www.1ai.net/en/15997.html](https://www.1ai.net/en/15997.html)

### 3.3. Baixar os modelos InsightFace

- Os modelos `.onnx` ou `.pth` são baixados automaticamente pelo node; se der erro, baixe manualmente e coloque nas pastas indicadas pelo README.

### 3.4. Reinicie o ComfyUI

---

## 4. Flux, StD e outros nodes/modelos

- Instale nodes customizados colocando-os em `ComfyUI/custom_nodes`.
- Modelos (SDXL, SD1.5, LoRA, etc.) vão em `ComfyUI/models/`.

#### Links Úteis:
- [Como instalar custom nodes no ComfyUI (Wiki)](https://comfyui-wiki.com/en/install/install-custom-nodes)
- [Guia Flux (Wiki)](https://comfyui-wiki.com/en/tutorial/advanced/flux1-comfyui-guide-workflow-and-examples)
- [Dependencies - ComfyUI Docs](https://docs.comfy.org/essentials/core-concepts/dependencies)

---

## 5. Dicas Extras

- Sempre leia o README de cada node customizado.
- Se faltar algum modelo ou arquivo, verifique as mensagens de erro no terminal.
- Se tiver dúvida sobre onde colocar um arquivo, pergunte!

---

## 6. Tutoriais e Referências

- [Manual Installation - ComfyUI (Docs)](https://docs.comfy.org/installation/manual_install)
- [PuLID no RunComfy](https://www.runcomfy.com/comfyui-nodes/PuLID_ComfyUI)
- [YouTube: How To Install Pulid ComfyUI in 2025](https://www.youtube.com/watch?v=cO0vVLkFMx4)
- [YouTube: Como INSTALAR O INSIGHTFACE no COMFYUI | SEM ERROS](https://www.youtube.com/watch?v=tIwEP_jb8pI)

---

*Guia gerado com auxílio do GitHub Copilot, 18/05/2025.*
