# PyTorch Transformers — Repositório de Pesquisa e Desenvolvimento

## 📋 Sumário Executivo

Este repositório contém implementações avançadas e tutoriais abrangentes para **Redes Neurais Transformers** utilizando PyTorch. O projeto concentra-se em aplicações práticas de inteligência artificial, incluindo tradução automática e Deep Learning com arquiteturas transformer, fundamentado no artigo seminal *"Attention is All You Need"* (Vaswani et al., 2017).

---

## 📚 Estrutura do Repositório

### 1. **tr.ipynb** — Transformer para Tradução Automática (Inglês → Francês)
**Objetivo**: Implementação da arquitetura Transformer original (Encoder-Decoder) para tarefas de tradução automática.

**Componentes Principais**:
- **Módulo Encoder**: Processa entrada em língua de origem (Inglês) e gera representações contextuais
- **Módulo Decoder**: Gera saída em língua alvo (Francês) utilizando cross-attention sobre representações do encoder
- **Self-Attention Multi-Head**: Permite que o modelo foque em diferentes partes da entrada simultaneamente
- **Redes Feed-Forward**: Transformações posição-wise dentro da arquitetura
- **Codificações Posicionais**: Codifica informações de posição sequencial, essencial pois transformers carecem de percepção inerente de sequência

**Aplicações**:
- Tarefas de tradução sequência-para-sequência
- Sistemas de tradução automática (Machine Translation)
- Tarefas encoder-decoder (resumo, geração de legendas, etc.)

---

### 2. **transformers_learning (1) (1).ipynb** — Redes Neurais Transformers: Deep Learning com PyTorch
**Objetivo**: Exploração abrangente de arquiteturas Transformer em aprendizado profundo utilizando PyTorch.

**Tópicos Cobertos**:
- Fundamentos de arquitetura Transformer
- Mecanismos de atenção e self-attention
- Detalhes de implementação em PyTorch
- Modelos pré-treinados e transfer learning
- Fine-tuning e avaliação de modelos
- Aplicações práticas e casos de uso

**Foco Técnico**:
- Padrões de implementação PyTorch
- Design de arquitetura de modelos
- Estratégias de otimização de treinamento
- Análise de métricas e performance

---

## 🛠️ Stack Técnico

| Componente | Versão |
|-----------|---------|
| **Python** | 3.8+ |
| **PyTorch** | Última versão estável |
| **Transformers** | Biblioteca Hugging Face |
| **Datasets** | Biblioteca Hugging Face |
| **SacreBLEU** | Métricas de tradução |
| **SentencePiece** | Tokenização |
| **Polars** | Manipulação de dados (opcional) |

---

## 📦 Dependências

Instale os pacotes requeridos:

```bash
pip install transformers datasets sacrebleu sentencepiece polars
```

**Detalhes dos Pacotes**:
- `transformers`: Modelos pré-treinados e tokenizadores da Hugging Face
- `datasets`: Datasets padrão para treinamento e avaliação
- `sacrebleu`: Métricas automáticas de avaliação para tradução automática (BLEU)
- `sentencepiece`: Biblioteca de tokenização com suporte a unidades de subpalavra
- `polars`: Biblioteca de dataframe de alto desempenho para processamento de dados

---

## 🚀 Início Rápido

### Para o Notebook de Tradução Automática:
```python
# Carregar tradutor pré-treinado ou treinar modelo customizado
# Codificar texto em Inglês → Gerar tradução em Francês
# Avaliar utilizando scores BLEU
```

### Para o Notebook de Aprendizado Transformer:
```python
# Carregar modelo transformer
# Configurar parâmetros da arquitetura
# Treinar em tarefas downstream
# Avaliar performance
```

---

## 🔑 Conceitos Fundamentais

### Arquitetura Transformer
O Transformer é uma arquitetura de aprendizado profundo baseada inteiramente em **mecanismos de atenção**, eliminando a necessidade de recorrência e convolução:

**Estrutura Encoder-Decoder**:
- **Encoder**: Camadas empilhadas de attention multi-head e feed-forward processando sequências de entrada
- **Decoder**: Pilhas similares com attention cruzada adicional sobre saídas do encoder
- **Attention is All You Need**: Toda modelagem é realizada através de mecanismos de atenção

**Componentes Principais**:
1. **Self-Attention Multi-Head**: Cabeças de atenção paralelas capturam diferentes relacionamentos
2. **Codificações Posicionais**: Funções seno/cosseno codificam informação de posição absoluta
3. **Redes Feed-Forward**: Redes totalmente conectadas com ativação ReLU
4. **Layer Normalization & Residual Connections**: Melhorias de estabilidade de treinamento
5. **Masking & Dropout**: Técnicas de regularização para robustez

### Aplicações
- **Tradução Automática**: Inglês → Francês e outros pares de idiomas
- **Compreensão de Linguagem Natural**: Reconhecimento de Entidades Nomeadas, Classificação
- **Geração de Linguagem**: Sumarização de texto, Geração de legendas
- **Transfer Cruzado de Idiomas**: Transferência de conhecimento entre idiomas

