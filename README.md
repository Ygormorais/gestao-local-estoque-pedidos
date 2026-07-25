# Gestão Local — Estoque e Pedidos

Aplicação web criada para apoiar pequenos empreendedores no controle de produtos e no agendamento de encomendas. O sistema reúne informações de estoque, alerta quando um item precisa de reposição e acompanha prazos de entrega, reduzindo vendas de produtos esgotados e atrasos com clientes.

## Funcionalidades

- Painel com totais de produtos, itens a repor, valor do estoque, pedidos atrasados e valor agendado.
- Cadastro, consulta, busca, filtro e remoção de produtos.
- Status automático de estoque: **OK** ou **Repor**.
- Cadastro, consulta, busca, filtro e remoção de pedidos.
- Cálculo automático do valor de cada pedido.
- Status automático de pedidos: **Agendado**, **Entregue** ou **Atrasado**.
- Ação para marcar uma entrega como concluída ou reabrir um pedido.
- Interface responsiva para notebooks e tablets.
- Dados de demonstração carregados ao abrir.

## Como abrir e usar

1. Baixe ou clone este repositório.
2. Abra o arquivo `index.html` em qualquer navegador moderno.
3. Use os botões **Novo produto** e **Agendar pedido** para incluir registros.
4. Use a busca e os filtros para localizar informações rapidamente.

Não é necessário instalar programas, dependências ou iniciar um servidor. Os dados ficam somente na memória do navegador e voltam ao estado de demonstração quando a página é recarregada.

## Tecnologias

- HTML5
- CSS3
- JavaScript puro

Todo o sistema está contido em um único arquivo, sem bibliotecas externas, backend ou banco de dados.

## Publicar no GitHub

Com o Git instalado, abra um terminal nesta pasta e execute:

```bash
git init
git branch -M main
git add .
git commit -m "feat: adiciona sistema de gestão de estoque e pedidos"
```

Depois:

1. Acesse [github.com/new](https://github.com/new).
2. Crie um repositório vazio, sem adicionar README, `.gitignore` ou licença.
3. Copie a URL HTTPS fornecida pelo GitHub.
4. No terminal, conecte e envie o projeto:

```bash
git remote add origin https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git
git push -u origin main
```

Substitua `SEU-USUARIO` e `NOME-DO-REPOSITORIO` pelos dados do repositório criado.
