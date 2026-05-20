# Memorandum de Estrutura de Negócio: Plataforma de Tokenização de Ativos Imobiliários de Alto Valor

**Data:** 20 de Maio de 2026  
**Assunto:** Proposta de Modelo de Negócio e Fluxo Operacional para Tokenização de Terrenos de Luxo  
**Status:** Documento de Trabalho / Solicitação de Análise Jurídica  

---

## 1. Visão Geral do Projeto
O objetivo é a criação de uma startup de tecnologia financeira focada na tokenização de ativos imobiliários de altíssimo valor, especificamente terrenos destinados ao desenvolvimento de empreendimentos de luxo (resorts, pousadas e condomínios).

A tese central é a **democratização do acesso a ativos de alta valorização**, permitindo que investidores com menor capacidade de aporte participem da valorização de terrenos cujo ticket de entrada tradicional seria de dezenes ou centenas de milhões de reais.

## 2. Modelo de Operação Proposto (Tese de Negócio)

Para mitigar riscos regulatórios iniciais e evitar a necessidade imediata de licença como Instituição Financeira ou PSAV (Prestadora de Serviços de Ativos Virtuais) com exigências de capital social elevadas, propõe-se o seguinte modelo:

### 2.1. Estrutura de Lastro (Segregação Patrimonial)
A startup não deteria a propriedade direta dos terrenos. A proposta é a utilização de um veículo segregado:
*   **Veículo:** Criação de uma SPE (Sociedade de Propósito Específico) ou FII (Fundo de Investimento Imobiliário) para cada ativo.
*   **Propriedade:** A escritura do terreno é registrada em nome do veículo (SPE/Fundo).
*   **Tokenização:** O que é tokenizado são as **cotas/participações** do veículo, e não o imóvel em si.

### 2.2. Papéis e Responsabilidades
*   **Sua Startup:** Atuaria como a camada de tecnologia, gestão do portal, onboarding de investidores (KYC/AML) e interface de governança.
*   **Parceiro Regulador (DTVM/Escriturador):** Atuaria como o custodiante legal, validando que a emissão de tokens em blockchain corresponde rigorosamente às cotas existentes no veículo legal.

## 3. Fluxos Operacionais Previstos

### 3.1. Fluxo de Capital (Investimento)
Para garantir a transparência e evitar a confusão patrimonial:
`Investidor` $\rightarrow$ `Gateway de Pagamento / Conta Escrow` $\rightarrow$ `Conta da SPE/Fundo` $\rightarrow$ `Aquisição do Ativo`.
A startup remuneraria sua operação via taxas de estruturação e gestão, sem transitar o capital principal do ativo por suas próprias contas operacionais.

### 3.2. Governança e Tomada de Decisão
Propõe-se um modelo híbrido:
*   **Gestão Especialista:** A startup (ou parceiro) define a estratégia técnica (estudos de viabilidade, projetos, negociações com incorporadoras).
*   **Voto dos Tokenholders:** Decisões críticas (ex: aprovação de venda do ativo para uma incorporadora) seriam submetidas a votação dos detentores de tokens via blockchain.

### 3.3. Estratégia de Liquidez
Para enfrentar a natureza ilíquida do imobiliário, propõe-se:
1.  **Mercado Secundário Interno:** Negociação de tokens entre usuários da plataforma.
2.  **Janelas de Liquidez:** Possibilidade de recompra parcial de tokens em datas pré-definidas.
3.  **Evento de Saída (Exit):** Liquidação total dos tokens após a venda do terreno para o desenvolvedor final.

---

## 4. Seção de Dúvidas e Refinamento (Para Análise Jurídica)

*Este documento apresenta a visão de negócio e operacional. As seguintes questões devem ser analisadas e respondidas pelo corpo jurídico para viabilizar a operação:*

### A. Enquadramento Regulatório (CVM e BC)
*   Os tokens representativos de cotas de SPE ou FII serão classificados como **Valores Mobiliários**? 
*   Caso positivo, qual a melhor norma de oferta para o MVP? (Ex: Crowdfunding de Investimento, Oferta com Esforços Restritos ou Registro Automático).
*   A operação da plataforma como interface tecnológica, sem custódia direta dos ativos, isenta a startup da necessidade de licença de PSAV junto ao Banco Central?

### B. Natureza do Lastro e Segurança Jurídica
*   A tokenização de cotas de SPE é juridicamente blindada em caso de falência da plataforma tecnológica?
*   Como formalizar a "conversão" do registro na escritura/livro de atas da SPE para o registro na blockchain de forma que seja aceita por tribunais e cartórios brasileiros?

### C. Tributação
*   Qual a incidência tributária sobre a negociação de tokens no mercado secundário (Ganho de Capital)?
*   Como deve ser estruturada a distribuição de lucros da SPE para os tokenholders para otimizar a carga tributária?

### D. KYC e Prevenção à Lavagem de Dinheiro (AML)
*   Quais os requisitos mínimos de KYC para investidores de varejo vs. investidores qualificados neste modelo de tokenização imobiliária?

---

## 5. Considerações Finais
O objetivo deste memorandum é fornecer a base lógica do negócio para que o jurídico possa desenhar a "armadura" legal necessária, sugerindo alterações nos fluxos acima para garantir a conformidade total com a legislação brasileira vigente.
