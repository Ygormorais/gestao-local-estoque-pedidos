Leia o arquivo PROJETO.md em anexo — ele contém a especificação completa de um sistema de gestão para pequenos empreendedores (controle de estoque + agendamento de pedidos).

Construa o projeto a partir dessa especificação, seguindo exatamente os campos, módulos e regras descritas nela. Requisitos para a entrega:

1. Gere um único arquivo `index.html` autocontido (HTML + CSS + JavaScript no mesmo arquivo), sem dependências externas, sem necessidade de build step, funcionando ao abrir direto no navegador.
2. Popule o sistema com os dados de exemplo listados no PROJETO.md (tabelas de estoque e pedidos), para que o sistema já apareça funcionando com dados reais ao abrir.
3. Implemente os cálculos automáticos descritos: status "Repor"/"OK" no estoque, status "Agendado"/"Entregue"/"Atrasado" nos pedidos, e os totais do painel-resumo.
4. Aplique a identidade visual sugerida no documento (cor primária azul #2F5496, cards brancos com bordas arredondadas, badges coloridos de status).
5. Depois de gerar o código, monte a estrutura de um repositório Git pronto para subir no GitHub:
   - `index.html` (o sistema)
   - `README.md` — com o título do projeto, uma descrição curta do problema que ele resolve (baseada no contexto do PROJETO.md), como abrir/usar o sistema, e as tecnologias usadas
   - `.gitignore` básico (se fizer sentido para o stack escolhido)
6. Me devolva também a sequência de comandos Git para inicializar o repositório localmente e subir para o GitHub (`git init`, `git add`, `git commit`, instruções para criar o repositório remoto e `git push`), assumindo que ainda não criei o repositório no GitHub.

Não adicione autenticação, backend ou banco de dados — os dados devem viver em memória no próprio JavaScript, conforme especificado no PROJETO.md.
