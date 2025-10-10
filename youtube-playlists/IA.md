# Guia Completo de Fundamentos em Inteligência Artificial

## Parte 1: Fundamentos Teóricos e Matemáticos

### 1.1 Base Matemática Essencial
- **Álgebra Linear**: Vetores, matrizes, tensores, multiplicação de matrizes, transformações lineares, autovalores e autovetores
- **Cálculo**: Derivadas (simples e parciais), gradientes, regra da cadeia, otimização, funções de custo
- **Estatística e Probabilidade**: Média, mediana, desvio padrão, distribuições de probabilidade, teorema de Bayes, testes de hipóteses, inferência estatística
- **Otimização**: Gradiente descendente, Adam, SGD, L-BFGS, conceitos de convexidade e mínimos locais/globais

### 1.2 Fundamentos Teóricos de IA
- Busca e otimização
- Representação de conhecimento
- Aprendizado por reforço (básico)
- Viés e ética em IA

## Parte 2: Machine Learning e Deep Learning

### 2.1 Machine Learning Clássico
- **Tipos de Aprendizado**:
  - **Aprendizado Supervisionado**: Modelos que aprendem a partir de dados rotulados
    - **Regressão**: Prever valores contínuos (Regressão Linear)
    - **Classificação**: Prever categorias (Regressão Logística, Árvores de Decisão, SVM, Random Forests)
  - **Aprendizado Não Supervisionado**: Encontrar padrões em dados não rotulados
    - **Clusterização**: Agrupar dados similares (K-Means)
    - **Redução de Dimensionalidade**: Simplificar dados (PCA)

- **Processo e Avaliação**:
  - Pré-processamento de dados
  - Engenharia de Features (Feature Engineering)
  - Overfitting, underfitting e regularização
  - Validação cruzada
  - Métricas de avaliação: acurácia, precisão, recall, F1-score, AUC, MSE

### 2.2 Deep Learning e Redes Neurais
- **Arquitetura Fundamental**:
  - Neurônios (Nós), Camadas (Input, Hidden, Output)
  - Funções de Ativação (ReLU, Sigmoid)
  - Backpropagation
  - Técnicas de treinamento: Batch Normalization, Dropout, Learning Rate Scheduling

- **Arquiteturas Especializadas**:
  - **CNNs (Redes Neurais Convolucionais)**: Visão computacional
  - **RNNs/LSTMs/GRUs**: Dados sequenciais
  - **Transformers**: Linguagem natural e multimodalidade
  - Mecanismo de Attention e Self-Attention

### 2.3 Processamento de Linguagem Natural (NLP)
- Tokenização e embeddings (Word2Vec, GloVe, BERT)
- Arquitetura Transformer
- Modelos pré-treinados (BERT, GPT)
- Fine-tuning e transfer learning

### 2.4 Aprendizado por Reforço
- Agente, ambiente, política, recompensa
- Q-Learning, SARSA
- Deep Q-Network (DQN)
- Política Proximal (PPO) - usado em IA moderna

## Parte 3: Ferramentas e Implementação Prática

### 3.1 Linguagens e Frameworks
- **Python**: Linguagem dominante em IA
- **Bibliotecas Fundamentais**:
  - NumPy: Computação numérica
  - Pandas: Manipulação e análise de dados
  - Scikit-learn: Algoritmos clássicos de ML
  - TensorFlow e PyTorch: Frameworks de Deep Learning
- **Ferramentas de Desenvolvimento**:
  - Jupyter Notebooks
  - Git para versionamento
  - Bibliotecas de visualização (Matplotlib, Seaborn)

### 3.2 Engenharia de Dados para IA
- Limpeza e pré-processamento de dados
- Feature engineering e seleção
- Lidar com desbalanceamento
- Data augmentation
- Feature stores e pipelines de dados
- Versionamento de dados e modelos (DVC, MLflow)

## Parte 4: IA Generativa e LLMs - Conceitos Práticos

