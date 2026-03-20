# FastAPI Gemini API: Solução de IA Generativa com Python

![img_1.png|width=225,height=80,id=Oku3rtkeJ2NEST8uK2CFQc](img_1.png)

Este projeto apresenta uma **API robusta e escalável** desenvolvida com **FastAPI** em Python, integrando-se ao modelo de **Inteligência Artificial Generativa (GenAI) Google Gemini**. A solução foi arquitetada para facilitar a interação com modelos de linguagem avançados, oferecendo um *backend* eficiente e um *frontend* simplificado para demonstração.

## ✨ Funcionalidades Principais

- **Interação com Google Gemini:** Envio de *prompts* e recebimento de respostas do modelo de linguagem Gemini.

- **API RESTful:** Exposição de *endpoints* bem definidos para comunicação cliente-servidor.

- **Interface de Usuário (Frontend):** Um *frontend* básico para demonstração interativa da funcionalidade da API.

- **Documentação Interativa:** Geração automática de documentação da API via Swagger UI e ReDoc para fácil exploração e teste.

- **Validação de Dados:** Garantia da integridade dos dados de entrada e saída através de esquemas robustos.

## ⚙️ Tecnologias e Ferramentas

Este projeto utiliza um *stack* tecnológico moderno e eficiente:

- **FastAPI:** *Framework* web de alta performance para construção de APIs assíncronas em Python.

- **Pydantic:** Biblioteca para validação de dados e gerenciamento de configurações, garantindo a tipagem e a estrutura dos dados da API.

- **Uvicorn:** Servidor ASGI (Asynchronous Server Gateway Interface) otimizado para executar aplicações FastAPI de forma rápida e eficiente.

- **Poetry:** Ferramenta para gerenciamento de dependências e empacotamento de projetos Python, assegurando ambientes virtuais isolados e reprodutíveis.

- **Google Generative AI SDK:** Biblioteca oficial para integração programática com os modelos de IA Generativa do Google, incluindo o Gemini.

- **python-dotenv:** Utilizado para carregar variáveis de ambiente de um arquivo `.env`, facilitando a gestão de credenciais e configurações sensíveis.

## 📦 Instalação e Configuração

Para configurar e executar o projeto localmente, siga os passos abaixo:

1. **Clonar o Repositório:**

   ```bash
   git clone https://github.com/seu-usuario/Python-Projeto.git
   cd Python-Projeto
   ```

1. **Configuração da Chave de API:**

   Crie um arquivo `.env` na raiz do projeto e adicione sua chave de API do Google Gemini:

   ```
   GOOGLE_API_KEY="sua-chave-aqui"
   ```

   *Obtenha sua chave de API no *[*Google AI Studio*](https://aistudio.google.com/app/apikey)*.*

1. **Instalar Dependências:**

   Utilize o Poetry para instalar as dependências do projeto:

   ```bash
   poetry install
   ```

   Alternativamente, se preferir `pip`:

   ```bash
   pip install -r requirements.txt
   ```

## ▶️ Executando a Aplicação

Para iniciar o servidor da API e o *frontend* de demonstração:

Com Poetry:

```bash
poetry run uvicorn server:app --reload
```

Após a inicialização, acesse a aplicação no seu navegador:

- **Frontend do Chat:** 👉 `http://127.0.0.1:8000/`

### Testes Automatizados

Para executar os testes unitários e de integração do projeto:

```bash
pytest tests/test_chat.py -v -s -W ignore::pytest.PytestConfigWarning
```

## 📘 Documentação da API

O FastAPI gera automaticamente interfaces interativas para a documentação da API:

- **Swagger UI:** 👉 `http://127.0.0.1:8000/docs`
  - Ideal para desenvolvedores testarem os *endpoints* diretamente no navegador, com suporte a autenticação e exemplos de requisição/resposta.

- **ReDoc:** 👉 `http://127.0.0.1:8000/redoc`
  - Oferece uma visualização mais limpa e organizada da especificação da API, excelente para documentação oficial e consulta.

## 📡 Endpoints da API

### `POST /chat/ask`

Envia um *prompt* textual para o modelo Google Gemini e retorna a resposta gerada.

- **Requisição (Body JSON ):**

   ```json
   {
     "prompt": "Qual é a capital do Brasil?"
   }
   ```

- **Resposta (Body JSON):**

   ```json
   {
     "output": "A capital do Brasil é Brasília."
   }
   ```

## 🖥️ Arquitetura do Frontend

O *frontend* de demonstração, localizado em `frontend/index.html`, é uma interface simples que:

- Realiza requisições assíncronas (`fetch`) para o *endpoint* `/chat/ask`.

- Permite a entrada de *prompts* via `textarea` e exibe as respostas do Gemini em uma `div` dedicada.

## 📌 Estrutura do Projeto e Boas Práticas

O projeto segue uma estrutura modular e em camadas para promover a organização, manutenibilidade e escalabilidade:

- **`Models/`****:** Define os esquemas de entrada e saída de dados utilizando Pydantic, garantindo a validação e serialização/desserialização.

- **`Services/`****:** Contém a lógica de negócio principal, incluindo a integração com o Google Gemini e o processamento das interações.

- **`Routes/`****:** Gerencia os *endpoints* da API, roteando as requisições para os serviços apropriados.

- **`Frontend/`****:** Abriga os arquivos estáticos da interface de usuário para demonstração.

As rotas da API são acessíveis via `/chat/ask`, enquanto a interface de usuário está disponível na raiz (`/`).

## 👤 Autor

**Mateus Venâncio**


