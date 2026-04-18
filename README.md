# 🎙️ Transcrição de Áudio Simples PT-BR

Uma aplicação web moderna, limpa e funcional para transcrição de áudio em Português Brasileiro, utilizando Inteligência Artificial de ponta para converter reuniões presenciais e entrevistas em documentos editáveis de forma rápida e segura.

🚀 **Acesse a aplicação rodando na nuvem:** https://transcricaoaudiosimplesptbr.streamlit.app/

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)
![OpenAI Whisper](https://img.shields.io/badge/OpenAI%20Whisper-412991?style=for-the-badge&logo=openai&logoColor=white)

---

## 🌟 Funcionalidades

- **Transcrição de Alta Precisão:** Utiliza o modelo `small` do OpenAI Whisper, configurado especificamente para captar nuances do Português (PT-BR).
- **Compatibilidade Total:** Suporte para múltiplos formatos de áudio: `.mp3`, `.wav`, `.m4a`, `.ogg` e `.flac`.
- **Interface Focada em UX:** 
  - Feedback em tempo real sobre cada etapa do processamento.
  - Design limpo, sem distrações e fácil de usar para usuários leigos.
- **Exportação Multiformato:** Converta o áudio e baixe o resultado imediatamente:
  - **PDF** (Ideal para relatórios e leitura rápida).
  - **DOCX** (Arquivo editável para Microsoft Word).

---

## 🛠️ Tecnologias e Bibliotecas

- **[Streamlit](https://streamlit.io/):** Utilizado para construir a interface web rápida e interativa.
- **[OpenAI Whisper](https://github.com/openai/whisper):** O "cérebro" da aplicação, responsável pelo reconhecimento de fala via rede neural.
- **[Pydub](http://pydub.com/):** Biblioteca essencial para manipulação, padronização e conversão de codecs de áudio.
- **[FPDF2](https://pyfpdf.github.io/fpdf2/) & [Python-Docx](https://python-docx.readthedocs.io/):** Utilizadas para a geração dinâmica dos arquivos de exportação.

---

## 🚀 Como Executar o Projeto

### 1. Pré-requisitos (Obrigatório)

O motor de processamento de áudio depende do **FFmpeg**. Certifique-se de que ele está instalado no seu sistema:

- **Windows:** Abra o terminal e digite `winget install ffmpeg`.
- **Linux:** Execute `sudo apt install ffmpeg`.
- **Mac:** Execute `brew install ffmpeg`.

### 2. Instalação do Ambiente

Clone o repositório e configure o ambiente virtual Python:

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio

# Crie um ambiente virtual (Recomendado Python 3.10 ou 3.11)
python -m venv .venv

# Ative o ambiente
# No Windows:
.venv\Scripts\activate
# No Linux/Mac:
source .venv/bin/activate

# Instale as dependências
pip install streamlit openai-whisper pydub fpdf2 python-docx audioop-lts

### 3. Execução

Com o ambiente ativo, inicie a aplicação com o comando:

```bash
python -m streamlit run app.py
```

A aplicação abrirá automaticamente no seu navegador padrão no endereço `http://localhost:8501`.

---

## 🧠 Decisões de Engenharia de Software

Para garantir um resultado de nível sênior, foram aplicadas as seguintes melhorias técnicas:

1. **Estabilidade de Idioma:** Configuramos o parâmetro `language='pt'` de forma fixa para evitar que o modelo tente adivinhar o idioma e acabe gerando textos em outros alfabetos (como coreano ou japonês).
2. **Otimização de Performance:** Utilizamos o modelo `small`. Ele é um equilíbrio ideal: muito mais preciso que o modelo `base`, mas ainda leve o suficiente para rodar em computadores comuns sem necessidade de placas de vídeo (GPU) profissionais.
3. **Robustez via FP16:** Desativamos o `fp16` para garantir que o processamento em CPUs (comum em ambientes de serviço público) ocorra sem erros de cálculo ou repetições infinitas de texto.

---

## 📝 Licença

Este projeto é um protótipo funcional desenvolvido durante o curso **Inteligência Artificial Aplicada à Gestão e Inovação no Serviço Público**.

---


> **Trabalho Final do Curso:** [Inteligência Artificial Aplicada à Gestão e Inovação no Serviço Público](https://sites.google.com/view/painel-turma1/projetos).
