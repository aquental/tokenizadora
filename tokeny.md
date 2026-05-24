# Tokeny

O processo completo de tokenização de valores mobiliários na plataforma T-REX da Tokeny, cobrindo toda a jornada do ativo: onboarding, emissão, servicing e distribuição secundária.[1]

## Ideia central

A proposta da Tokeny é simplificar mercados de capitais com tokenização, escondendo a complexidade do blockchain para emissores, agentes e investidores. A plataforma é apresentada como agnóstica em relação ao tipo de ativo, à jurisdição e também multicadeia dentro do ecossistema EVM.[1]

## Onboarding

Na etapa de onboarding, os investidores passam por verificação KYC, envio de documentos e qualificação por emissores ou agentes de compliance. Depois disso, assinam a documentação digitalmente e podem entrar no processo de subscrição. O sistema também aceita pagamentos em moeda fiduciária e em cripto/tokenized cash, com reconciliação e confirmação integradas.[1]

## Emissão

Na emissão, os emissores implantam o smart contract do token ERC3643 e configuram informações do ativo, regras de elegibilidade, compliance e armazenamento de identidade. Em seguida, os tokens são alocados aos investidores, com geração automática de identidade digital quando necessário e atualização em tempo real do cap table.[1]

## Servicing

A parte de servicing vai além de relatórios: inclui ações corporativas, gestão do cap table, exportação de relatórios e ferramentas operacionais para emissores e agentes. O sistema permite operações como mint, burn, pause, block/unblock, force transfer e recover tokens, sempre com controle de compliance. Também há suporte para subscrições contínuas, resgates e mensagens aos investidores.[1]

## Distribuição secundária

Na distribuição secundária, os tokens podem ser marcados como negociáveis e transferidos apenas entre investidores qualificados. A Tokeny cita várias rotas de liquidez: bulletin board, exchanges centralizadas, protocolos DeFi, DEXs e marketplaces OTC. Em todos os casos, o objetivo é manter compliance embutido no token e atualização automática do cap table.[1]

## Benefícios principais

O material destaca ganhos para emissores, agentes e investidores: mais automação, menos custo operacional, dados em tempo real, melhor experiência digital e maior escalabilidade. Para os investidores, a experiência é descrita como mais parecida com e-commerce, com acesso 24/7 para comprar, manter, transferir e recuperar tokens.[1]

## Resumo em uma frase

Em termos simples, o arquivo mostra como a Tokeny usa a plataforma T-REX para transformar a emissão e a gestão de valores mobiliários em um fluxo digital, automatizado e com compliance embutido em todo o ciclo de vida.[1]

Fontes
[1] The-Complete-Tokenization-Process-Tokeny.pdf https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/collection_36c355f2-66dc-4a82-9047-ec2473c71122/967e326f-190a-47f0-b2d0-97146e62d74e/The-Complete-Tokenization-Process-Tokeny.pdf

---

# Clonar na Solana faz sentido?

Faz sentido **do ponto de vista de produto**, mas não é um simples “_porte_” entre blockchains. A ideia da Tokeny pode ser implementada em outra rede, inclusive Solana, porém é necessário redesenhar a camada de smart contracts, identidade, regras de compliance e integrações de mercado para o modelo nativo dessa blockchain.[1][2][3]

## O que muda em Solana

