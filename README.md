# Aprova 26 + Supabase

MVP de uma plataforma de preparação para o ENEM.

## 1. Criar o projeto Supabase
1. Crie um projeto em https://supabase.com
2. Abra **SQL Editor**
3. Cole e execute `supabase/schema.sql`

## 2. Configurar as variáveis
Copie:
```bash
cp .env.example .env.local
```
No painel do Supabase, abra **Project Settings > API** e preencha:
- `NEXT_PUBLIC_SUPABASE_URL`
- `NEXT_PUBLIC_SUPABASE_ANON_KEY`

Nunca coloque a `service_role` no front-end.

## 3. Rodar
```bash
npm install
npm run dev
```

Abra http://localhost:3000

## O que já funciona
- Cadastro e login com Supabase Auth
- Perfil automático ao criar usuário
- RLS para proteger dados individuais
- Dashboard lendo dados reais
- Questões com registro de tentativa
- Redação salva no banco
- Estrutura para cronograma, sessões e simulados
- Layout responsivo

## Próximas etapas recomendadas
- Onboarding do aluno
- CRUD administrativo de questões
- Sistema adaptativo por taxa de erro
- Revisão espaçada
- Correção de redação por IA
- Simulados completos
- Upload de materiais no Supabase Storage
- Assinatura premium
- Deploy na Vercel


## Deploy na Vercel

No painel da Vercel, adicione estas variáveis de ambiente:

- `NEXT_PUBLIC_SUPABASE_URL`
- `NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY`

Depois faça o deploy. Não use `sb_secret_...` nem `service_role` no frontend.
