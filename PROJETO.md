# Sistema de Gestão para Pequenos Empreendedores

Sistema web simples para controle de estoque e agendamento de pedidos, voltado a uma associação de pequenos empreendedores locais (artesãos, produtores de alimentos caseiros, prestadores de serviço informais).

## Contexto do projeto

Trabalho de extensão universitária (curso de Análise e Desenvolvimento de Sistemas). O sistema resolve dois problemas reais identificados junto a um grupo de microempreendedores:

1. Falta de controle confiável sobre a quantidade de produtos em estoque, gerando vendas de itens esgotados ou acúmulo desnecessário de mercadoria.
2. Falta de um sistema de agendamento de pedidos, gerando atrasos de entrega e perda de confiança dos clientes.

## Objetivo técnico

Construir uma aplicação web funcional, de fácil uso para pessoas com pouca familiaridade com tecnologia, que centralize:

- Cadastro e consulta de produtos em estoque, por empreendedor(a).
- Alerta automático de reposição quando a quantidade em estoque atinge o mínimo definido.
- Cadastro de pedidos/encomendas, vinculados a um produto e a uma data de entrega.
- Indicação automática de status do pedido (agendado / entregue / atrasado).
- Um painel/resumo com totais (itens cadastrados, itens a repor, valor total em estoque, pedidos atrasados, valor total agendado).

## Módulos

### 1. Controle de Estoque

Campos por produto:
- Código (gerado automaticamente, ex: EST001)
- Nome do produto
- Nome do(a) empreendedor(a) responsável
- Categoria (ex: Artesanato, Alimentos, Cosméticos, Decoração, Acessórios)
- Quantidade em estoque
- Estoque mínimo (limite que dispara alerta de reposição)
- Preço unitário (R$)
- Status (calculado: "Repor" se quantidade ≤ mínimo, senão "OK")

Ações: cadastrar novo produto, listar todos, remover produto.

### 2. Agendamento de Pedidos

Campos por pedido:
- Código do pedido (gerado automaticamente, ex: PED001)
- Nome do cliente
- Produto (selecionado a partir do estoque cadastrado)
- Quantidade
- Data do pedido
- Data de entrega prevista
- Status (Agendado / Entregue / Atrasado — "Atrasado" quando a data de entrega já passou e o pedido não foi marcado como entregue)
- Valor total (calculado automaticamente: quantidade × preço unitário do produto vinculado)

Ações: agendar novo pedido, listar todos, remover pedido.

## Requisitos não funcionais

- Interface simples e objetiva, pensada para usuários leigos em tecnologia.
- Não é necessário login/autenticação nesta versão.
- Não é necessário backend/banco de dados nesta versão — os dados podem viver em memória (estado da aplicação), sendo aceitável perder os dados ao recarregar a página.
- Responsivo o suficiente para uso em notebook e tablet.
- Sem dependências externas complexas — priorizar HTML/CSS/JavaScript puro, ou um framework leve caso o ambiente já utilize um (ex: React), mas sem necessidade de build step complicado.

## Identidade visual sugerida

- Cor primária: azul (#2F5496)
- Cards brancos com bordas suaves arredondadas
- Selos/badges coloridos para status (verde = OK/Entregue, vermelho = Repor/Atrasado, amarelo = Agendado)
- Tipografia simples, sem serifa

## Dados de exemplo para popular o sistema

**Estoque:**
| Código | Produto | Empreendedor(a) | Categoria | Qtd. | Mínimo | Preço |
|---|---|---|---|---|---|---|
| EST001 | Bolsa artesanal de crochê | Maria Silva | Artesanato | 12 | 5 | R$ 45,00 |
| EST002 | Doce caseiro (caixa 10un) | Joana Pereira | Alimentos | 3 | 8 | R$ 18,50 |
| EST003 | Sabonete artesanal | Ana Costa | Cosméticos | 25 | 10 | R$ 12,00 |
| EST004 | Vela aromática | Ana Costa | Decoração | 7 | 6 | R$ 22,00 |
| EST005 | Bijuteria em resina | Carla Souza | Acessórios | 2 | 5 | R$ 15,00 |

**Pedidos:**
| Código | Cliente | Produto | Qtd. | Data pedido | Data entrega | Status |
|---|---|---|---|---|---|---|
| PED001 | Fernanda Lima | EST001 | 2 | 05/08/2026 | 12/08/2026 | Entregue |
| PED002 | Roberto Alves | EST002 | 5 | 06/08/2026 | 08/08/2026 | Entregue |
| PED003 | Patrícia Nunes | EST003 | 10 | 10/08/2026 | 15/08/2026 | Agendado |

## Entregável esperado

Um único arquivo (ou projeto pequeno) que possa ser aberto direto no navegador, demonstrando visualmente os dois módulos funcionando com os dados de exemplo acima, incluindo os cálculos automáticos de status e totais.
