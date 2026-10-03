```text
    _ _____ _ 
   | |_____| |    ____   ___  _        ____        _                  _       
   | |     | |   / ___| / _ \| |      / ___| _ __ (_)_ __  _ __   ___| |_ ___ 
   | |_____| |   \___ \| | | | |      \___ \| '_ \| | '_ \| '_ \ / _ \ __/ __|
   | |     | |    ___) | |_| | |___    ___) | | | | | |_) | |_) |  __/ |_\__ \
   | |_____| |   |____/ \__\_\_____|  |____/|_| |_|_| .__/| .__/ \___|\__|___/
   | |     | |                                      |_|   |_|                 
   '-'-----'-'   [ Banco de Dados & Snippets de Consultas ]
```

<a id="topo"></a>

<h1 align="center">SQL Snippets</h1>

<p align="center">
  Repositório de consultas de referência, boas práticas, otimização e scripts para SGBDs relacionais e NoSQL.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/language-SQL%20%7C%20NoSQL-steelblue" alt="Linguagem" /> <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-green" alt="Licença" /></a> <a href="https://github.com/vinicius-stutz" target="_blank"><img src="https://img.shields.io/github/followers/vinicius-stutz?label=follow&style=social" height="20" title="Siga-me!" alt="Siga-me!" /></a>
</p>

## Sobre o Projeto
Base de conhecimento técnico voltada para desenvolvedores, administradores de bancos de dados (DBAs) e engenheiros de dados. Reúne soluções consolidadas para cenários frequentes de manipulação, definição e monitoramento de dados.

### Propósito do projeto
Oferecer acesso rápido a instruções testadas e padronizadas, reduzindo o tempo despendido na busca por particularidades de sintaxe e comportamentos específicos de cada dialeto de banco de dados.

### Termos do domínio e seus significados
- **DDL (Data Definition Language)**: Comandos para estruturação de esquemas e tabelas (`CREATE`, `ALTER`, `DROP`).
- **DML (Data Manipulation Language)**: Comandos para alteração de dados gravados (`INSERT`, `UPDATE`, `DELETE`, `MERGE`).
- **DQL (Data Query Language)**: Comandos para leitura e projeção de dados (`SELECT`).
- **Coluna Identity**: Recurso de autoincremento gerenciado nativamente pelo banco de dados.
- **CTE (Common Table Expression)**: Tabela temporária nomeada, definida no escopo de uma única instrução de consulta.
- **V$SESSION**: Visão dinâmica de performance do Oracle que expõe dados das conexões e sessões ativas.
- **Aggregation Pipeline**: Estrutura do MongoDB para processamento e transformação de documentos em estágios encadeados.

<p align="right">(<a href="#topo">voltar ao topo</a>)</p>

## Dicas
- [Microsoft SQL Server](./tips/mssql.md)
- [MongoDB](./tips/mongo.md)
- [Ordem de execução SQL](./tips/sql-execution-order.md)
- [Oracle Database](./tips/oracle.md)

### Estrutura do repositório
```text
.
├── CODE_OF_CONDUCT.md          # Código de conduta para colaboradores
├── CONTRIBUTING.md             # Guia de contribuição e modelo de branching GitFlow
├── LICENSE                     # Licença MIT do projeto
├── README.md                   # Documentação principal e visão geral
├── SECURITY.md                 # Políticas e reporte de vulnerabilidades
└── tips/                       # Coleção de instruções técnicas
    ├── mongo.md                # Snippets e pipelines para MongoDB
    ├── mssql.md                # Scripts transacionais e consultas SQL Server
    ├── oracle.md               # Recursos de instrumentação Oracle
    ├── pgsql.md                # Recursos de instrumentação PostgreSQL (breve)
    └── sql-execution-order.md  # Sequência lógica e visual de execução do SQL
```

### Principais funcionalidades
- Demonstração comparativa das cláusulas `ALWAYS`, `BY DEFAULT` e `BY DEFAULT ON NULL` para colunas `IDENTITY` no Oracle.
- Monitoramento e identificação de rotinas em execução no Oracle via package `DBMS_APPLICATION_INFO` e leitura em `V$SESSION`.
- Padrões de scripts transacionais seguros no SQL Server com controle de rollback.
- Consultas utilizando cláusula `VALUES` isolada e operações atômicas com comando `MERGE` e auditoria via `OUTPUT`.
- Operações de ordenação, contagem e atualização massiva com expressões de substituição no MongoDB.
- Diagramação do fluxo lógico sequencial da ordem interna de execução de consultas SQL.

<p align="right">(<a href="#topo">voltar ao topo</a>)</p>

## Roadmap
- [ ] Insert com `RETURNING INTO` no Oracle
- [ ] `Lateral Join` com PostgreSQL
- [ ] Exemplos de consultas complexas com MongoDB

<p align="right">(<a href="#topo">voltar ao topo</a>)</p>

## Contribuindo
Contribuições são fundamentais para a evolução deste repositório. Para propor melhorias, novos scripts ou correções, consulte o nosso [Guia de Contribuição](CONTRIBUTING.md).

<p align="right">(<a href="#topo">voltar ao topo</a>)</p>

## Licença
Este projeto está distribuído sob a licença **MIT**. Para detalhes completos sobre direitos e permissões, consulte o arquivo [LICENSE](LICENSE).

<p align="right">(<a href="#topo">voltar ao topo</a>)</p>

## Contato
- **Responsável**: Vinícius Stutz
- **GitHub**: [@vinicius-stutz](https://github.com/vinicius-stutz)
- **Repositório**: [https://github.com/vinicius-stutz/sql](https://github.com/vinicius-stutz/sql)

## Referências
Principais Ferramentas e Documentações Oficiais:
- [Oracle Database](https://docs.oracle.com/en/database/)
- [Microsoft SQL Server](https://learn.microsoft.com/sql/sql-server/)
- [MongoDB](https://www.mongodb.com/docs/)
- [Mermaid.js](https://mermaid.js.org/)
- [Git](https://git-scm.com/doc)
- [Markdown](https://www.markdownguide.org/)

<p align="right">(<a href="#topo">voltar ao topo</a>)</p>
