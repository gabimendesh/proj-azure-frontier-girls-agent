# 🎓 AZ-900 Study Assistant

## Assistente Inteligente para Preparação da Certificação Azure Fundamentals

[![Azure](https://img.shields.io/badge/Azure-AI%20Foundry-0078D4?logo=microsoft-azure)](https://ai.azure.com)
[![Python](https://img.shields.io/badge/Python-3.11-3776AB?logo=python)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-Educational-green)](LICENSE)

> Projeto desenvolvido para o **Azure Frontier Girls - 2025**

---

## 📋 Sobre o Projeto

O **AZ-900 Study Assistant** é um agente inteligente desenvolvido no Azure AI Foundry para auxiliar estudantes na preparação para a certificação Microsoft Azure Fundamentals (AZ-900). O agente oferece:

- 📝 **Quizzes Personalizados** - Geração de testes com 50+ perguntas sobre tópicos da AZ-900
- 📊 **Planos de Estudo** - Cálculo de tempo necessário e cronograma personalizado
- 📚 **Recomendação de Recursos** - Indicação de materiais oficiais e gratuitos
- 💬 **Explicações Didáticas** - Conceitos do Azure explicados de forma clara
- 🎯 **Acompanhamento** - Suporte motivacional e correção de quizzes

---

## 🏗️ Arquitetura da Solução

```
Azure AI Foundry
├── Agent: AZ-900 Study Assistant
│   ├── Model: GPT-4o-mini
│   ├── Instructions: Persona educacional
│   └── Tools:
│       └── Code Interpreter (Python)
│
├── Knowledge Base (Arquivos .txt)
│   ├── conceitos.txt (Fundamentos do Azure)
│   ├── desmitifying_azure.txt (Conceitos detalhados)
│   └── questions_answers.txt (Perguntas e respostas)
│
└── Functions (JSON + Python)
    ├── quiz_database.json (50+ perguntas)
    └── Funções executadas via Code Interpreter
```

---

## ✨ Funcionalidades Principais

### 1. 📝 Gerador de Quiz Interativo

O agente gera quizzes personalizados sobre diversos tópicos da AZ-900:

**Tópicos disponíveis:**
- IaaS, PaaS, SaaS
- Azure Storage (Blob, Files, tiers)
- Conceitos de Nuvem (Híbrida, CapEx/OpEx)
- SLA e disponibilidade
- Networking (VNet, VPN, ExpressRoute)
- Identity (Azure AD, MFA)
- Compute, Database, Management
- Cost Management e Monitoring

**Fluxo interativo:**
1. Usuário solicita quiz sobre um tópico
2. Agente apresenta perguntas (sem revelar respostas)
3. Usuário responde
4. Agente corrige com explicações detalhadas
5. Feedback motivacional baseado na pontuação

**Base de dados:** `quiz_database.json` com 50+ perguntas categorizadas

### 2. 📊 Calculadora de Tempo de Estudo

Calcula tempo necessário baseado em:
- Nível atual (iniciante, intermediário, avançado)
- Horas disponíveis por semana
- Experiência prévia em TI

**Retorna:**
- Total de horas necessárias
- Plano semanal detalhado (8 semanas)
- Data recomendada para o exame
- Dicas de estudo personalizadas

### 3. 📚 Recomendador de Recursos

Sugere materiais de estudo oficiais e gratuitos:
- Microsoft Learn (roteiros completos)
- Documentação oficial Azure
- Vídeos educacionais
- Laboratórios práticos
- Ferramentas úteis (calculadoras de preço e TCO)

Filtragem por:
- Idioma (português/inglês)
- Formato (vídeo/documentação/laboratório)
- Tópico específico

### 4. 💬 Explicador de Conceitos

Explica conceitos do Azure de forma didática:
- Linguagem acessível
- Analogias do dia a dia
- Comparação entre serviços similares
- Exemplos práticos
- Dicas para o exame

---

## 🛠️ Tecnologias Utilizadas

- **Azure AI Foundry** - Plataforma de desenvolvimento
- **GPT-4o-mini** - Modelo de linguagem
- **Code Interpreter** - Execução de Python na nuvem
- **Knowledge Base** - Base de conhecimento personalizada
- **Python** - Funções customizadas
- **JSON** - Base de dados de perguntas

---

## 📸 Demonstrações

(em algumas imagens borrei o id do agente por possíveis questões de privacidade)

### Criação e Configuração do Agente

#### 1. Criação do Agente
![Criação do Agent](./assets/criação%20do%20agent.png)
*Configuração inicial do agente no Azure AI Foundry*

#### 2. Code Interpreter Ativado
![Code Interpreter](./assets/adicionado%20o%20interpretador%20de%20código%201.png)
*Habilitação do Code Interpreter para execução de Python*

#### 3. Base de Conhecimento
![Adicionando Knowledge](./assets/adicionando%20base%20de%20conhecimento.png)
*Upload de arquivos .txt para a base de conhecimento*

![Knowledge Adicionada](./assets/base%20de%20conhecimento%20em%20adicionada.png)
*Confirmação dos arquivos processados*

---

### Interações com o Agente

#### 4. Primeira Interação
![Playground](./assets/playground%201.png)
*Interface do playground do Azure AI Foundry*

![Primeira Conversa](./assets/primeira%20interação%20com%20o%20chat.png)
*Apresentação do agente e suas capacidades*

---

#### 5. Quiz Interativo

![Quiz 1](./assets/pedindo%20um%20quiz%20para%20o%20agent%201.png)
*Solicitando um quiz sobre Azure Storage*

![Quiz 2](./assets/pedindo%20um%20quiz%20para%20o%20agent%202.png)
*Perguntas apresentadas sem revelar respostas*

![Quiz 3](./assets/pedindo%20um%20quiz%20para%20o%20agent%203.png)
*Usuário respondendo às perguntas*

![Quiz 4](./assets/pedindo%20um%20quiz%20para%20o%20agent%204.png)
*Correção detalhada com explicações e feedback*

---

#### 6. Plano de Estudos Personalizado

![Plano 1](./assets/plano%20de%20estudo.png)
*Solicitação de plano de estudos*

![Plano 2](./assets/plano%20de%20estudo%202.png)
*Cálculo de tempo necessário e cronograma*

![Plano 3](./assets/plano%20de%20estudo%203.png)
*Plano semanal detalhado com dicas*

---

#### 7. Recomendação de Recursos
![Recursos](./assets/recomendação%20de%20estudo.png)
*Lista de recursos oficiais Microsoft Learn em português*

---

#### 8. Suporte e Explicações

![Ajuda 1](./assets/pedindo%20ajuda%20para%20o%20agent.png)
*Solicitando explicação sobre conceitos difíceis*

![Ajuda 2](./assets/pedindo%20ajuda%20para%20o%20agent%202.png)
*Explicação didática com exemplos práticos*

---

#### 9. Exemplo Extra
![Receita](./assets/pedindo%20receita%20para%20o%20agent.png)
*Demonstração de versatilidade do agente (responde que foca em AZ-900)*

---

## 📂 Estrutura do Repositório

```
proj-azure-frontier-girls-agent/
│
├── README.md                           # Este arquivo
├── INSTRUCOES_AGENTE.md               # Instruções do sistema usadas no agente
│
├── assets/                            # Imagens e arquivos de suporte
│   ├── *.png                          # Screenshots das interações
│   ├── conceitos.txt                  # Base de conhecimento: Fundamentos
│   ├── desmitifying_azure.txt        # Base de conhecimento: Conceitos
│   ├── questions_answers.txt         # Base de conhecimento: Q&A
│   └── quiz_database.json            # Base de 50+ perguntas

```

---

## 🎯 Implementação Técnica

### Base de Conhecimento (Knowledge Base)

Três arquivos de texto foram adicionados à Knowledge Base do agente:

1. **conceitos.txt**
   - Fundamentos do Azure
   - Conceitos de nuvem
   - Modelos de serviço

2. **desmitifying_azure.txt**
   - Conceitos detalhados
   - Explicações aprofundadas
   - Comparações entre serviços

3. **questions_answers.txt**
   - Perguntas frequentes
   - Respostas estruturadas
   - Dicas para o exame

Esses arquivos foram processados pelo Azure AI Foundry e estão disponíveis para o agente consultar durante as conversas, garantindo respostas mais precisas e baseadas em conteúdo oficial.

### Code Interpreter

O **Code Interpreter** foi habilitado para permitir a execução de código Python diretamente no agente. Ele processa:

**Arquivo principal:** `quiz_database.json`
- 50+ perguntas sobre AZ-900
- Organizadas em 11 categorias
- 3 níveis de dificuldade (básico, intermediário, avançado)
- Explicações detalhadas para cada resposta

**Categorias:**
- `iaas` - Infrastructure as a Service (3 perguntas)
- `paas` - Platform as a Service (3 perguntas)
- `saas` - Software as a Service (2 perguntas)
- `storage` - Armazenamento Azure (4 perguntas)
- `cloud_concepts` - Conceitos de nuvem (4 perguntas)
- `sla` - Service Level Agreement (3 perguntas)
- `networking` - Redes Azure (3 perguntas)
- `identity` - Identidade e acesso (3 perguntas)
- `compute` - Serviços de computação (3 perguntas)
- `database` - Bancos de dados (2 perguntas)
- `management` - Gerenciamento Azure (3 perguntas)
- `cost` - Gerenciamento de custos (2 perguntas)
- `monitoring` - Monitoramento (2 perguntas)

### Instruções do Sistema

As instruções completas do agente estão documentadas em [`INSTRUCOES_AGENTE.md`](./INSTRUCOES_AGENTE.md).

**Principais diretrizes:**
- Persona educacional e motivadora
- Tom encorajador e paciente
- Respostas em português brasileiro
- Foco em didática e clareza
- Uso de analogias e exemplos práticos
- Apresentação de quizzes sem revelar respostas inicialmente
- Correção detalhada com explicações

---

## 🎓 Tópicos Cobertos (AZ-900)

O agente aborda todos os objetivos do exame AZ-900:

### 1. Conceitos de Nuvem (25-30%)
- Benefícios da computação em nuvem
- Modelos de nuvem: Público, Privado, Híbrido
- Tipos de serviço: IaaS, PaaS, SaaS
- Modelo de responsabilidade compartilhada
- CapEx vs OpEx

### 2. Arquitetura e Serviços Azure (35-40%)
- Componentes arquiteturais: Regiões, Zonas, Datacenters
- Recursos e grupos de recursos
- Serviços de computação: VMs, App Service, Functions, Containers
- Serviços de rede: VNet, VPN Gateway, ExpressRoute
- Serviços de armazenamento: Blob, Disk, Files, Archive
- Identidade: Azure AD (Entra ID), MFA
- Bancos de dados: SQL Database, Cosmos DB

### 3. Gerenciamento e Governança (30-35%)
- Ferramentas: Portal, CLI, PowerShell, ARM
- Monitoramento: Azure Advisor, Service Health, Monitor
- Governança: Policy, Blueprints, Locks
- Gerenciamento de custos: Calculadoras, Tags
- SLA e cálculos

---

## 🚀 Como Usar

### Exemplos de Comandos

**Gerar Quiz:**
```
Me dê um quiz sobre Azure Storage com 5 perguntas de nível intermediário
```

**Calcular Tempo de Estudo:**
```
Calcule meu plano de estudos. Sou iniciante e tenho 10 horas por semana disponíveis.
```

**Recomendar Recursos:**
```
Me recomende recursos de estudo em português, prefiro documentação e laboratórios práticos.
```

**Explicar Conceito:**
```
Explique a diferença entre IaaS, PaaS e SaaS com exemplos do Azure.
```

**Pedir Ajuda:**
```
Estou com dificuldade em entender SLA. Pode me ajudar?
```

---

## 📊 Métricas e Resultados

### Funcionalidades Implementadas
- ✅ **Code Interpreter** com funções customizadas
- ✅ **Base de conhecimento** com 3 documentos (25 KB)
- ✅ **50+ perguntas** no quiz database
- ✅ **Instruções personalizadas** (6 KB de prompts)
- ✅ **Quiz interativo** (pergunta → resposta → correção)

### Interações Testadas
- ✅ Quiz completo com feedback detalhado
- ✅ Plano de estudos personalizado
- ✅ Recomendação de recursos filtrados
- ✅ Explicações de conceitos complexos
- ✅ Suporte motivacional e didático

### Qualidade
- ✅ Respostas em português brasileiro
- ✅ Tom educacional e encorajador
- ✅ Explicações didáticas com analogias
- ✅ Feedback construtivo
- ✅ Correções detalhadas com explicações

---

## 🔗 Links e Referências

### Documentação Oficial Microsoft
- [Certificação AZ-900](https://learn.microsoft.com/pt-br/certifications/azure-fundamentals/)
- [Microsoft Learn - Roteiro AZ-900](https://learn.microsoft.com/pt-br/training/paths/az-900-describe-cloud-concepts/)
- [Guia de Estudos AZ-900](https://learn.microsoft.com/pt-br/certifications/resources/study-guides/az-900)
- [Documentação Azure](https://learn.microsoft.com/pt-br/azure/)

### Azure AI Foundry
- [Azure AI Foundry Portal](https://ai.azure.com/)
- [Documentação Azure AI Foundry](https://learn.microsoft.com/en-us/azure/ai-foundry/what-is-azure-ai-foundry)
- [Azure AI Agent Service](https://learn.microsoft.com/en-us/azure/ai-foundry/agents/overview)

### Challenge
- [Repositório Azure Frontier Girls](https://github.com/AZFRONTIERGIRLS/AzureFrontierGirls-AI-Challenge)

---

## 👩‍💻 Sobre a Desenvolvedora

**Projeto desenvolvido por:** Gabrielly Mendes
**Challenge:** Azure Frontier Girls - 2025  

---

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais como parte do Azure Frontier Girls Challenge.

---

<div align="center">

**Desenvolvido com 💙 para o Azure Frontier Girls Challenge**

[![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)](https://azure.microsoft.com)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![AI](https://img.shields.io/badge/AI-Foundry-brightgreen?style=for-the-badge)](https://ai.azure.com)

</div>

