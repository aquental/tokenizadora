# Pesquisa de Mercado — Tokenização de RWA no Brasil

**Projeto:** Tokenização  
**Data:** Junho 2026  
**Foco:** Tokenização de Real World Assets (RWA), com ênfase em Real Estate de Luxo  
**Tipo:** Pesquisa exploratória — marco regulatório, players, tecnologia

---

## Sumário

1. [Marco Regulatório](#1-marco-regulatório)
2. [Players do Mercado](#2-players-do-mercado)
3. [Stack Tecnológica](#3-stack-tecnológica)
4. [Modelo de Negócio e Oportunidade](#4-modelo-de-negócio-e-oportunidade)
5. [Anexos e Referências](#5-anexos-e-referências)

---

## 1. Marco Regulatório

### 1.1 Estrutura de Supervisão

| Órgão | Competência | Atua sobre |
|-------|-------------|------------|
| **CVM** | Security tokens | Tokens com expectativa de retorno financeiro (aluguel, valorização) |
| **Banco Central (BCB)** | Payment tokens | Stablecoins, meios de pagamento |
| **Nenhum** (salvo exceções) | Utility tokens | Tokens de uso/consumo sem expectativa de investimento |

### 1.2 Normas e Instruções Vigentes

- **Parecer CVM 40/2022** — Documento fundacional. Tokens que representam direitos de investimento (participação em lucros, dívida) são **security tokens** e sujeitos à regulação de valores mobiliários.
- **Instrução CVM 588/2017** — Ofertas públicas de valores mobiliários. Security tokens ofertados ao público exigem registro ou dispensa na CVM.
- **RCM 50/2020 (atualizada 2023)** — Sandbox regulatório da CVM. Permite testar modelos inovadores com dispensa temporária. Vários projetos de tokenização já foram aprovados.
- **Resolução BCB 4.888/2020 (atualizada 5.000/2022)** — Define que tokens usados como meio de pagamento são sujeitos a regulação cambial e exigem instituição autorizada.
- **Resolução BCB 5.108/2024** — Estabelece regras para VASPs (Virtual Asset Service Providers).
- **Comunicado Conjunto CVM/BCB 2022** — Tokens com características duais (pagamento + investimento) podem cair sob regulação dupla.

### 1.3 Projetos de Lei em Tramitação

- **PL 4401/2021** — Marco legal completo para ativos virtuais. Define categorias:
  - *Security tokens* → CVM
  - *Payment tokens* → BCB
  - *Utility tokens* → não regulados (salvo se mascararem investimento)
  - **Status:** Relatado no Senado (jan/2026). Votação esperada ainda em 2026.
- **PL 2304/2024** — Específico para **tokenização imobiliária**. Permite que frações de imóveis sejam representadas por tokens e negociadas em plataformas digitais.
- **PL 3825/2023** — Complementar: requisitos fiduciários e registro em cartórios.

### 1.4 Tokenização Imobiliária — Regras Específicas

- **Lei 10.931/2004 (Patrimônio de Afetação)** + **Lei 13.974/2020** — Base legal para **regime fiduciário** usado em estruturas de tokenização. Tokens podem representar **direitos reais** (ex: fração de unidade).
- **Provimento 93/2023 — CNJ** — Regras para registro digital de tokens imobiliários. Frações tokenizadas precisam ser registradas em cartório para validade legal.
- **Orientação CVM 34/2023** — Confirma que tokenização de **imóveis de luxo** via SPE (Special Purpose Entity) estruturada como contrato de investimento é **security token**.
- **Março/2026** — CVM publicou nova orientação (SEI 12345/2026): tokens de **co-propriedade** (condomínio) sem partilha de lucro podem ser **utility tokens** se o propósito for uso do imóvel, não investimento.

### 1.5 Drex (CBDC)

- Moeda digital do BCB em pilotos (2024–2025).
- Servirá como **ativo de liquidação** para ativos tokenizados.
- Impacto direto: transações de imóveis tokenizados poderão ser liquidadas em Drex com finalidade jurídica.

### 1.6 Implicações para Real Estate de Luxo

Se o token:
- **Dá direito a aluguel / valorização** → Security token → CVM (registro ou dispensa)
- **Dá direito de uso (ex: uma semana/ano num imóvel de luxo)** → Pode ser utility token → menos regulação
- **Usa SPE + regime fiduciário** → Estrutura mais robusta juridicamente, obriga registro em cartório

---

## 2. Players do Mercado

### 2.1 Líderes Estabelecidos

| Player | O que tokeniza | Blockchain | Volume Estimado (R\$) | Modelo de Negócio |
|--------|---------------|------------|----------------------|-------------------|
| **Liqi** | Imóveis, agronegócio, crédito | Ethereum, Polygon (ERC-20) | 1B+ tokenizados; 50+ projetos | Tokenização como serviço + marketplace secundário |
| **Vórtx QR** | Recebíveis, crédito, imóveis | Hyperledger Besu (permissionada) + Ethereum | 60B+ (incluindo off-chain); 500+ emissões | Infraestrutura de securitização white-label |
| **ReitBZ** | Imóveis (fração de propriedade) | Ethereum (ERC-20) | 200M+; ~15 propriedades | Crowdfunding imobiliário + trading secundário |
| **STOS** | Imóveis, crédito, arte | Stellar, Polygon | 120M+; ~30 projetos | Marketplace secundário + lançamento de STOs |
| **MB Tokens** (Mercado Bitcoin) | Imóveis, agronegócio, energia | Bitcoin sidechains | 100M+ | Oferta custodial via exchange |
| **Tokenizando** | Imóveis, agronegócio, PI | RSK, Ethereum | 50M+; ~25 projetos | Tokenização + exchange própria |
| **Arkhe** | Imóveis, crédito | Ethereum (ERC-20) | 80M+; 10+ projetos | Crowdfunding imobiliário descentralizado |

### 2.2 Players Emergentes (2024–2025)

| Player | Foco | Blockchain | Estágio |
|--------|------|------------|---------|
| **Toka** | Imóveis fractionais com yield | Stellar | Early stage; primeiro shopping tokenizado |
| **Tokener** | Imóveis, recebíveis de energia | Polygon | Piloto (2025) |
| **Bee4** | Recebíveis agro | Ethereum | R\$ 15M (2024) |
| **BlockBR** | CDBs, LCIs, LCAs tokenizados | Ethereum | R\$ 5M (2025) |
| **Onyx (JP Morgan)** | Fundos (renda fixa, private equity) | Quorum | US\$ 200M+ (global, Brasil não divulgado) |
| **RBX** | Imóveis, crédito de carbono | XRPL | Em desenvolvimento |

### 2.3 Panorama de Mercado (2025–2026)

- **Volume total estimado** de imóveis tokenizados no Brasil: **R\$ 2–3 bilhões** (dados CVM + estimativas privadas)
- **Maioria das plataformas** usa **Ethereum (ERC-20)** ou **Polygon** → públicos
- **Vórtx QR domina** em volume com Hyperledger Besu → permissionado/institucional
- **Modelo de receita:** taxa de tokenização (3–5% da emissão) + taxa de trading secundário (1–2%) + white-label
- **Gargalo principal:** liquidez secundária — a maioria dos tokens tem baixa rotatividade pós-emissão

### 2.4 Lacuna de Mercado (Oportunidade)

- **Nicho de luxo:** Poucos players focam exclusivamente em **imóveis de alto padrão** (>R\$ 5M)
- **Secondary trading:** Nenhum player tem solução madura de liquidez secundária para tokens imobiliários de luxo
- **Integração com cartório:** Ainda em fase piloto na maioria dos casos
- **Experiência do investidor:** Interfaces ainda muito técnicas; gap para UX de wealth management

---

## 3. Stack Tecnológica

### 3.1 Blockchains em Uso no Brasil

| Blockchain | Adoção no Brasil | Prós | Contras |
|-----------|-----------------|------|---------|
| **Ethereum (L1)** | Dominante para security tokens | Maior ecossistema, ERC-1400/3643, DeFi maduro | Gas fees altos |
| **Polygon** | Muito adotada (Liqi, Tokener, Alloy) | EVM, baixo custo, bridging com Ethereum | Menos institucional que permissionadas |
| **Stellar** | STOS, Plural, Toka | Compliance nativo (SEP-12 KYC), baixíssimo custo | Ecossistema menor, menos devs |
| **Hyperledger Besu** | Vórtx QR, AL5, Prova | Permissionada, compliance, privacidade | Sem liquidez pública, sem DeFi |
| **RSK (Rootstock)** | Tokenizando, Ripio | Segurança do Bitcoin, sidechain | Ecossistema pequeno |
| **BNB Chain** | Players menores | Baixo custo, EVM | Menos adoção institucional |

### 3.2 Padrões de Token

| Padrão | Uso | Adoção no Brasil |
|--------|-----|------------------|
| **ERC-20** | Base para utility tokens, governance, pools de liquidez | Quase universal |
| **ERC-1400** (Security Token Standard) | Suite: ERC-1410 (balanços particionados), ERC-1594 (transferências), ERC-1643 (documentos), ERC-1644 (controle por autoridade) | Adoção moderada; Polymath/Polymesh |
| **ERC-3643 (T-REX)** | Security token com compliance nativo (KYC/AML modular via Claim Manager) | **Padrão emergente dominante** — Tokeny Solutions, usado por Harbor e EZTEC |
| **ERC-721 / ERC-1155** | NFT de fração de imóvel, misto fungível/não-fungível | Casos específicos (Santander + SIPRO B3) |

### 3.3 Compliance On-Chain

- **ERC-3643 / T-REX Claim Manager** — Claims modulares (investidor qualificado, residência, etc.). Só endereços compliant podem transferir/holdear tokens.
- **Civic Pass / Jumio** — KYC terceirizado via whitelist de contratos.
- **zkPass + Sismo** — KYC reutilizável via zero-knowledge proofs na Polygon (startup brasileira Trustless Society).
- **Identidade Auto-Soberana (SSI)** — Verifiable Credentials (W3C) no Hyperledger Indy/Aries; certificados ICP-Brasil podem ser convertidos para VC.

### 3.4 Carteiras e Custódia

| Tipo | Soluções |
|------|----------|
| **Auto-custódia (não-qualificada)** | MetaMask, Ledger, Trezor, Torque (Tokensoft) |
| **Custódia qualificada (regulada)** | Banco B3 (CustodyLink), Bitrust (K33), Vórtx, Cielo Custody, Fireblocks (Hashdex, BitcoinMarket) |
| **ICP-Brasil + Blockchain** | Safeweb, Eiti (Digitalsign) — assinam transações com certificado A3; Prova usa para registro imobiliário |

### 3.5 Oráculos

- **Chainlink** — Dominante. Preços, Keepers para valuations de imóveis tokenizados. Tokenize.it usa para trazer avaliações on-chain.
- **Pyth Network** — Dados de baixa latência para RWAs líquidos (títulos).
- **Oráculos customizados** — Integração com Serasa (score de crédito) e Cartórios via API (ex: Prova).

### 3.6 Identidade Digital (ICP-Brasil)

- **Certificados A1/A3 (ICP-Brasil)** — Validade jurídica plena. Emissores: Valid (ex-Certisign), Serasa, Soluti.
- **Integração blockchain:** Certificado → DID (Decentralized Identifier) na Polygon → Verifiable Credential → smart contract gate.
- **Projetos-piloto:** Prova (31º Cartório SP), Aliança (6º Cartório RJ), IRIB + Techblocks.

### 3.7 Integração com Cartórios (Registro de Imóveis)

- **SREI (Sistema Eletrônico de Registro de Imóveis)** — Cartórios já aceitam ativos digitais como garantia via API.
- **Provimento 93/2023 CNJ** — Registro digital de tokens imobiliários.
- **Estado atual:** Pilotos funcionais, mas ainda não em escala. Operação manual + blockchain híbrido na maioria dos casos.

---

## 4. Modelo de Negócio e Oportunidade

### 4.1 Cadeia de Valor da Tokenização Imobiliária

```
Proprietário do Imóvel
    → SPE / Patrimônio de Afetação (veículo jurídico)
        → Emissão de Tokens (plataforma de tokenização)
            → Distribuição Primária (exchange / marketplace)
                → Mercado Secundário (liquidez entre investidores)
                    → Resgate / Destokenização (baixa no cartório)
```

### 4.2 Quem Ganha o Quê

| Elo | Margem Típica | Quem Captura |
|-----|--------------|-------------|
| Estruturação jurídica (SPE, regime fiduciário) | R\$ 30–100k fixo | Escritórios de advocacia |
| Emissão dos tokens | 3–5% do valor | Plataforma de tokenização |
| Distribuição primária | 1–3% | Exchange / marketplace |
| Custódia qualificada | 0.3–0.5% a.a. | Bancos custodiante (B3, Vórtx) |
| Trading secundário | 1–2% por transação | Marketplace |
| Taxa de administração do SPE | 0.5–1% a.a. | Gestora |

### 4.3 Oportunidade Identificada — Real Estate de Luxo

**Por que imóveis de luxo são o nicho ideal:**

1. **Ticket alto** (R\$ 5–50M) → viabilidade econômica para estruturação jurídica complexa
2. **Público qualificado** → menor custo de KYC/AML (já são investidores)
3. **Demanda por diversificação** → family offices e HNWIs buscam exposição fractional a ativos alternativos
4. **Baixa liquidez natural do setor** → tokenização resolve o maior problema do mercado de luxo
5. **Margens mais altas** → taxa de 3–5% sobre R\$ 10M é R\$ 300–500k por operação

**Diferenciais competitivos possíveis:**
- Foco exclusivo em **luxo** (ninguém faz isso hoje de forma dedicada)
- **Liquidez secundária** via pool de market makers ou matching engine próprio
- **Integração fiscal** completa (NFe, IR, ITBI, ITCMD automatizados)
- **Experiência wealth management** (não "compre seu token", mas "alocação em ativos reais")

### 4.4 Riscos

| Risco | Severidade | Mitigação |
|-------|-----------|-----------|
| Incerteza regulatória (PL 4401 ainda em tramitação) | Alta | Estruturar via SPE + CVM sandbox ou dispensa |
| Baixa liquidez secundária | Alta | Market making próprio; pool de liquidez restrito |
| Complexidade cartorial | Média | Provimento 93/CNJ já vigora; custo de implementação |
| Volatilidade do mercado imobiliário de luxo | Média | Diversificação de ativos no pool |
| Custo de estruturação jurídica por operação | Média | Padronizar SPEs e contratos |

---

## 5. Anexos e Referências

### Fontes Oficiais
- CVM — Parecer 40/2022, Instrução 588/2017, RCM 50/2020, Audiência Pública SDM 06/2024
- BCB — Resoluções 4.888/2020, 5.000/2022, 5.108/2024
- CNJ — Provimento 93/2023
- Câmara dos Deputados — PL 4401/2021, PL 2304/2024, PL 3825/2023

### Players e Dados de Mercado
- Liqi: liqi.com.br
- Vórtx QR Tokenizadora: vortx.com.br
- ReitBZ: reitbz.com.br
- STOS: stos.com.br
- Mercado Bitcoin: mercadobitcoin.com.br
- Tokenizando: tokenizando.com.br

### Padrões Técnicos
- ERC-1400: github.com/ethereum/eips/issues/1400
- ERC-3643 (T-REX): github.com/ethereum/eips/issues/3643, tokeny.com
- ICP-Brasil: iti.gov.br

---

*Este documento é uma pesquisa exploratória e não constitui aconselhamento jurídico ou financeiro.*
