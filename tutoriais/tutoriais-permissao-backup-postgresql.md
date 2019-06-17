# Dando permissão de backup a um usuário PostgreSQL

## Neste simples tutorial aprenderemos como dar permissão de backup a um usuário no PostgreSQL.

> Não me responsabilizo se por acaso você não saiba o que está fazendo.  
> Sugiro você dár uma estudada antes.

Primeiro vamos listar as tabelas e sequencias do banco de dados que entrarão no backup

```sql
select 'grant select on table ' || tablename || ' to dumpuser;'
from pg_tables
where schemaname = 'public'
```

```sql
select 'grant select on sequence ' || relname || ' to dumpuser;'
from pg_class
where relkind = 'S'
```

Salvamos o resultado das consultas anteriores em arquivos `.sql`

Agora abrimos cada um dos arquivos script salvos e rodamos os comandos ‘grant’`.`





