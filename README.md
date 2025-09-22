# Repositório - Fraudes Corporativas no Brasil: Atuação da CVM no Enforcement do Arcabouço Regulatório-Legal dos Mercados de Capital 

## Descrição

Este repositório contém os dados, códigos e documentos relacionados ao projeto de iniciação científica desenvolvido entre setembro de 2024 e outubro de 2025 na FEA/USP. O projeto teve como objetivo investigar fraudes corporativas no Brasil por meio da análise sistemática dos Processos Administrativos Sancionadores (PAS) conduzidos pela Comissão de Valores Mobiliários (CVM), focalizando especificamente casos de expropriação de acionistas minoritários por controladores e seus subordinados.
Devido ao volume extenso de processos (mais de 2.100), o estudo adotou técnicas de Processamento de Linguagem Natural (PLN) para classificação automática dos documentos, representando a primeira tentativa de sistematização metodológica para aplicação de PLN a documentos regulatórios da CVM.

## Estrutura do Repositório

```
├── data/
│   ├── raw/           # Dados brutos, sem processamento
│   ├── interim/       # Dados parcialmente processados
│   └── processed/     # Dados finais, prontos para análise
├── notebooks/         # Jupyter notebooks com códigos e análises
└── docs/              # Relatório parcial e final, respectivas apresentações, codebooks e manual e anotação
```

## Dados

### `/data/raw/`
Contém os dados originais coletados/obtidos para a pesquisa. Isso inclui os PDFs dos Extratos das Sessões de Julgamento (ESJs) e Pareceres do Comitê de Termo de Compromisso (CTC).

### `/data/interim/`
Dados em estágio intermediário de processamento. Inclui os textos extraídos dos PDFs, para PCTCs e ESJs separadamente, além de produtos complementares que foram extraídos (ex.: nome dos acusados, data do julgamento, ementa).

### `/data/processed/`
Dados finais utilizados nas análises: o corpus, a amostra anotada e os produtos complementares.

## Notebooks

A pasta `/notebooks/` contém os códigos desenvolvidos durante a pesquisa, organizados de forma sequencial:

- **01_download_pareceres_ctc**: Download automatizado dos PDFs dos Pareceres do CTC do site da CVM
- **02_extracao_textos_pdfs**: Extração dos textos dos pdfs e armazenamento das informações em uma base de dados
- **03_extracao_relatorios**: A partir dos textos obtidos, extração dos relatórios usando expressões regulares
- **04_uniao_corpus**: União das bases de dados obtidas (relatórios dos Paraceres do CTC e dos ESJs) em um corpus
- **10_produtos_complementares**: Extração de outras variáveis de interesse (ex.: nome dos acusados, data do julgamento, ementa).

## Documentação

- Relatório parcial e a apresentação usada
- Relatório final e a apresentação usada
- Codebook e manual de anotação desenvolvidos

## Principais Resultados

### Infraestrutura de Dados

- 2.094 processos identificados (2000-2023)
- 1.993 relatórios extraídos com sucesso
- 8.422 acusados identificados (limite inferior)
- 100 processos anotados manualmente

### Corpus Anotado

- Variáveis classificadas: relevância, punição, tipo de punição
- Manual de anotação com critérios linguísticos objetivos
- Base para treinamento de modelos de PLN

### Contribuições Metodológicas

- Primeiro pipeline sistemático para análise de documentos regulatórios da CVM
- Corpus replicável para pesquisas futuras
- Ferramentas de PLN adaptadas ao contexto jurídico-administrativo brasileiro

## 👥 Autor

**Tomás Peres Ribeiro**
- Estudante de Economia - FEA/USP
- Email: tomas.ribeiro@usp.br

**Orientador: Dante Mendes Aldrighi**
- Professor do Departamento de Economia da FEA/USP

---

**Última atualização**: 22/09/2025
