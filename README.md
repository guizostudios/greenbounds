# greenbounds
Hackathon - desafio 2

# Contrato Inteligente Green Bounds para Empréstimos com Títulos Verdes

Este repositório contém contratos inteligentes desenvolvidos para o projeto "Green Bounds", que visa utilizar títulos verdes como garantia para empréstimos a ONGs ou empresas de pequenos produtores no setor de crédito de carbono. O projeto envolve a emissão de NFTs vinculados a esses títulos, que podem ser colocados como colateral por pessoas físicas interessadas em apoiar iniciativas sustentáveis.

## Visão Geral da Proposta

### Quem
- **Tesouro Direto**
- **Bancos e instituições financeiras**
- **Pessoas físicas**
- **Pequenos produtores**
- **Empresas privadas**
- **ONGs**

### Para
- **Utilizar títulos verdes como colateral para empréstimos a ONGs ou pequenos produtores no setor de crédito de carbono.**

### Como
- **Pessoas físicas podem deixar títulos como colateral para permitir que ONGs ou empresas façam empréstimos e invistam em soluções geradoras de receita com créditos de carbono no futuro.**
- **Cada projeto emite NFTs adquiridos com títulos do Tesouro, usados como colateral.**
- **Os investidores recebem o valor pago pelo NFT mais uma recompensa ao apoiar um projeto bem-sucedido.**
- **Os NFTs podem ser revendidos em um mercado secundário no marketplace.**

### Diferencial
- **Facilita o acesso ao crédito inicial para pequenos produtores e ONGs no setor de crédito de carbono.**
- **Pessoas e empresas podem apoiar regiões específicas ou entidades empresariais de maneira simples e sem burocracia.**
- **Estimula o cumprimento dos acordos, pois várias pessoas acreditam nas iniciativas.**

## Arquitetura do Contrato Inteligente

### Contrato GBContract
- **Funcionalidades:**
  - KYC (Conheça Seu Cliente) para aprovação de endereços.
  - Emissão e listagem de NFTs vinculados a títulos verdes.
  - Controle de saldos de empréstimos, datas de início e término de contratos.
  - Empréstimo de fundos para ONGs.
  - Repagamento de fundos por ONGs.
  - Retirada de garantias se ONGs não pagarem após o vencimento do contrato.
  - Reembolso de NFTs ao comprador se as ONGs pagarem com sucesso.

### Contrato GBERC721
- **Funcionalidades:**
  - Extensão do padrão ERC721 para NFTs vinculados a projetos verdes.
  - Atualização de dados do projeto (status, ativo).
  - Verificação de propriedade para garantir que apenas o proprietário do NFT possa atualizar os dados.

### Contrato GBMarketplace
- **Funcionalidades:**
  - Listagem, compra e cancelamento de NFTs no mercado.
  - Cálculos de comissões e pagamentos durante as transações.
  - Atualização de informações de NFT pelo proprietário ou por administradores.

## Como Funciona

1. **Listagem de NFTs:**
   - As ONGs listam seus NFTs no GBMarketplace.
   - Os NFTs são adquiridos por pessoas interessadas em ajudar o projeto.

2. **Empréstimos para ONGs:**
   - ONGs podem solicitar empréstimos, fornecendo esses NFTs como garantia.

3. **Pagamento e Recompensa:**
   - Se as ONGs pagarem o empréstimo corretamente, os investidores recebem de volta o valor pago pelos NFTs mais uma recompensa.
   - Em caso de não pagamento, os perdem têm direito à garantia.

4. **Reembolso e Revenda:**
   - Os investidores podem revender os NFTs no mercado secundário.

## Uso

1. **Deploy dos Contratos:**
   - Implante o contrato GBContract, GBERC721 e GBMarketplace.
   - Configure as permissões adequadas para o contrato GBMarketplace acessar e interagir com os outros contratos.

2. **Operações com NFTs:**
   - Listar NFTs no GBMarketplace.
   - Comprar NFTs no GBMarketplace.
   - Cancelar listagens no GBMarketplace.

3. **Empréstimos e Pagamentos:**
   - ONGs solicitam empréstimos usando títulos verdes como garantia.
   - Investidores recebem recompensas após o pagamento bem-sucedido pelas ONGs.
   - Em caso de não pagamento, os investidores recebem a garantia.

4. **Atualizações e Reembolsos:**
   - Proprietários ou administradores atualizam informações de NFTs, se necessário.
   - Reembolso de NFTs para compradores em caso de pagamento bem-sucedido.

