# Prêmio Turim de Investimentos 2025 - Equity & Wealth Management Case

Este repositório contém os arquivos e a modelagem desenvolvida para o **Prêmio Turim de Investimentos 2025**, organizado pela Turim MFO. O projeto consiste em uma solução completa de gestão patrimonial, dividida em duas frentes: uma tese de investimento em Equity (Stock Picking) e uma estratégia de Alocação de Ativos (Asset Allocation) para um perfil Ultra-High-Net-Worth (UHNWI).

* **`Modelagem_Financeira.xlsx`**: O modelo completo em Excel, contendo a otimização de portfólio, simulação de fluxo de caixa de 60 anos, cálculo de impostos e rebalanceamento dinâmico.
* **`Apresentacao_Case.pdf`**: O deck de apresentação defendendo a tese e a estratégia de alocação.

## Parte 1: Equity Research - Abbott (ABT)

A tese de investimento foi fundamentada no conceito da **Longevity Economy** (Economia da Longevidade). A escolha da **Abbott Laboratories (ABT)** baseou-se em sua capacidade de capturar valor no aumento da expectativa de vida saudável (Healthspan).

* **Tese:** Crescimento Orgânico Sustentável focado em *Medical Devices* (ex: FreeStyle Libre) e Nutrição.
* **Drivers:** Liderança em monitoramento contínuo de glicose, portfólio diversificado e histórico de "Dividend Aristocrat".
* **Projeção:** Estimativa de crescimento de lucros >8% a.a., alinhada com a demanda inelástica do envelhecimento populacional.

## Parte 2: Asset Allocation & Wealth Management

O desafio consistia em gerir um patrimônio inicial de **US$ 20 milhões** ao longo de três fases de vida de um cliente (Jovem Profissional, Família em Crescimento, Aposentadoria), com o objetivo de cobrir gastos anuais crescentes e garantir uma herança real líquida (Inflação + 1%).

### Metodologia e Modelagem

Foi desenvolvido um modelo quantitativo robusto no Excel para determinar a alocação ótima entre **Renda Fixa**, **Renda Variável** e **Ilíquidos (Private Equity/Venture Capital)**.

#### Destaques Técnicos do Modelo:

1.  **Otimização de Portfólio (MPT Ajustada):**
    * Utilização da *Modern Portfolio Theory* (Markowitz) adaptada com restrições de liquidez.
    * Interpolação linear entre carteiras de Mínima Variância e Máximo Sharpe para definir o perfil de risco de cada fase da vida.

2.  **Estratégia "Liquidity-Aware" (Sensível à Liquidez):**
    * Desenvolvimento de um algoritmo de rebalanceamento que respeita os *lock-ups* dos ativos ilíquidos (ciclos de 7 anos).
    * Implementação de uma função de decaimento para a exposição em Renda Variável caso a parcela de Ilíquidos ultrapasse limites de segurança, protegendo o fluxo de caixa de curto prazo.

3.  **Simulação Fiscal e Sucessória:**
    * Cálculo detalhado de impostos sobre ganhos de capital (15%) no momento da geração de liquidez (venda para rebalanceamento ou distribuição de ilíquidos).
    * Projeção do ITCMD (4%) e verificação da meta de herança baseada no poder de compra (Inflação acumulada + ganho real).

4.  **Excel Avançado:**
    * Uso de **Matrizes Dinâmicas (Dynamic Arrays)** (`SEQUENCE`, `VSTACK`, `DROP`) para tornar a linha do tempo flexível.
    * Criação de cenários de *stress test* e visualização da evolução patrimonial líquida de inflação.

* **Ferramentas:** Microsoft Excel (Advanced Modeling, Solver), PowerPoint.
* **Conceitos Financeiros:** Modern Portfolio Theory (MPT), CAGR, Sharpe Ratio, Drawdown, Rebalanceamento de Carteira, Goal-Based Investing.
* **Design Patterns (Lógica):** Estruturação de dados sequencial e lógica condicional aninhada para tratamento de exceções de liquidez.
