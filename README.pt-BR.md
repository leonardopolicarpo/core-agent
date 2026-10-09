> 🇺🇸 Este README também está disponível em [inglês](README.md).

# 🧠 Core Agent

O **Core Agent** é o cérebro central de agentes inteligentes com memória persistente.
Projetado para integrar-se a interfaces (como chat web ou assistente por voz), consumir múltiplos modelos LLMs (como o Gemini) e evoluir constantemente com base nas interações.

> Este projeto é o coração do seu ecossistema inteligente — a base para construir agentes com personalidade, voz e aprendizado constante.

---

## ✨ Visão Geral

O Core Agent permite:

- Conversar com usuários via texto ou voz
- Armazenar memórias de curto, médio e longo prazo
- Integrar diferentes LLMs (Gemini, LLaMA, etc.)
- Coletar dados para treinar agentes personalizados
- Evoluir com base em interações e construir especialistas

---

## 🧠 Funcionalidades

- 📚 **Memória persistente** com MongoDB
- 🧩 **Arquitetura modular de agentes** (ex: Gemini)
- 🔁 **Collector** para treinar agentes a partir de interações
- 🧠 **Gerador de contexto inteligente**
- 🧠 **Memória de curto prazo** funcional (ultimas interações)
- 🗣️ **TTS (Text-to-Speech)**
- 🎤 **STT (Speech-to-Text)** para interações por voz
- 💻 Interface CLI funcional e legado
- 🌐 API FastAPI pronta para Web (com documentação automática)

---

## ⚒️ Tecnologias

- **Python 3.11+**
- **FastAPI** – API REST moderna
- **MongoDB** – banco de dados para sessões/memórias
- **Pydantic** – validação de dados
- **Google Generative AI** – LLM padrão atual (Gemini)
- **Docker** – para banco de dados local
- **TTS/STT** – integração com voz
- **dotenv** – gerenciamento de variáveis

---

## 📂 Estrutura do Projeto

```
core-agent/
├── api/                # Rotas FastAPI
├── agents/             # Agentes (ex: GeminiAgent)
├── audio/              # TTS/STT
├── cli/                # CLI legado (ainda funcional)
├── core/               # Engine principal (ex: run_agent)
├── memory/             # Repositório, conexão e manipulação com MongoDB
├── scripts/            # Scripts auxiliares (ex: reset do banco)
├── utils/              # Helpers para geração de contexto e outros
├── main.py             # Ponto de entrada da CLI
├── requirements.txt    # Dependências
├── docker-compose.yml  # Subir MongoDB com facilidade
└── .env                # Variáveis de ambiente (.env.example incluso)
```

---

## ⚙️ Como rodar localmente

### Requisitos

- Python 3.11+
- MongoDB rodando localmente ou via Docker

### 1. Clone o repositório

```bash
git clone https://github.com/leonardopolicarpo/core-agent.git
cd core-agent
```

### 2. Crie o ambiente virtual e ative

```bash
python -m venv .venv
source .venv/bin/activate  # Linux/macOS
# .venv\Scripts\activate.bat  # Windows
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

### 4. Configure as variáveis de ambiente

Crie um `.env`:

```env
GEMINI_API_KEY=your_google_generative_ai_key
MONGO_URI=mongodb://localhost:27017
```

### 5. Rode a API

```bash
uvicorn api.main:app --reload
```

Acesse a API: [http://localhost:8000/docs](http://localhost:8000/docs)

---

## 🐳 Rodar MongoDB com Docker (opcional)

```bash
docker compose up -d
```

Isso subirá o MongoDB localmente na porta `27017`.

---

## 🧠 Sobre o projeto

Este repositório é o coração da arquitetura planejada para múltiplas aplicações com IAs personalizadas.\

---

## 📄 Licença

Este projeto está licenciado sob a **Licença MIT** - consulte o arquivo [LICENSE](LICENSE) para obter detalhes.

---

## 👤 Autor

Desenvolvido por **Leonardo Policarpo**\
🔗 [linkedin.com/in/leonardo-policarpo](https://linkedin.com/in/leonardo-policarpo)

