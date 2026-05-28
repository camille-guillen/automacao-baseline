# Automação de Criação de Baselines ATC

## Visão Geral

A automação de criação de baselines ATC foi desenvolvida com o objetivo de reduzir o esforço operacional e o tempo gasto no tratamento manual de objetos identificados pelo ATC (ABAP Test Cockpit) em projetos de conversão SAP S/4HANA.

A solução foi inicialmente desenvolvida pela Débora e surgiu devido ao alto volume de objetos encontrados nos projetos de conversão, onde alguns clientes possuem entre 1.500 até mais de 50.000 objetos ATC.

Grande parte desses objetos:
- São obsoletos;
- Não possuem impacto real no negócio;
- Não são tratáveis manualmente;
- Geram alto esforço operacional.

A automação permite analisar, filtrar e criar baselines automaticamente no SAP utilizando regras definidas via Excel.

---

# Problema Atual

## Processo Manual (AS IS)

Atualmente a criação de baselines é feita manualmente através da transação ATC no SAP.

### Fluxo atual:
1. Executar o ATC;
2. Filtrar os objetos;
3. Analisar os resultados;
4. Criar os baselines manualmente;
5. Repetir o processo para milhares de objetos.

### Problemas encontrados:
- Alto esforço operacional;
- Longo tempo de execução;
- Baixa escalabilidade;
- Risco operacional;
- Falta de padronização;
- Dificuldade em tratar grandes volumes.

---

# Solução Desenvolvida

A solução automatiza completamente o processo de criação de baselines utilizando:
- Leitura do último run do ATC;
- Controle de filtros via Excel;
- Criação automática dos baselines no SAP.

A implementação foi construída utilizando as mesmas classes standard SAP identificadas através de debug técnico do processo nativo da SAP.

## Benefícios da abordagem
- Redução de risco técnico;
- Compatibilidade com S/4HANA;
- Maior segurança;
- Menor impacto em upgrades futuros;
- Reutilização do comportamento standard SAP.

---

# Funcionamento da Automação

## Fluxo do Programa

### 1. Leitura do Último Run do ATC
O programa identifica automaticamente o último resultado executado do ATC no ambiente SAP.

---

### 2. Leitura da Planilha Excel
O Excel funciona como base de controle da automação.

### Informações controladas no Excel:
- Objetos baseline;
- Tipo do objeto;
- Filtros;
- Regras;
- Notas;
- Declarações;
- Critérios de tratamento.

---

### 3. Criação Automática dos Baselines
Com base nas regras cadastradas no Excel, o programa cria automaticamente os baselines diretamente no ambiente SAP.

Não é necessário criar os objetos manualmente um a um.

---

# Estrutura de Controle

## Controle via Excel

Os filtros são controlados diretamente pela planilha.

### Possibilidades:
- Separação por tipo de objeto;
- Controle de regras;
- Definição de objetos baseline;
- Controle de notas;
- Criação de grupos de baseline;
- Identificação de objetos tratáveis.

---

# Reports Gerados

A solução também possui reports para:
- Retorno de dados;
- Validação dos filtros;
- Controle dos grupos de baseline;
- Auditoria dos objetos processados.

---

# Resultados Obtidos

A automação já foi validada em clientes como:
- Amaggi;
- Cornelio;
- CSN.

## Benefícios alcançados
- Redução significativa dos objetos tratados manualmente;
- Redução de custo operacional;
- Redução de esforço técnico;
- Redução de tempo;
- Padronização do processo;
- Maior escalabilidade;
- Melhor qualidade nas entregas.

---

# Integração com Portal MIGNOW

Já existe uma melhoria de execução ATC desenvolvida no Portal MIGNOW pelo Pablo e Otávio.

Parte das funcionalidades necessárias para integração da solução já estão disponíveis.

## Funcionalidades existentes no Portal
- Tela Parameters;
- Cadastro ATC Result Execution;
- Estrutura de tabelas;
- Controle de baselines na aba "Control".

---

# Objetivo da Evolução

O objetivo da nova demanda é integrar a automação da Débora diretamente ao Portal MIGNOW.

## Fluxo esperado no Portal
1. Leitura automática do último run do ATC;
2. Consumo dos filtros definidos no Excel;
3. Criação automática dos baselines;
4. Atualização automática no ambiente SAP;
5. Centralização do processo no Portal.

A intenção é permitir que toda execução seja feita através do Portal, eliminando atividades manuais diretamente na transação ATC.

---

# Processo Atual vs Novo Processo

## Antes

### Manual
- Criação manual dos baselines;
- Filtragem manual;
- Alto esforço operacional;
- Baixa escalabilidade.

### Automático
- Leitura automática do Excel;
- Criação automática no SAP;
- Execução padronizada;
- Escalabilidade.

---

# Próximos Passos

Foi solicitado que o Cabrera:
- Avalie tecnicamente a solução;
- Analise a arquitetura atual;
- Estruture a demanda junto ao time de Discovery;
- Levante os requisitos para desenvolvimento no Portal MIGNOW.

---

# Referência

## Documento Relacionado
- Melhorias na execução do ATC - Clean Core

Link:
https://mignow.atlassian.net/wiki/spaces/PM/pages/1124433933/Melhorias+na+execu+o+do+ATC+-+Clean+Core
