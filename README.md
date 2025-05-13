# Projeto-de-An-lise-de-Logs-com-PySpark

### **Tabela de Progresso: Projeto de Análise de Logs com PySpark**

| Fase        | Tarefa                                  | Status         | Dependências Principais                     | Habilidades Chave (Curso)        | Observações                                    |
| :---------- | :-------------------------------------- | :------------- | :------------------------------------------ | :------------------------------- | :--------------------------------------------- |
| **Fase 1**  | **Preparação e Fundamentos**            |                |                                             |                                  |                                                |
|             | 1.1 Concluir Seção 4 (Spark SQL)        | Não Iniciado   | Tempo de estudo                             | Spark SQL (Core)                 | **Prioridade Máxima**                          |
|             | 1.2 Obter/Gerar Dados de Log            | Não Iniciado   | Decisão (Simular vs. Real)                  | (Python Scripting se gerar)      | Definir formato (ex: Combined Log Format)      |
|             | 1.3 Confirmar Ambiente PySpark          | *Concluído?*   | Instalação PySpark                          | Seção 2                          | Verificar `SparkSession`                       |
| **Fase 2**  | **Ingestão e Parsing dos Logs**         |                |                                             |                                  |                                                |
|             | 2.1 Carregar Logs Brutos (`.text`)      | Não Iniciado   | Fase 1.2, Fase 1.3                          | Seção 3 (Leitura básica)         | DataFrame com coluna "value"                   |
|             | 2.2 Definir Padrão Regex                | Não Iniciado   | Fase 1.2 (Formato do log)                   | Regex                            | Testar regex separadamente                     |
|             | 2.3 Aplicar Parsing (`regexp_extract`)  | Não Iniciado   | Fase 1.1, Fase 2.1, Fase 2.2                | Seção 4 (Funções String SQL)     | Criar colunas para cada campo                  |
|             | 2.4 Limpeza e Conversão de Tipos        | Não Iniciado   | Fase 2.3                                    | Seção 4 (Cast, Funções Data/Hora) | Tratar nulos, converter timestamp, int, etc. |
| **Fase 3**  | **Análise com Spark SQL**               |                |                                             |                                  |                                                |
|             | 3.1 Realizar Análises Principais        | Não Iniciado   | Fase 2.4                                    | Seção 4 (GROUP BY, WHERE, Agg)   | Horários pico, Top URLs, Erros, User Agents... |
|             |   *  - Horários de Pico                 | Não Iniciado   | Fase 2.4                                    | Spark SQL                        | `hour(timestamp)`                              |
|             |   *  - Páginas Mais Acessadas           | Não Iniciado   | Fase 2.4                                    | Spark SQL                        | `GROUP BY url`                                 |
|             |   *  - Erros Frequentes                 | Não Iniciado   | Fase 2.4                                    | Spark SQL                        | `WHERE status >= 400`                          |
|             |   *  - Análise User Agent               | Não Iniciado   | Fase 2.4                                    | Spark SQL                        | `GROUP BY user_agent`                          |
|             |   *  - Detecção Bots (Simples)          | Não Iniciado   | Fase 2.4                                    | Spark SQL                        | `GROUP BY ip_address`                          |
| **Fase 4**  | **Enriquecimento (Opcional)**           |                |                                             |                                  |                                                |
|             | 4.1 Estudar Seção 5 (Outras Fontes)     | Não Iniciado   | Interesse em Geolocalização                 | Seção 5                          | Focar em leitura CSV/JSON                      |
|             | 4.2 Obter Banco de Dados GeoIP          | Não Iniciado   | Decisão de fazer Fase 4                     | -                                | Ex: GeoLite2 (MaxMind)                         |
|             | 4.3 Carregar Dados GeoIP                | Não Iniciado   | Fase 4.1, Fase 4.2                          | Seção 5 (Leitura CSV/etc.)       | Criar `geo_df`                                 |
|             | 4.4 Implementar Geolocalização (JOIN)   | Não Iniciado   | Fase 2.4, Fase 4.3                          | Seção 4 (JOIN), Seção 5          | Juntar `logs_df` com `geo_df` pelo IP          |
|             | 4.5 Análises Geográficas                | Não Iniciado   | Fase 4.4                                    | Seção 4 (GROUP BY)               | Contagem por país/cidade                       |
| **Fase 5**  | **Finalização e Documentação**          |                |                                             |                                  |                                                |
|             | 5.1 Salvar Resultados Analíticos        | Não Iniciado   | Fase 3 (e Fase 4 se feita)                  | Seção 3/5 (Escrita de dados)     | Formato Parquet ou CSV                         |
|             | 5.2 Organizar e Refatorar Código        | Não Iniciado   | Código das Fases 2, 3, 4                    | -                                | Clareza, comentários, funções                  |
|             | 5.3 Criar Documentação (README.md)      | Não Iniciado   | Projeto funcional (Fases 1-3/4), Fase 5.1/5.2 | -                                | Descrição, como rodar, resultados, GitHub      |

**Status Possíveis:**

*   **Não Iniciado:** A tarefa ainda não começou.
*   **Em Andamento:** A tarefa foi iniciada, mas não concluída.
*   **Concluído:** A tarefa foi finalizada com sucesso.
*   **Bloqueado:** A tarefa não pode progredir devido a um impedimento.
*   **Opcional/Não Aplicável:** A tarefa pode ser pulada ou não se aplica ao escopo final decidido.
