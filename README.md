# Projeto Futuro — V6 FINAL

Arquivos prontos para GitHub Pages:
- `index.html` — experiência do 9º ano, enquadrada para tela/projetor.
- `admin/index.html` — painel administrativo.
- `firebase/firestore.rules` — regras do Firestore.
- `README.md`.

## Acesso
O administrador principal é `raphael122362@gmail.com`.

Somente o administrador principal pode:
- criar/remover/revogar acessos;
- criar, ativar/desativar e excluir turmas.

Coordenação:
- consulta resultados ao vivo;
- acompanha resultados por turma;
- gera relatório PNG;
- exporta Excel;
- não altera turmas nem acessos.

Para liberar uma pessoa:
1. crie a conta dela em Firebase Authentication → Usuários, usando e-mail e senha;
2. entre no `/admin/` com o administrador principal;
3. abra `Usuários autorizados`;
4. informe exatamente o mesmo e-mail;
5. escolha `Coordenação` ou `Administrador`;
6. clique em `Autorizar acesso`.

A conta passa a ser autorizada imediatamente.

## Publicação
Suba os arquivos mantendo esta estrutura:
```
index.html
admin/index.html
firebase/firestore.rules
README.md
```

Depois publique `firebase/firestore.rules` no Firebase Console → Firestore Database → Rules.

Cada usuário autorizado pode ler apenas o próprio registro `admins/{email}` para validar seu perfil; somente o administrador principal pode criar, alterar ou revogar acessos.
