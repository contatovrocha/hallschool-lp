# Hall School: LP com quiz

Site estático (GitHub Pages) com quiz de captação para pais de crianças de 6 a 16 anos.

- `index.html`: quiz (idade, cursos, estado, se já faz curso, contato) seguido da landing page.
- `admin/`: painel de leads com login Google (Supabase Auth). Só e-mails cadastrados em `hallschool_admins` têm acesso.
- Leads vão para a tabela `hallschool_leads` do projeto Supabase "V8 OSS". A página só pode inserir dados, sem leitura pública (RLS).

## Liberar outro admin
No SQL Editor do Supabase:
```sql
insert into public.hallschool_admins(email) values ('novo.admin@gmail.com');
```
