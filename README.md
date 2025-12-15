# Mini-Projecto #03 - Logística Express
### 👥 Autores

| Nome Completo | Número de Matrícula | Curso e Instituição |
| :--- | :--- | :--- |
| **Geraldo Abreu Leão Chiquemba** | 20230043 | Engenharia Informática, ISPTEC |
| **Kialenguluka Kialenguluka Tuavile** | 20231633 | Engenharia Informática, ISPTEC |
| **Nvemba Silva** | 20232319 | Engenharia Informática, ISPTEC 
## Descrição
Sistema para maximizar o lucro diário através da seleção ótima de pacotes a transportar num camião com capacidade limitada.

## Estrutura do Projeto
```
.
├── README.md
├── requirements.txt
├── logistica_express.py     # Programa completo com menu (único ficheiro)
├── knapsack_solver.py       # Solução do problema (modular)
├── generate_data.py         # Gerador de dados (modular)
├── analyze_capacity.py      # Análise de diferentes capacidades
├── build_completo.py        # Script para criar executável único
├── dados_entrega.txt        # Ficheiro de entrada (gerado)
└── .gitignore
```

## Como Usar

### Opção 1: Usar o Executável (Recomendado)

**Basta dar duplo clique em `LogisticaExpress.exe`** (na pasta `dist`)!

O executável:
- ✅ Funciona sem precisar instalar Python
- ✅ Funciona sem precisar copiar outros ficheiros
- ✅ Tem menu interativo com todas as funcionalidades
- ✅ Verifica automaticamente se precisa gerar dados na primeira execução

**Como usar:**
1. Abra a pasta `dist`
2. Dê duplo clique em `LogisticaExpress.exe`
3. Se for a primeira vez, o programa oferecerá gerar dados automaticamente
4. Novas opções do menu:
   - 1 = Gerar dados (`dados_entrega.txt`)
   - 2 = Resolver problema (otimizar carga)
   - 3 = Analisar impacto da capacidade
   - 4 = Resumo rápido do ficheiro de dados
   - 5 = Sair

### Opção 2: Usar Python

#### 1. Instalar dependências (apenas para criar executável)
```bash
pip install -r requirements.txt
```
(Nota: Para uso normal, não são necessárias dependências externas)

#### 2. Executar programa completo com menu
```bash
python logistica_express.py
```

#### 3. Ou usar scripts individuais
```bash
# Gerar dados
python generate_data.py

# Resolver problema
python knapsack_solver.py

# Análise de capacidades
python analyze_capacity.py
```

## Criar Executável Único

Para criar um único executável (.exe) completo com menu:

### 1. Instalar PyInstaller
```bash
pip install pyinstaller
```

### 2. Criar executável completo
```bash
python build_completo.py
```
O executável será criado em `dist\LogisticaExpress.exe`

Este executável único inclui:
- Menu interativo
- Gerador de dados
- Solver de otimização
- Todas as funcionalidades combinadas

**Nota:** Não é necessário ter o ficheiro `dados_entrega.txt` previamente, pois pode gerá-lo através do menu do executável.

## Formato do Ficheiro dados_entrega.txt
- Primeira linha: capacidade máxima (em kg)
- Linhas seguintes: um pacote por linha no formato `peso,valor`

## Algoritmo
Utiliza Programação Dinâmica para resolver o problema do Knapsack 0/1, garantindo a solução ótima.

## Autor
Desenvolvido para o Mini-Projecto #03 de Análise de Algoritmos - ISPTEC

