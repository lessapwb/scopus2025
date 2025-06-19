
# 📊 Análise Bibliométrica com IA usando Dados da Scopus

Este projeto realiza uma análise inteligente de publicações científicas extraídas da base **Scopus**, utilizando técnicas de NLP (Processamento de Linguagem Natural) e **modelos de linguagem (LLMs)** como o `gpt-4o`. A ferramenta foi projetada para entregar **insights reais e confiáveis**, sem alucinação, a partir de uma base estruturada de artigos científicos.

---

## 🚀 Objetivo

Permitir que pesquisadores e analistas explorem uma base de dados bibliográfica com auxílio de IA de forma segura, objetiva e interpretável, com foco em:

- Identificação de temas emergentes
- Reconhecimento de padrões de autoria, periódicos e citações
- Síntese textual a partir de centenas de artigos
- Geração de um **chatbot confiável** que responde exclusivamente com base na base extraída

---

## 🧠 Tecnologias Utilizadas

- **Python 3.11+**
- [OpenAI API](https://platform.openai.com/)
- `pandas`
- `openai`
- `python-dotenv`
- `tiktoken`
- CSV extraído da [API da Scopus](https://dev.elsevier.com/documentation/SCOPUSSearchAPI.wadl)

---

## 📁 Estrutura do Projeto

```
📦 projeto-scopus-ia
├── base_scopus_ddm.csv         # Base de artigos extraída da API da Scopus
├── POC_Scopus_API.ipynb        # Notebook interativo com coleta, estruturação e chatbot
├── .env                        # Contém sua chave da OpenAI (não versionar)
├── README.md                   # Este documento
```

---

## 📌 Pré-requisitos

1. **Python instalado** (versão 3.10+ recomendada)
2. Crie um arquivo `.env` com a seguinte variável:

```
OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
scopus_api=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

3. Instale as dependências:

```bash
pip install pandas openai python-dotenv tiktoken
```

---

## 🧪 Como Funciona

O notebook realiza:

1. **Extração automática da base da Scopus via API**
2. **Tratamento e limpeza da base**, removendo colunas irrelevantes
3. **Busca de resumos completos (abstracts)** via DOI
4. **Criação de um chatbot local interativo**, com base textual estruturada
5. A IA responde apenas com base nos artigos enviados, sem alucinar

**Observação:** é necessário usar uma VPN Institucional, ou estar uma uma instituição que permita acessar a Scopus Search, para permitir grande quantidade de registros da Scopus.

---

## 🛡️ Segurança e Controle

- O modelo **não alucina**, pois trabalha **exclusivamente com os registros estruturados**
- O chatbot mantém **histórico de contexto**, limitado aos tokens permitidos
- Nenhum dado é enviado a terceiros além da OpenAI

---

## 📈 Resultados Esperados

- Análise objetiva dos temas abordados na base
- Identificação de padrões de coautoria e citação
- Tendências de publicação ao longo do tempo
- Um chatbot interativo para explorar a base com confiabilidade

---

## 💬 Exemplo de Perguntas ao Chatbot

- Quais são os principais temas emergentes nos artigos?
- Qual periódico mais aparece?
- Qual autor é mais recorrente?
- Há alguma tendência temporal nas publicações?

---

## 💻 Executando no Google Colab

1. Suba os arquivos `base_scopus_ddm.csv`, `.env` e o notebook `.ipynb` para o Colab.
2. Execute célula por célula.
3. Para uso seguro, adicione manualmente a chave no notebook se necessário:
```python
import os
os.environ['OPENAI_API_KEY'] = "sua-chave-aqui"
```

---

## ✨ Autor

Desenvolvido por **Patrick Lessa**  
📧 E-mail: patrickwbarbosa@gmail.com  
🔗 LinkedIn: [linkedin.com/in/lessapwb](https://www.linkedin.com/in/lessapwb/)

---

## 📜 Licença

Este projeto é livre para uso acadêmico. Para fins comerciais, consulte os termos de uso da Scopus e da OpenAI.
