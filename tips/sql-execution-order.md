# Ordem de execução das consultas SQL
Guia visual e lógico detalhando a sequência exata de execução interna das cláusulas em consultas SQL.

1. Source
2. `FROM` e `JOIN`
3. Merged
4. `WHERE`
5. Filtered
6. `GROUP BY`
7. Grouped
8. `HAVING`
9. Filtered
10. `SELECT`
11. Selected (*projeção*)
12. `ORDER BY`
13. Ordered
14. `LIMIT` e `OFFSET`
15. Limited

```mermaid
flowchart TD
    A[1. Source] --> B["2. FROM & JOIN"]
    B --> C[3. Merged]
    C --> D["4. WHERE"]
    D --> E[5. Filtered]
    E --> F["6. GROUP BY"]
    F --> G[7. Grouped]
    G --> H["8. HAVING"]
    H --> I[9. Filtered]
    I --> J["10. SELECT"]
    J --> K["11. Selected (projeção)"]
    K --> L["12. ORDER BY"]
    L --> M[13. Ordered]
    M --> N["14. LIMIT & OFFSET"]
    N --> O[15. Limited]
```
