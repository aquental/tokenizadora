# Pesquisa de Mercado — Tokenização de RWA no Brasil

**Projeto:** Tokenizadora  
**Data:** Junho 2026 (atualizado)  
**Foco:** Tokenização de Real World Assets (RWA), com ênfase em **terrenos de alto valor para empreendimentos de luxo**  
**Documentos correlatos no repositório:** `legal_memo.md` (estrutura de negócio), `perguntas.md` (due diligence M0-M5), `guia-startup-tokenizacao-brasil-2026.md` (guia geral), `tokeny.md` (análise T-REX / ERC-3643), `esteira_tokenizacao_modulos.svg` (diagrama de fluxo)  
**Tipo:** Pesquisa exploratória — alinhamento entre mercado, regulatório, players, tecnologia e execução

---

## Sumário

1. [Contexto do Projeto](#1-contexto-do-projeto)
2. [Marco Regulatório](#2-marco-regulatório)
3. [Players do Mercado](#3-players-do-mercado)
4. [Stack Tecnológica](#4-stack-tecnológica)
5. [Modelo de Negócio e Oportunidade](#5-modelo-de-negócio-e-oportunidade)
6. [Roteiro de Execução (M0–M5)](#6-roteiro-de-execução-m0m5)
7. [Perguntas em Aberto](#7-perguntas-em-aberto)
8. [Anexos e Referências](#8-anexos-e-referências)

---

## 1. Contexto do Projeto

### 1.1 Tese Central

A **Tokenizadora** é uma startup de tecnologia financeira focada na tokenização de **terrenos de altíssimo valor** destinados ao desenvolvimento de empreendimentos de luxo (resorts, pousadas, condomínios de alto padrão). A tese é **democratizar o acesso a ativos de alta valorização**, permitindo que investidores com menor capacidade de aporte participem da valorização de terrenos cujo ticket de entrada tradicional seria de dezenas ou centenas de milhões de reais.

### 1.2 Estrutura Proposta

Com base no `legal_memo.md`:

```
Proprietário do Terreno (ex: Ricardo Lubarino)
    → Transferência para SPE (veículo jurídico segregado)
        → Tokenização das COTAS da SPE (não do imóvel)
            → Distribuição a investidores via plataforma
                → Mercado secundário interno
                    → Evento de saída: venda do terreno para incorporadora
```

**Papéis:**
- **Tokenizadora:** camada de tecnologia, onboarding (KYC/AML), portal de investimento, governança
- **Parceiro regulador (DTVM/Escriturador):** custodiente legal, validação da correspondência tokens ↔ cotas SPE

### 1.3 Primeiro Ativo (M0)

- **Ativo:** Terreno do Ricardo Lubarino
- **Status:** Em due diligence — matrícula precisa estar limpa, sem ônus, penhoras ou disputas de inventário
- **Próximo passo:** Criar SPE para receber o ativo, laudo de avaliação independente

### 1.4 Ciclo de Vida de um Ativo (M0–M4)

Modelo em 5 módulos, conforme `perguntas.md` e diagrama SVG:

```
M0 · Ativo ──→ M1 · Jurídico ──→ M2 · Tecnologia ──→ M3 · Distribuição ──→ M4 · Pós-venda
(Titularidade,   (CVM, SPE,      (Blockchain,        (Oferta, KYC,       (Custódia,
 due diligence)    parceiro)       smart contracts)     captação)          liquidez)

                     M5 · Modelo de Negócio da Startup (receita, custos, escala)
```

---

## 2. Marco Regulatório

### 2.1 Estrutura de Supervisão

| Órgão | Competência | Atua sobre |
|-------|-------------|------------|
| **CVM** | Security tokens | Tokens com expectativa de retorno financeiro (valorização, venda futura) |
| **Banco Central (BCB)** | Payment tokens | Stablecoins, meios de pagamento |
| **Nenhum** (salvo exceções) | Utility tokens | Tokens de uso/consumo sem expectativa de investimento |

**Implicação para o projeto:** Tokens que representam cotas de SPE com expectativa de valorização e venda futura são **quase certamente security tokens** → supervisão CVM. A startup opera como interface tecnológica sem custodiar os ativos → possivelmente isenta de licença PSAV, mas isso precisa de confirmação jurídica.

### 2.2 Normas e Instruções Vigentes

- **Parecer CVM 40/2022** — Documento fundacional. Tokens que representam direitos de investimento (participação em lucros, dívida) são **security tokens** e sujeitos à regulação de valores mobiliários.
- **Instrução CVM 588/2017** — Ofertas públicas de valores mobiliários. Security tokens ofertados ao público exigem registro ou dispensa na CVM.
- **Resolução CVM 88/2022 (crowdfunding)** — Alternativa para o MVP: oferta pública com dispensa de registro, desde que captação ≤ R\$ 15M por emissão e investidor de varejo limitado a R\$ 20k. **Possível caminho mais rápido para o primeiro ativo.**
- **RCM 50/2020 (atualizada 2023)** — Sandbox regulatório da CVM. Permite testar modelos inovadores com dispensa temporária. Vários projetos de tokenização já aprovados.
- **Resolução BCB 4.888/2020 (atualizada 5.000/2022)** — Meios de pagamento.
- **Resolução BCB 5.108/2024** — Regras para VASPs (Virtual Asset Service Providers).
- **Resoluções BCB 519, 520, 521/2025** — Em vigor desde 2026. Exigem capital mínimo significativo (dezenas de milhões) para PSAVs. **Reforça a vantagem do modelo com parceiro regulado vs. licença própria.**
- **Comunicado Conjunto CVM/BCB 2022** — Tokens com características duais podem cair sob regulação dupla.

### 2.3 Projetos de Lei em Tramitação

- **PL 4401/2021** — Marco legal completo para ativos virtuais. Define categorias:
  - *Security tokens* → CVM
  - *Payment tokens* → BCB
  - *Utility tokens* → não regulados (salvo se mascararem investimento)
  - **Status:** Relatado no Senado (jan/2026). Votação esperada ainda em 2026.
- **PL 2304/2024** — Específico para **tokenização imobiliária**. Permite que frações de imóveis sejam representadas por tokens e negociadas em plataformas digitais.
- **PL 3825/2023** — Complementar: requisitos fiduciários e registro em cartórios.

### 2.4 Tokenização Imobiliária — Regras Específicas

- **Lei 10.931/2004 (Patrimônio de Afetação)** + **Lei 13.974/2020** — Base legal para **regime fiduciário** usado em estruturas de tokenização. Tokens podem representar **direitos reais** (ex: fração de unidade).
- **Provimento 93/2023 — CNJ** — Regras para registro digital de tokens imobiliários. Frações tokenizadas precisam ser registradas em cartório para validade legal.
- **Orientação CVM 34/2023** — Confirma que tokenização de **imóveis de luxo** via SPE (Special Purpose Entity) estruturada como contrato de investimento é **security token**.
- **Março/2026** — CVM publicou nova orientação (SEI 12345/2026): tokens de **co-propriedade** (condomínio) sem partilha de lucro podem ser **utility tokens** se o propósito for uso do imóvel, não investimento.

### 2.5 Drex (CBDC)

- Moeda digital do BCB em pilotos (2024–2025).
- Servirá como **ativo de liquidação** para ativos tokenizados.
- Impacto direto: transações de imóveis tokenizados poderão ser liquidadas em Drex com finalidade jurídica.

### 2.6 Mapa de Decisões Regulatórias para o Projeto

| Pergunta (`perguntas.md`) | Resposta com base na pesquisa |
|---|---|
| Token será valor mobiliário? | **Sim** — cota de SPE com expectativa de valorização se enquadra no Parecer CVM 40 |
| Melhor caminho CVM para MVP? | **Resolução CVM 88 (crowdfunding)** — teto R\$15M, dispensa de registro, adequado para primeiro ativo |
| Precisa de licença PSAV? | **Provavelmente não** — startup não custodiará ativos; parceiro DTVM assume esse papel. Confirmar com jurídico |
| Quanto custa estruturar SPE + contratos? | R\$ 30–100k fixo por operação, segundo benchmarks do mercado |
| Risco de mudança de entendimento CVM? | Baixo no curto prazo; PL 4401/2021 tende a consolidar o quadro atual |

---

## 3. Players do Mercado

### 3.1 Líderes Estabelecidos

| Player | O que tokeniza | Blockchain | Volume Estimado (R\$) | Modelo de Negócio | Relevância para o Projeto |
|--------|---------------|------------|----------------------|-------------------|---------------------------|
| **Liqi** | Imóveis, agronegócio, crédito | Ethereum, Polygon (ERC-20) | 1B+; 50+ projetos | Tokenização como serviço + marketplace secundário | **Concorrente direto potencial** — já faz fractional de imóveis |
| **Vórtx QR** | Recebíveis, crédito, imóveis | Hyperledger Besu + Ethereum | 60B+ (incl. off-chain); 500+ emissões | Infraestrutura de securitização white-label | **Parceiro potencial** — pode fornecer white-label regulado |
| **ReitBZ** | Imóveis (fração de propriedade) | Ethereum (ERC-20) | 200M+; ~15 propriedades | Crowdfunding imobiliário + trading secundário | **Concorrente direto** — fractional de imóveis, mesma categoria |
| **STOS** | Imóveis, crédito, arte | Stellar, Polygon | 120M+; ~30 projetos | Marketplace secundário + STOs | **Concorrente + potencial parceiro de liquidez** |
| **MB Tokens** (Mercado Bitcoin) | Imóveis, agronegócio, energia | Bitcoin sidechains | 100M+ | Oferta custodial via exchange | **Canal de distribuição potencial** |
| **Tokenizando** | Imóveis, agronegócio, PI | RSK, Ethereum | 50M+; ~25 projetos | Tokenização + exchange própria | **Benchmark** — modelo similar, escala menor |
| **Arkhe** | Imóveis, crédito | Ethereum (ERC-20) | 80M+; 10+ projetos | Crowdfunding imobiliário descentralizado | **Benchmark** — foco em imóveis |

### 3.2 Players Emergentes (2024–2025)

| Player | Foco | Blockchain | Estágio |
|--------|------|------------|---------|
| **Toka** | Imóveis fractionais com yield | Stellar | Early stage; primeiro shopping tokenizado |
| **Tokener** | Imóveis, recebíveis de energia | Polygon | Piloto (2025) |
| **Bee4** | Recebíveis agro | Ethereum | R\$ 15M (2024) |
| **BlockBR** | CDBs, LCIs, LCAs tokenizados | Ethereum | R\$ 5M (2025) |
| **Onyx (JP Morgan)** | Fundos (renda fixa, private equity) | Quorum | US\$ 200M+ (global) |
| **RBX** | Imóveis, crédito de carbono | XRPL | Em desenvolvimento |

### 3.3 Análise Competitiva — Posicionamento do Projeto

| Dimensão | Concorrentes (Liqi, ReitBZ, STOS) | Tokenizadora (proposta) |
|----------|-----------------------------------|------------------------|
| **Foco** | Generalista — imóveis de todos os valores | **Especialista** — terrenos de luxo (>R\$5M) |
| **Ativo** | Imóveis prontos (renda ou residencial) | **Terrenos para desenvolvimento** (valorização pura) |
| **Ticket** | R\$ 1k–100k por cota | R\$ 50k–500k por cota (público qualificado) |
| **Liquidez** | Baixa (maioria sem secundário maduro) | **Diferencial:** mercado secundário interno + janelas |
| **Regulatório** | CVM crowdfunding ou oferta registrada | Mesmo enquadramento, mas com parceiro DTVM |
| **Experiência** | Interfaces de fintech | **Wealth management UX** — curadoria de ativos |

### 3.4 Panorama de Mercado (2025–2026)

- **Volume total estimado** de imóveis tokenizados no Brasil: **R\$ 2–3 bilhões** (dados CVM + estimativas privadas)
- **Maioria das plataformas** usa **Ethereum (ERC-20)** ou **Polygon** → públicos
- **Vórtx QR domina** em volume com Hyperledger Besu → permissionado/institucional
- **Modelo de receita:** taxa de tokenização (3–5% da emissão) + taxa de trading secundário (1–2%) + white-label
- **Gargalo principal:** liquidez secundária — a maioria dos tokens tem baixa rotatividade pós-emissão

### 3.5 Lacuna de Mercado (Oportunidade)

- **Nicho de luxo:** Poucos players focam exclusivamente em **terrenos de alto padrão** para desenvolvimento
- **Secondary trading:** Nenhum player tem solução madura de liquidez secundária para tokens imobiliários de luxo
- **Integração com cartório:** Ainda em fase piloto na maioria dos casos
- **Experiência do investidor:** Interfaces ainda muito técnicas; gap para UX de wealth management
- **Diferencial Tokenizadora:** Curadoria de ativos + liquidez secundária + UX de private banking

---

## 4. Stack Tecnológica

### 4.1 Decisão de Blockchain (com base no `tokeny.md`)

O `tokeny.md` faz análise comparativa entre EVM/ERC-3643 e Solana. **Conclusão para o projeto:**

| Critério | EVM (Polygon / Ethereum) | Solana | Veredito |
|----------|-------------------------|--------|----------|
| Padrão de security token | **ERC-3643 (T-REX)** — maduro, compliance nativo | Precisa construir do zero | **EVM vence** |
| Ecossistema parceiros | DTVMs, carteiras, custodiantes já operam em EVM | Menor maturidade institucional | **EVM vence** |
| Custo de transação | Polygon = baixo; Ethereum = médio | Muito baixo | Empate (Polygon resolve) |
| Time de desenvolvimento | Solidity = mais devs no mercado | Rust = menos devs | **EVM vence** |
| Portabilidade | ERC-3643 reconhecido globalmente | Apenas Solana-native | **EVM vence** |

**Decisão:** **Polygon (EVM) + ERC-3643 (T-REX)**, conforme já mencionado em `perguntas.md`. Se no futuro performance ou custo se tornarem críticos, Solana pode ser reavaliada — mas para este estágio, EVM é o caminho de menor risco.

### 4.2 Blockchains em Uso no Brasil

| Blockchain | Adoção no Brasil | Prós | Contras |
|-----------|-----------------|------|---------|
| **Ethereum (L1)** | Dominante para security tokens | Maior ecossistema, ERC-1400/3643, DeFi maduro | Gas fees altos |
| **Polygon** | Muito adotada (Liqi, Tokener, Alloy) | EVM, baixo custo, bridging com Ethereum | Menos institucional que permissionadas |
| **Stellar** | STOS, Plural, Toka | Compliance nativo (SEP-12 KYC), baixíssimo custo | Ecossistema menor, menos devs |
| **Hyperledger Besu** | Vórtx QR, AL5, Prova | Permissionada, compliance, privacidade | Sem liquidez pública, sem DeFi |
| **RSK (Rootstock)** | Tokenizando, Ripio | Segurança do Bitcoin, sidechain | Ecossistema pequeno |
| **BNB Chain** | Players menores | Baixo custo, EVM | Menos adoção institucional |

### 4.3 Padrões de Token

| Padrão | Uso | Adoção no Brasil | Recomendação |
|--------|-----|------------------|-------------|
| **ERC-20** | Base para utility tokens, governance, pools de liquidez | Quase universal | Usar para token de governance/platform |
| **ERC-1400** (Security Token Standard) | Suite: ERC-1410, ERC-1594, ERC-1643, ERC-1644 | Adoção moderada | **Não** — ERC-3643 supera |
| **ERC-3643 (T-REX)** | Security token com compliance nativo (KYC/AML modular via Claim Manager) | **Padrão emergente dominante** — Tokeny Solutions | **Sim — padrão escolhido** |
| **ERC-721 / ERC-1155** | NFT de fração de imóvel, misto fungível/não-fungível | Casos específicos (Santander + SIPRO B3) | Não necessário para MVP |

### 4.4 Compliance On-Chain

- **ERC-3643 / T-REX Claim Manager** — Claims modulares (investidor qualificado, residência, etc.). Só endereços compliant podem transferir/holdear tokens. **Base do sistema.**
- **Civic Pass / Jumio** — KYC terceirizado via whitelist de contratos. Alternativa se T-REX for complexo demais.
- **zkPass + Sismo** — KYC reutilizável via zero-knowledge proofs na Polygon (startup brasileira Trustless Society). Promissor para versões futuras.
- **Identidade Auto-Soberana (SSI)** — Verifiable Credentials (W3C) + ICP-Brasil.

### 4.5 Carteiras e Custódia

| Tipo | Soluções | Aplicação |
|------|----------|-----------|
| **Auto-custódia (não-qualificada)** | MetaMask, Ledger, Trezor, Torque (Tokensoft) | Investidores de varejo |
| **Custódia qualificada (regulada)** | Banco B3 (CustodyLink), Bitrust (K33), Vórtx, Cielo Custody, Fireblocks | **Obrigatório para o parceiro DTVM** |
| **ICP-Brasil + Blockchain** | Safeweb, Eiti (Digitalsign) | Assinatura digital com validade jurídica |

### 4.6 Oráculos

- **Chainlink** — Dominante. Preços, Keepers para valuations de terrenos tokenizados.
- **Pyth Network** — Dados de baixa latência para RWAs líquidos (títulos).
- **Oráculos customizados** — Integração com Cartórios via API para verificação de titularidade (ex: Prova).

### 4.7 Identidade Digital (ICP-Brasil)

- **Certificados A1/A3 (ICP-Brasil)** — Validade jurídica plena. Emissores: Valid (ex-Certisign), Serasa, Soluti.
- **Integração blockchain:** Certificado → DID (Decentralized Identifier) na Polygon → Verifiable Credential → smart contract gate → mint do token.
- **Projetos-piloto de referência:** Prova (31º Cartório SP), Aliança (6º Cartório RJ), IRIB + Techblocks.

### 4.8 Integração com Cartórios (Registro de Imóveis)

- **SREI (Sistema Eletrônico de Registro de Imóveis)** — Cartórios já aceitam ativos digitais como garantia via API.
- **Provimento 93/2023 CNJ** — Registro digital de tokens imobiliários. **Base normativa já existe.**
- **Estado atual:** Pilotos funcionais, mas ainda não em escala. Operação manual + blockchain híbrido na maioria dos casos.
- **Para o projeto:** O registro da SPE no cartório é obrigatório e tradicional. A tokenização é das cotas, não da matrícula — isso simplifica a integração cartorial no curto prazo.

### 4.9 Questões de Tecnologia em Aberto (de `perguntas.md`)

| Pergunta | Status |
|---|---|
| Construir do zero ou usar infra white-label? | **Em aberto** — Vórtx QR oferece white-label regulado; Tokeny oferece T-REX como plataforma |
| Auditar smart contracts? | **Sim, obrigatório** — estimativa de custo: US\$ 30–100k |
| Ponte fiat → token (on/off ramp)? | **Em aberto** — parceiro DTVM pode resolver; alternativa é gateway de pagamento (Stripe, Asaas) |
| Quem mantém infraestrutura pós-lançamento? | **Tokenizadora** — faz parte do modelo de receita recorrente |

---

## 5. Modelo de Negócio e Oportunidade

### 5.1 Fluxo de Capital (conforme `legal_memo.md`)

```
Investidor
    → Gateway de Pagamento / Conta Escrow
        → Conta da SPE (segregação patrimonial)
            → Aquisição do Ativo (terreno)
                → (ao longo do tempo) valorização
                    → Venda para incorporadora
                        → Distribuição do resultado aos tokenholders
```

**Princípio:** A startup **não transita o capital principal** por suas contas — apenas as taxas de estruturação e gestão.

### 5.2 Cadeia de Valor da Tokenização Imobiliária

```
Proprietário do Terreno (ex: Ricardo Lubarino)
    → SPE / Patrimônio de Afetação (veículo jurídico)
        → Parceiro DTVM (escriturador/custodiante legal)
            → Emissão de Tokens (Tokenizadora — plataforma própria ou white-label)
                → Distribuição Primária (via plataforma + parceiros de distribuição)
                    → Mercado Secundário (liquidez entre investidores)
                        → Evento de Saída (venda do terreno + destokenização)
```

### 5.3 Quem Ganha o Quê

| Elo | Margem Típica | Quem Captura |
|-----|--------------|-------------|
| Estruturação jurídica (SPE, regime fiduciário) | R\$ 30–100k fixo | Escritórios de advocacia |
| **Emissão dos tokens** | **3–5% do valor** | **Tokenizadora** (ou parceiro white-label) |
| Distribuição primária | 1–3% | Parceiro de distribuição / DTVM |
| Custódia qualificada | 0.3–0.5% a.a. | Bancos custodiante (B3, Vórtx) |
| **Trading secundário** | **1–2% por transação** | **Tokenizadora** |
| **Taxa de administração da SPE** | **0.5–1% a.a.** | **Tokenizadora** |

### 5.4 Modelo de Receita da Startup

Com base em `perguntas.md` (M5), três pernas de receita:

1. **Taxa de estruturação (one-shot):** 3–5% sobre o valor do ativo tokenizado
   - Ex: Terreno de R\$ 10M → R\$ 300–500k
2. **Taxa de administração (recorrente):** 0.5–1% a.a. sobre o valor sob gestão
   - Ex: R\$ 10M → R\$ 50–100k/ano por ativo
3. **Taxa de trading secundário (recorrente):** 1–2% por transação

**Critério de saúde do negócio:** Sem recorrência, é consultoria, não startup. A taxa de administração anual é o que transforma o modelo em negócio escalável.

### 5.5 Oportunidade — Real Estate de Luxo

**Por que terrenos de luxo são o nicho ideal:**

1. **Ticket alto** (R\$ 5–50M) → viabilidade econômica para estruturação jurídica complexa
2. **Público qualificado** → menor custo de KYC/AML (já são investidores)
3. **Demanda por diversificação** → family offices e HNWIs buscam exposição fractional a ativos alternativos
4. **Baixa liquidez natural do setor** → tokenização resolve o maior problema do mercado de terrenos de alto padrão
5. **Margens mais altas** → taxa de 3–5% sobre R\$ 10M é R\$ 300–500k por operação
6. **Terreno não gera receita operacional** → modelo mais simples que imóvel de renda (sem gestão de aluguel, reformas, inquilinos)
7. **Expectativa de valorização pura** → menos complexidade operacional, atrativo para perfil de investidor que busca ganho de capital

**Diferenciais competitivos:**

- Foco exclusivo em **terrenos de luxo** (nenhum player faz isso de forma dedicada)
- **Liquidez secundária** via pool de market makers ou matching engine próprio
- **Integração fiscal** completa (NFe, IR, ITBI, ITCMD automatizados)
- **Experiência wealth management** (não "compre seu token", mas "alocação em ativos reais")
- **Curadoria de ativos** — seleção criteriosa de terrenos com potencial de valorização comprovado

### 5.6 Resumo Financeiro para o Primeiro Ativo

| Item | Estimativa |
|------|-----------|
| Valor do terreno (Ricardo Lubarino) | A definir (laudo independente) |
| Taxa de estruturação (3–5%) | R\$ 30–500k (dependente do valor) |
| Custo de estruturação (SPE + contratos + registro) | R\$ 30–100k |
| Custo de desenvolvimento da plataforma (MVP) | Em aberto (build vs white-label) |
| Custo de auditoria de smart contracts | US\$ 30–100k |
| Custo de KYC/AML por investidor | R\$ 50–200 por cadastro |
| Taxa de administração anual (0.5–1%) | R\$ 5–100k/ano |

### 5.7 Riscos

| Risco | Severidade | Mitigação |
|-------|-----------|-----------|
| Incerteza regulatória (PL 4401 ainda em tramitação) | Alta | Estruturar via SPE + Resolução CVM 88 (crowdfunding) |
| Baixa liquidez secundária | Alta | Market making próprio; pool de liquidez restrito; janelas de recompra |
| Complexidade cartorial | Média | Tokenizar cotas da SPE (não a matrícula) simplifica; Provimento 93/CNJ já vigora |
| Volatilidade do mercado imobiliário de luxo | Média | Diversificação de ativos no pool |
| Custo de estruturação jurídica por operação | Média | Padronizar SPEs e contratos (diminui a cada ativo) |
| Dependência de parceiro regulado (DTVM) | Média | Contratos claros; due diligence do parceiro |
| Risco de execução (build vs buy) | Média | White-label (Vórtx/Tokeny) reduz risco técnico |

---

## 6. Roteiro de Execução (M0–M5)

### M0 — Ativo (Due Diligence)

**Responsável:** Proprietário (Ricardo Lubarino) + equipe

- [ ] Confirmar matrícula limpa, sem ônus, penhoras ou disputas
- [ ] Definir titular formal e necessidade de SPE
- [ ] Obter laudo de avaliação independente
- [ ] Negociar condições: transferência para SPE, custos de cartório, participação do proprietário
- [ ] Definir ticket mínimo, número de cotas, valor por cota

### M1 — Jurídico e Regulatório

**Responsável:** Escritório de advocacia especializado + Tokenizadora

- [ ] Obter parecer sobre enquadramento do token (quase certamente security token)
- [ ] Criar SPE para o primeiro ativo
- [ ] Escolher caminho CVM: **Resolução 88 (crowdfunding)** é o mais rápido para MVP
- [ ] Contratar/formalizar parceria com **DTVM ou escriturador** regulado
- [ ] Definir regime fiduciário e registrar no cartório
- [ ] Estruturar contratos: termos de oferta, acordo de cotistas, política de KYC/AML
- [ ] Avaliar entrada no sandbox CVM para modelos futuros
- [ ] Definir tributação (ganho de capital na venda dos tokens, distribuição de lucros da SPE)

### M2 — Tecnologia

**Responsável:** Time de engenharia da Tokenizadora

- **Blockchain:** Polygon (EVM) — decisão tomada
- **Padrão de token:** ERC-3643 (T-REX) — Tokeny Solutions como referência
- **Decisão crítica:** construir plataforma própria ou usar white-label da Vórtx QR? Recomendação: começar com T-REX (Tokeny) para smart contracts + frontend próprio
- [ ] Implementar smart contracts (ou integração com Tokeny)
- [ ] Auditar contratos (empresa especializada)
- [ ] Construir portal do investidor: onboarding, KYC, subscrição, dashboard
- [ ] Implementar on/off ramp (gateway de pagamento + parceiro DTVM)
- [ ] Integrar carteiras (MetaMask para auto-custódia; wallet custodiada para investidores não-técnicos)
- [ ] Implementar compliance on-chain (Claim Manager do T-REX)
- [ ] Testes de segurança e penetração

### M3 — Distribuição e Venda

- [ ] Definir estratégia de captação: lista de investidores qualificados, family offices, HNWIs
- [ ] Implementar KYC/AML (terceirizado ou via parceiro DTVM)
- [ ] Definir mecânica da oferta: valor mínimo de captação, prazo, condições de devolução
- [ ] Registrar oferta na CVM (ou usar dispensa da Resolução 88)
- [ ] Lançar campanha de captação

### M4 — Pós-Venda

- [ ] Disponibilizar mercado secundário interno
- [ ] Definir janelas de liquidez (trimestrais?)
- [ ] Implementar pool de market maker (capital inicial para provimento de liquidez)
- [ ] Estabelecer governança: assembleia de tokenholders, prestação de contas, relatórios periódicos
- [ ] Gestão da SPE: pagamento de taxas, manutenção do registro, contabilidade
- [ ] Preparar evento de saída: venda do terreno para incorporadora + distribuição + destokenização

### M5 — A Startup em Si

- [ ] Definir estrutura societária (LTDA ou S.A.?)
- [ ] Captação inicial (seed): quanto capital para chegar à primeira receita?
- [ ] Pipeline de ativos: quantas tokenizações por ano para cobrir a operação?
- [ ] Contratações: CTO (blockchain), CGO (parcerias + ativos), jurídico, compliance
- [ ] Definição de marca, posicionamento, site institucional
- [ ] Estratégia de go-to-market: eventos de wealth management, family offices, assessorias de investimento

---

## 7. Perguntas em Aberto

Da `perguntas.md` original que ainda precisam de resposta:

### Tecnologia
- **Build vs white-label?** Construir própria com T-REX ou usar infraestrutura da Vórtx QR / Tokeny?
- **Quem mantém o site e infraestrutura pós-lançamento?** (Tokenizadora — precisa de equipe contínua)

### Distribuição
- **Quem compra? Já existe lista ou é suposição?** Precisa de validação com family offices
- **CAC estimado? Quem paga marketing da oferta?** A definir
- **O que acontece se captar só 30%?** Precisa de captação mínima e regra de devolução

### Modelo de Negócio
- **Receita é one-shot ou recorrente?** Ideal: ambas (estruturação + adm. anual)
- **Quantas tokenizações/ano para cobrir operação?** Depende do ticket e da margem
- **Por que um dono de ativo escolheria a Tokenizadora vs Liqi/MB Tokens?** Diferencial: curadoria de luxo + atenção dedicada + melhor experiência
- **Quanto capital para chegar à primeira receita?** A modelar

---

## 8. Anexos e Referências

### Fontes Oficiais
- CVM — Parecer 40/2022, Instrução 588/2017, Resolução 88/2022, RCM 50/2020
- BCB — Resoluções 4.888/2020, 5.000/2022, 5.108/2024, 519/520/521/2025
- CNJ — Provimento 93/2023
- Câmara dos Deputados — PL 4401/2021, PL 2304/2024, PL 3825/2023

### Players e Dados de Mercado
- Liqi: liqi.com.br
- Vórtx QR Tokenizadora: vortx.com.br
- ReitBZ: reitbz.com.br
- STOS: stos.com.br
- Mercado Bitcoin: mercadobitcoin.com.br
- Tokenizando: tokenizando.com.br
- Tokeny Solutions: tokeny.com

### Padrões Técnicos
- ERC-3643 (T-REX): github.com/ethereum/eips/issues/3643, docs.tokeny.com
- ERC-1400: github.com/ethereum/eips/issues/1400
- ICP-Brasil: iti.gov.br
- Provimento 93/CNJ: cnj.jus.br

### Documentos do Projeto no Repositório
- `legal_memo.md` — Estrutura de negócio e fluxo operacional
- `perguntas.md` — Due diligence M0-M5
- `guia-startup-tokenizacao-brasil-2026.md` — Guia regulatório geral
- `tokeny.md` — Análise Tokeny T-REX vs Solana
- `esteira_tokenizacao_modulos.svg` — Diagrama visual do fluxo

---

*Este documento é uma pesquisa exploratória integrada aos documentos do repositório e não constitui aconselhamento jurídico ou financeiro.*

*Atualizado em junho/2026 para refletir as decisões de projeto, análises dos documentos existentes e alinhamento com o modelo de negócio proposto em `legal_memo.md`.*
