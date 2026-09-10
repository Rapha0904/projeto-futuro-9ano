# Projeto Futuro — 9º Ano

Sistema interativo para a experiência dos 9º anos.

## Estrutura do GitHub

- `index.html` → site dos alunos
- `admin/index.html` → painel administrativo
- `firebase/firestore.rules` → regras do Firestore

## Recursos desta versão

- Firebase Authentication anônimo para alunos, sem login visível;
- seleção de turma carregada do Firestore;
- 12 perguntas;
- resultado calculado e salvo automaticamente;
- uma participação por UID anônimo persistido no navegador;
- bloqueio de nova criação de resultado/resposta pelo mesmo UID;
- painel administrativo com Firestore em tempo real (`onSnapshot`);
- cadastro, ativação, desativação e exclusão de turmas;
- relatório visual em PNG;
- exportação dos dados brutos para Excel.

## Publicação no GitHub Pages

1. Envie o conteúdo desta pasta para a raiz do repositório.
2. GitHub → Settings → Pages.
3. Source: Deploy from a branch.
4. Branch: `main`.
5. Folder: `/ (root)`.
6. Save.

Site do aluno:
`https://rapha0904.github.io/projeto-futuro-9ano/`

Painel:
`https://rapha0904.github.io/projeto-futuro-9ano/admin/`

## Firebase

As regras em `firebase/firestore.rules` precisam ser publicadas em:
Firestore Database → Regras.

Authentication deve ter:
- E-mail/senha ativado;
- Anônimo ativado.

Não é necessário criar manualmente as coleções `turmas`, `respostas` ou `resultados`.

## Observação sobre repetição

O bloqueio é feito sem coletar nome, e-mail ou telefone dos alunos. O navegador recebe uma identidade anônima do Firebase e o resultado usa esse UID como ID do documento. Limpar os dados do navegador, usar outro navegador/dispositivo ou perder a identidade anônima pode gerar um novo UID.