### 4.1 Fundamentos de Modelos de Linguagem (LLMs)
- **Tokens e Tokenização**: Blocos de construção do texto, contagem e custos
- **Contexto e Janela de Contexto**: Memória do modelo (ex: 8K-200K tokens), estratégias de gerenciamento
- **Funcionamento dos LLMs**:
  - Probabilidade de próximo token
  - Sampling e temperatura
  - Top-k e Top-p (nucleus sampling)
  - Inference vs. Training

### 4.2 Engenharia de Prompts
- **Técnicas Fundamentais**:
  - Zero-Shot Prompting: Perguntas diretas sem exemplos
  - Few-Shot Prompting: Fornecer exemplos no prompt
  - Chain-of-Thought: Raciocínio passo a passo
- **Estratégias Avançadas**:
  - Personas e papéis
  - Instruções claras com contexto suficiente
  - Regras e restrições explícitas
  - Especificação de formato de saída
  - Prompt modular e templates reutilizáveis

### 4.3 RAG (Retrieval Augmented Generation)
- Embeddings e similaridade semântica (cosine similarity)
- Bancos de dados vetoriais (FAISS, Pinecone, Weaviate, Chroma)
- Pipeline RAG: Chunking, busca semântica, augmentação de contexto
- Memória de longo prazo vs. contexto imediato

### 4.4 Integração e Agentes
- **APIs de LLMs**: Parâmetros (temperature, max_tokens), streaming, function calling
- **MCP (Model Context Protocol)**: Protocolo para conectar LLMs a ferramentas externas
- **Agentes de IA**: Sistemas que planejam, decidem e executam tarefas autonomamente
- **Ferramentas (Tools/Functions)**: Como LLMs chamam funções externas

## Parte 5: Produção e MLOps

### 5.1 Deployment e Monitoramento
- Deploy de modelos (FastAPI, Flask, Streamlit)
- Containerização (Docker)
- APIs e microserviços
- Monitoramento de desempenho e data drift

### 5.2 MLOps
- Versionamento de modelos
- Pipelines de treinamento automatizados
- CI/CD para IA
- Escalabilidade (Kubernetes, AWS, GCP, Azure)

### 5.3 Fine-tuning e Otimização
- Quando usar fine-tuning vs. prompt engineering
- LoRA e técnicas eficientes de adaptação
- Otimização de inferência
- Alinhamento (RLHF)

## Parte 6: Aspectos Práticos e Éticos

### 6.1 Limites e Boas Práticas
- **Alucinações (Hallucinations)**: Quando modelos inventam informações
- **Context Overflow**: Exceder janela de tokens
- **Confidencialidade de Dados**: Proteção de informações sensíveis
- **Testes e Validação**: IA como auxiliar, não substituta do julgamento humano

### 6.2 Ética e Responsabilidade
- Viés algorítmico e justiça de modelos
- Explicabilidade (LIME, SHAP)
- Privacidade e segurança de dados
- Regulações (GDPR, LGPD, IA Act)

### 6.3 Mentalidade e Produtividade
- Pensamento em etapas ("divide e conquista")
- IA como copiloto, não oráculo
- Desenvolvimento iterativo de prompts
- Construção de conhecimento incremental
- Automação de workflows com IA

## Parte 7: Aprendizado Contínuo

### 7.1 Manutenção de Conhecimento
- Leitura de papers (arXiv, Google Scholar)
- Conferências: NeurIPS, ICML, ICLR, CVPR
- Implementação de modelos do zero
- Compartilhamento de projetos (GitHub, blogs)

### 7.2 Ordem Sugerida de Estudo
1. **Fase 1 (1-2 meses)**: Matemática fundamental e Python
2. **Fase 2 (2-3 meses)**: Machine Learning clássico
3. **Fase 3 (3-4 meses)**: Deep Learning e NLP
4. **Fase 4 (2 meses)**: LLMs e engenharia de prompts
5. **Fase 5 (2 meses)**: MLOps e produção
6. **Fase 6 (contínuo)**: Projetos práticos e especialização

### 7.3 Foco Imediato para Produtividade
- Engenharia de prompts
- Gerenciamento de tokens e contexto
- RAG e bancos vetoriais
- APIs de LLMs e MCP
- Integração com ferramentas existentes