A Tokeny foi construída em torno do [ERC-3643](https://www.erc3643.org/), que é um padrão criado para ativos permissionados no ecossistema EVM e usa identidade on-chain, whitelist e regras de transferência no próprio token. Solana tem outra arquitetura e oferece ferramentas próprias para compliance e controle, como transfer hooks e extensões de token, então a implementação teria que ser adaptada em vez de reaproveitada literalmente. Em outras palavras: o **conceito** é transferível, mas a infraestrutura técnica muda bastante.[2][3][4][5][1]

## Quando vale a pena

Faz mais sentido em Solana se o objetivo for aproveitar **taxa baixa**, **alta performance** e **liquidação rápida**, especialmente para fluxos com muitas transferências ou maior exigência de escalabilidade. Também pode fazer sentido se você quiser atingir um ecossistema que já esteja construindo soluções de RWA e compliance nativas em Solana. Para um projeto institucional, isso pode ser atraente se a sua prioridade for throughput e custo operacional.[6][7][2]

## Principais riscos

O maior risco é regulatório, não técnico: tokenizar valores mobiliários exige KYC/AML, controle de jurisdição, restrições de transferência e trilha auditável, independentemente da blockchain usada. Outro ponto é a maturidade do ecossistema: na prática, o caminho de distribuição, custódia, agentes e mercado secundário precisa existir ou ser construído para a nova rede. Se você migrar só por “moda”, sem parceiros e infraestrutura de mercado, o projeto pode ficar tecnicamente bom e comercialmente fraco.[7][8][9][1][2]

## Leitura prática

Se a sua meta é replicar a lógica da Tokeny, a decisão é menos “Ethereum vs Solana” e mais “qual stack suporta melhor o meu modelo regulado?”. Se você já está preso ao padrão ERC-3643 e a parceiros do mundo EVM, continuar em EVM tende a ser mais simples. Se quer construir algo novo, com mais performance e uma arquitetura Solana-native, aí a migração pode fazer sentido — desde que o compliance e a distribuição sejam redesenhados junto.[3][5]

Fontes
[1] ERC3643 - The Token Standard for RWA Tokenization https://www.erc3643.org
[2] Real World Assets - Solana https://solana.com/solutions/real-world-assets
[3] ERC-3643 Permissioned Tokens - Tokeny - Documentation https://docs.tokeny.com/docs/the-erc-3643-token-standard
[4] What is ERC3643 on Solana? https://solana.com/el/developers/evm-to-svm/erc3643
[5] Ethereum Community Approves ERC3643 as the First ... https://www.erc3643.org/news/ethereum-community-approves-erc3643-as-the-first-tokenization-standard
[6] How to issue tokenized securities on Solana https://www.linkedin.com/posts/norbertgehrke_solana-tokenized-securities-activity-7330110192061177857-Nus2
[7] Solana RWA Token Program - QuillAudits https://www.quillaudits.com/research/rwa-development/non-evm-standards/solana-rwa-token-program
[8] What is ERC-3643? The Token Standard Powering Institutional ... https://www.finextra.com/blogposting/31460/what-is-erc-3643-the-token-standard-powering-institutional-finance
[9] Introduction to ERC-3643 Tokens - Chainalysis https://www.chainalysis.com/blog/introduction-to-erc-3643-ethereum-rwa-token-standard/
[10] ERC-3643 – The Official Smart Contract Standard for Permissioned ... https://tokeny.com/erc3643/
[11] Tokenization Is Growing Up - And ERC-3643 Is Leading the Charge. https://www.linkedin.com/posts/muneebahmed9398_tokenization-ethereum-solana-activity-7385925241081950208-W5Sk
[12] TOKENY: Token for Regulated Exchanges ERC-3643 https://seeblocks.eu/use-cases-list/tokeny-token-regulated-exchanges-erc-3643
[13] ERC3643 Token Standard | Boulder Tech Docs https://docs.bouldertech.fi/boulder-tech-docs/technology/erc3643-token-standard
[14] Statistical Securities Compliance on Solana by Brian Haney :: SSRN https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4189147
[15] Tokenized Securities: The On-Chain Revolution and Compliance ... https://www.binance.com/en/square/post/26781804835266

### tabela comparativa entre o modelo da Tokeny/ERC-3643 e uma implementação equivalente em Solana.

| Critério                | Tokeny / ERC-3643 em EVM                                                                                                             | Implementação semelhante em Solana                                                                                                                          |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Base técnica            | Padrão ERC-3643, um conjunto de smart contracts para tokens permissionados com identidade e regras de transferência embutidas [1][2] | Teria de usar o stack nativo de Solana e suas extensões para criar lógica de compliance equivalente [3][4]                                                  |
| Identidade e compliance | ONCHAINID e regras de oferta/investidor verificadas em cada transferência [1][5]                                                     | Solana já expõe tooling nativo para KYC/compliance, como transfer hooks, mas a arquitetura é diferente [3]                                                  |
| Transferências          | Só ocorrem entre investidores elegíveis, com validação no próprio token [1][6]                                                       | Também é viável, mas exigiria implementação específica para bloquear, permitir e auditar transferências [3][7]                                              |
| Emissão e servicing     | A Tokeny oferece fluxo completo: onboarding, emissão, servicing, cap table e ações corporativas [5][2]                               | Seria possível replicar a lógica, mas você teria que construir ou integrar boa parte da camada operacional no ecossistema Solana [3][8]                     |
| Liquidez e distribuição | Integração com exchanges, bulletin boards e soluções secundárias já pensadas para o modelo permissionado [9][5]                      | Solana tem ecossistema RWA crescente e possibilidade de distribuição mais rápida, mas a infraestrutura institucional precisa ser montada caso a caso [3][7] |
| Ecossistema maduro      | Forte histórico em tokenização de securities no mundo EVM e ERC-3643 amplamente documentado [1][10]                                  | Ecossistema RWA em crescimento, com propostas e padrões próprios ganhando espaço, mas ainda mais novo para security tokens institucionais [3][11]           |
| Portabilidade           | Mais interoperável com ferramentas EVM e contratos Solidity existentes [5][12]                                                       | Menos reaproveitamento direto do stack EVM; você ganha performance, mas perde compatibilidade imediata com Solidity/EVM [3][4]                              |
| Risco regulatório       | Compliance já é parte central do design do token [1][6]                                                                              | O risco regulatório continua igual; mudar de blockchain não reduz obrigação de KYC/AML e controle de jurisdição [1][3]                                      |
| Melhor uso              | Projetos que valorizam padrão já consolidado, compatibilidade EVM e fluxo institucional pronto [5][2]                                | Projetos que priorizam performance, custo baixo e querem construir uma stack Solana-native para RWA [3][13]                                                 |

## Leitura prática

Se o seu objetivo é copiar o modelo de negócio da Tokeny com o menor risco de execução, EVM/ERC-3643 ainda parece o caminho mais direto. Se a prioridade for construir uma plataforma nova, mais rápida e potencialmente mais barata para operação em escala, Solana pode fazer sentido — mas com mais trabalho de engenharia e integração.[1][2][3][7]

## Minha conclusão

A ideia é **portável**, mas não é plug-and-play. Em Solana, você recria a lógica de tokenização permissionada com outra arquitetura, enquanto em EVM você reaproveita melhor o padrão que já existe e já foi pensado para esse caso.[3][1]

Fontes
[1] ERC3643 - The Token Standard for RWA Tokenization https://www.erc3643.org
[2] ERC-3643 Permissioned Tokens - Tokeny - Documentation https://docs.tokeny.com/docs/the-erc-3643-token-standard
[3] Real World Assets - Solana https://solana.com/solutions/real-world-assets
[4] Overview of Real World Assets on Solana - Reflexivity Research https://reflexivity-research.webflow.io/all-reports/overview-of-real-world-assets-on-solana
[5] ERC-3643 – The Official Smart Contract Standard for Permissioned ... https://tokeny.com/erc3643/
[6] TOKENY: Token for Regulated Exchanges ERC-3643 https://seeblocks.eu/use-cases-list/tokeny-token-regulated-exchanges-erc-3643
[7] Real World Assets on Solana: A Comprehensive Overview - Helius https://www.helius.dev/blog/solana-real-world-assets
[8] Top Real World Assets (RWA) projects - Solana Compass https://solanacompass.com/projects/category/real-world-assets
[9] The-Complete-Tokenization-Process-Tokeny.pdf https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/collection_36c355f2-66dc-4a82-9047-ec2473c71122/967e326f-190a-47f0-b2d0-97146e62d74e/The-Complete-Tokenization-Process-Tokeny.pdf
[10] History of ERC-3643 https://www.erc3643.org/history-of-erc-3643
[11] sRFC 00020: RWA/Security Token Standard https://forum.solana.com/t/srfc-00020-rwa-security-token-standard/370
[12] GitHub - TokenySolutions/T-REX: T-REX is a suite of smart contracts ... https://github.com/TokenySolutions/T-REX
[13] Solana's Real-World Asset Ecosystem Hits $873M - LinkedIn https://www.linkedin.com/posts/solana_solanas-real-world-asset-rwa-ecosystem-activity-7412504516853563393-l-DV
[14] Solana Emerges as Contender In Real World Asset Tokenisation? https://blog.bitfinex.com/education/solana-emerges-as-contender-in-real-world-asset-tokenisation/
[15] Pierre-Alexandre Boulay's Post - LinkedIn https://www.linkedin.com/posts/boulay1_huge-milestone-solana-foundation-has-activity-7420718310536704000-vmOV
[16] ERC-3643 Permissioned Tokens | ERC3643 https://docs.erc3643.org/erc-3643