---

## 📊 Visão Geral do Conteúdo dos Notebooks

### Notebook 1: Tradução Automática (`tr.ipynb`)
- **Células**: 47 células de código e markdown abrangentes
- **Cobertura**:
  - Configuração do ambiente e dependências
  - Implementação de encoder-decoder transformer
  - Mecanismos de atenção e codificação posicional
  - Pipeline de treinamento e otimização
  - Inferência e geração de tradução
  - Avaliação com score BLEU
  - Visualização de pesos de atenção

### Notebook 2: Aprendizado Transformers (`transformers_learning (1) (1).ipynb`)
- **Células**: 49 células de código e markdown abrangentes
- **Cobertura**:
  - Fundamentos de arquitetura Transformer
  - Detalhes do mecanismo de self-attention
  - Implementação em PyTorch do zero
  - Fine-tuning de modelo pré-treinado
  - Variantes de arquitetura transformer
  - Benchmarking de performance
  - Aplicações práticas

---

## 📖 Caminho de Aprendizado

### Iniciante
1. Ler visão geral da arquitetura (Seções 0-1)
2. Compreender mecanismos de atenção
3. Explorar modelos pré-treinados da Hugging Face

### Intermediário
4. Estudar detalhes de implementação encoder-decoder
5. Implementar loops de treinamento customizados
6. Fine-tuning em tarefas específicas

### Avançado
7. Explorar técnicas de otimização
8. Analisar padrões de atenção e interpretabilidade
9. Implementar modelos para uso em produção

---

## 🎯 Casos de Uso

| Caso de Uso | Notebook | Status |
|----------|----------|--------|
| Tradução Automática | `tr.ipynb` | ✅ Implementado |
| Classificação de Sequências | `transformers_learning` | ✅ Implementado |
| Geração de Texto | `transformers_learning` | ✅ Implementado |
| Fine-tuning de Modelos Pré-treinados | Ambos | ✅ Implementado |

---

## 📈 Métricas de Performance

Os notebooks utilizam métricas de avaliação padrão da indústria:

- **BLEU Score**: Para avaliação de qualidade de tradução
- **Accuracy**: Para tarefas de classificação
- **Loss Functions**: Cross-entropy para tarefas NLP
- **Tempo de Inferência**: Medições de eficiência do modelo

---

## 🔗 Referências

1. Vaswani, A., Shazeer, N., Parmar, N., et al. (2017). *"Attention is All You Need"*
   - Paper original: https://arxiv.org/abs/1706.03762

2. Documentação Transformers — Hugging Face
   - https://huggingface.co/transformers/

3. Documentação Oficial PyTorch
   - https://pytorch.org/docs/stable/

4. Documentação BLEU Score
   - https://github.com/mjPost/sacrebleu

---

## 📝 Notas Importantes

- Todos os notebooks foram desenvolvidos para fins educacionais e de pesquisa
- Modelos pré-treinados são baixados do Hugging Face Model Hub
- Aceleração GPU recomendada para treinamento de modelos maiores
- Tokenização utiliza SentencePiece para tratamento de unidades de subpalavra
- Compatível com ambientes cloud (Google Colab, AWS SageMaker)

---

## 🤝 Contribuições

Este repositório é um recurso educacional. Modificações e extensões para fins educacionais são bem-vindas.

---

## 📄 Licença

Uso Educacional Exclusivamente

---

## 📋 Requisitos do Sistema

- **RAM Mínima**: 8 GB (16 GB recomendado)
- **GPU**: NVIDIA com CUDA 11.0+ (opcional, mas recomendado)
- **Espaço em Disco**: 10 GB para modelos pré-treinados
- **SO**: Windows, macOS ou Linux
- **Jupyter Notebook** ou **VS Code com extensão Jupyter**

---

## 🔧 Configuração Inicial

1. Clone o repositório:
```bash
git clone https://github.com/eliswilliam/pytorch.git
cd pytorch
```

2. Crie um ambiente virtual:
```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
# ou
venv\Scripts\activate  # Windows
```

3. Instale as dependências:
```bash
pip install -r requirements.txt
```

4. Inicie o Jupyter:
```bash
jupyter notebook
```

---

## 📧 Suporte

Para dúvidas ou esclarecimentos sobre os notebooks, consulte a documentação integrada e comentários dentro de cada célula dos notebooks.

---

## ✅ Checklist de Implementação

- ✅ Arquitetura Encoder-Decoder Transformer
- ✅ Mecanismos de Multi-Head Attention
- ✅ Codificações Posicionais
- ✅ Pipeline de Treinamento Completo
- ✅ Avaliação com BLEU Score
- ✅ Modelos Pré-treinados
- ✅ Fine-tuning para Tarefas Específicas
- ✅ Visualizações de Atenção
- ✅ Exemplos de Inferência
- ✅ Documentação Completa

---

**Última Atualização**: Maio de 2026  
**Versão**: 1.0  
**Status**: Recurso Ativo de Pesquisa e Desenvolvimento  
**Linguagem**: Python 3.8+  
**Frameworks**: PyTorch, Hugging Face Transformers
