#git/ssh #pkm
# Autenticação-ssh

Esse erro está relacionado à chave do SSH, ele não consegue autenticar você. Para usar a chave pública do GitHub precisa configurar no seu pc

Vamos configurar no passo a passo abaixo (antes pode verificar no perfil do github se a chave de fato existe)

`ssh-keygen -t ed25519 -C "your_email@example.com"`
Deve receber a mensagem
`not authenticated`

Seguir o passo a passo abaixo inserindo comando por comando. No final deve gerar o SHA252 card (imagem ilustrativa)

```text

+------------[ED25519 256]-------------+
|  sdsfa.sd.f .            .           |
| sdfsas.df+....+    .  ..             |
|. * O+k.k.....       .    ..          |
| +..................     ..     ..    |
|.........dd..........                 |
|   .00..........-.-                   |
|  .ttt.......... . . .                |
|   . ........x.    ..                 |
|      .      .. ss..ssssst            |
+---------------[SHA256]---------------+

```


`ssh-add -l -E sha256`

`ssh-keygen -t ed25519 -C "seuemail@gmail.com"`

Copie a chave pública ssh para a sua área de transferência

`cat ~/.ssh/id_ed25519.pub | clip`

Na parte superior direita do seu perfil do Github, clique na sua imagem de perfil e depois clique em `Settings`

Na seção `Acess` no submenu a esquerda, clique em `SSH and GPG keys`

Clique em `New SSH key`

No campo `Title`, adicione um título descritivo para a nova chave. Por exemplo, se estiver usando um  *notebook* ou computador, pode adicionar como título "Notebook (nome do notebook)" ou "Computador pessoal (nome do computador)". Para adicionar/encontrar o nome do dispositivo no windows aperte o botão *windows* e digite nome do dispositivo.

Selecione o tipo da chave (na maior parte das vezes autenticação).

No campo `Key` , cole a chave que copiamos por comando nos passos anteriores.

Clique em `Add SSH key`

Um símbolo de chave na cor amarela deve aparecer após atualizar a página.