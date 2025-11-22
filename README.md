# 🔖 AWS Simulator DVA-C02

Aplicação web interativa para simulados da certificação **AWS Developer Associate (DVA-C02)**, desenvolvida com Streamlit.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-1.28+-red.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 📋 Sobre o Projeto

Simulador completo para preparação do exame AWS Developer Associate (DVA-C02) com 65 questões, timer de 130 minutos e correção automática.

### ✨ Funcionalidades

- ⏱️ **Timer em tempo real** - Contador regressivo de 130 minutos (tempo oficial do exame)
- 📊 **65 Questões** - Simulado completo baseado no exame real
- ✅ **Múltipla escolha** - Suporte para questões de resposta única e múltipla
- 🎯 **Correção automática** - Feedback imediato após finalização
- 📈 **Métricas de desempenho** - Percentual de acertos e quantidade
- ❌ **Identificação visual** - Marcação visual das questões erradas
- 🔄 **Carregamento dinâmico** - Questões carregadas do Google Drive via CSV

## 🚀 Tecnologias Utilizadas

- **Python 3.8+**
- **Streamlit** - Framework para aplicações web
- **Pandas** - Manipulação de dados
- **Requests** - Requisições HTTP
- **Python-dotenv** - Gerenciamento de variáveis de ambiente

## 📦 Instalação

### Pré-requisitos

- Python 3.8 ou superior
- pip (gerenciador de pacotes Python)

### Passo a passo

1. **Clone o repositório**
```bash
git clone https://github.com/aryribeiro/aws-simulator3.git
cd aws-simulator3
```

2. **Crie um ambiente virtual (recomendado)**
```bash
python -m venv venv

# Windows
venv\Scripts\activate

# Linux/Mac
source venv/bin/activate
```

3. **Instale as dependências**
```bash
pip install -r requirements.txt
```

4. **Configure as variáveis de ambiente**

Crie um arquivo `.env` na raiz do projeto:
```env
GOOGLE_DRIVE_CSV_URL=https://drive.google.com/uc?export=download&id=SEU_ID_AQUI
```

5. **Execute a aplicação**
```bash
streamlit run app.py
```

A aplicação estará disponível em `http://localhost:8501`

## 📄 Estrutura do Arquivo CSV

O arquivo CSV deve seguir o formato:

```csv
question,options,answer,multiple
"Qual serviço AWS...","['A) EC2', 'B) Lambda', 'C) S3', 'D) RDS']","['B) Lambda']",false
"Selecione os serviços...","['A) DynamoDB', 'B) Aurora', 'C) RDS']","['A) DynamoDB', 'B) Aurora']",true
```

### Campos obrigatórios:
- **question**: Texto da pergunta
- **options**: Lista de opções no formato JSON
- **answer**: Lista com resposta(s) correta(s) no formato JSON
- **multiple**: `true` para múltipla escolha, `false` para única escolha

## 🎮 Como Usar

1. Acesse a aplicação no navegador
2. Clique em **"Iniciar Simulado"**
3. Responda todas as 65 questões
4. Clique em **"Finalizar Simulado"**
5. Visualize sua nota e questões erradas
6. Pressione **F5** para reiniciar

## 🛠️ Estrutura do Projeto

```
aws-simulator3
│
├── app.py                 # Aplicação principal
├── .env                   # Variáveis de ambiente (não versionado)
├── requirements.txt       # Dependências Python
├── README.md             # Documentação
└── .gitignore            # Arquivos ignorados pelo Git
```

## 📝 Arquivo requirements.txt

```txt
streamlit>=1.28.0
pandas>=2.0.0
requests>=2.31.0
python-dotenv>=1.0.0
```

## 🔒 Segurança

- Nunca commite o arquivo `.env` com credenciais
- Use variáveis de ambiente para dados sensíveis
- Mantenha o arquivo `.gitignore` atualizado

## 🤝 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para:

1. Fazer fork do projeto
2. Criar uma branch para sua feature (`git checkout -b feature/NovaFuncionalidade`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/NovaFuncionalidade`)
5. Abrir um Pull Request

## 📧 Contato

Por **Ary Ribeiro**: aryribeiro@gmail.com
