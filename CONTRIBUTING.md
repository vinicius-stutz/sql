<a id="topo"></a>

# Guia de Contribuição
Este documento estabelece as diretrizes e padrões de desenvolvimento para manter a consistência, qualidade e confiabilidade de todos os scripts do repositório.

<p align="right">(<a href="#topo">voltar ao topo</a>)</p>

## Padrões de Código e Documentação
Ao criar ou editar consultas, siga as seguintes práticas recomendadas:

### Padrões para SQL (Relacional)
- **Palavras-chave em maiúsculas**: Utilize sempre maiúsculas para palavras reservadas (`SELECT`, `INSERT`, `UPDATE`, `DELETE`, `FROM`, `WHERE`, `JOIN`, `MERGE`, etc.).
- **Identificadores**: Utilize nomenclatura clara e coerente. Prefira snake_case ou convenções nativas do SGBD específico.
- **Indentação**: Mantenha recuo consistente (4 espaços) para cláusulas subordinadas e subconsultas.
- **Transações seguras**: Scripts de alteração de dados (DML) devem conter blocos transacionais explícitos (`BEGIN TRANSACTION`, `COMMIT`, `ROLLBACK`) e validação de erros.
- **Compatibilidade**: Informe a versão mínima do SGBD quando o snippet depender de recurso específico (ex: `GENERATED ALWAYS AS IDENTITY` a partir do Oracle 12c).

### Padrões para NoSQL (MongoDB)
- Utilize comandos e operadores no padrão moderno suportado pelo driver/shell mais recente (`countDocuments` em vez do método depreciado `count()`, atualização via agregação quando cabível).
- Garanta formatação consistente em JSON/BSON com recuo de 2 ou 4 espaços.

### Padrões Gerais de Documentação Markdown
- Todos os arquivos devem estar codificados em UTF-8.
- Utilize blocos de código com a tag de linguagem apropriada (` ```sql `, ` ```json ` etc).
- Forneça explicações objetivas sobre o comportamento do código, efeitos colaterais e possíveis códigos de erro associados (ex: código de erro ORA).

<p align="right">(<a href="#topo">voltar ao topo</a>)</p>

## Processo de Envio (Pull Request)
1. Faça um Fork do repositório no GitHub.
2. Crie uma branch para sua alteração:
   ```bash
   git checkout -b feature/minha-nova-dica
   ```
3. Realize os commits utilizando mensagens claras no padrão Conventional Commits (ex: `docs: adicionar dica sobre CTE recursiva no SQL Server`).
4. Valide a renderização do arquivo Markdown e execute a consulta em um banco de teste.
5. Envie a branch para o seu repositório remoto:
   ```bash
   git push origin feature/minha-nova-dica
   ```
6. Abra um Pull Request com destino à branch principal.
7. Preencha a descrição do Pull Request informando o SGBD afetado, versão testada e a motivação do snippet.

<p align="right">(<a href="#topo">voltar ao topo</a>)</p>
