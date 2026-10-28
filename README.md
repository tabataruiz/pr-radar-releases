# PR Radar — instalação

App da barra do Mac que acompanha seus PRs e os do time no GitHub: status de review, CI, conflito, cycle time, respostas aos seus comentários, notificações e anúncio dos PRs para a guilda no Slack.

## Antes de instalar

O PR Radar usa o login do GitHub CLI (`gh`). Ele não pede senha nem token. Se você ainda não tem o `gh`, não precisa instalar antes: na primeira abertura o app confere e abre o Terminal para instalar pelo Homebrew e fazer login. Se preferir fazer à mão:

```bash
brew install gh
gh auth login
```

Para conferir: `gh auth status` deve mostrar sua conta logada.

## Instalar

1. Baixe o arquivo `PR-Radar_<versão>_universal.dmg` da [última versão](https://github.com/tabataruiz/pr-radar-releases/releases/latest).
2. Abra o DMG e arraste o **PR Radar** para a pasta **Aplicativos**.
3. Abra o PR Radar pela pasta Aplicativos. Na primeira vez, o macOS pergunta se você quer abrir um app baixado da internet: clique em **Abrir**.

O app é assinado e notarizado pela Apple, então funciona em Mac Intel e Apple Silicon com macOS 12 ou mais novo.

## Atualizações

Você só instala uma vez. Quando sai uma versão nova, aparece no topo do radar a faixa **"Versão X disponível"**: clique em **Atualizar e reiniciar** e o app se atualiza sozinho. O radar procura atualizações ao abrir e a cada 6 horas.

## Primeiro uso

O PR Radar não abre janela no Dock: ele aparece como um ícone de radar na barra do Mac, perto do relógio. Clique nele para abrir o painel.

Na primeira vez aparece a tela **Vamos configurar o PR Radar**, com o passo a passo:

1. **GitHub CLI e login:** se faltar algo, o botão abre o Terminal e o login termina no navegador.
2. **Organizações:** escolha onde o radar procura PRs. Nada vem pré-configurado.
3. **Pessoas do time (opcional):** logins do GitHub de quem você quer acompanhar na aba Time.
4. **Slack (opcional):** conecte para anunciar PRs na guilda direto do app.
5. Clique em **Começar a usar**.

Depois, tudo fica na engrenagem, onde também dá para ajustar o **cycle time** (o prazo do seu time, contado a partir do primeiro commit do PR), os **canais do Slack de cada repositório** e **Iniciar com o Mac**.

Permissões que o macOS vai pedir:

- **Notificações:** permita, para receber os avisos de aprovação, CI, comentários e respostas.

## O que cada aba mostra

- **Meus:** seus PRs abertos, do mais recente para o mais antigo. O trilho mostra Review, CI, Base e Merge, e a borda do card mostra o cycle time. Dá para atualizar a branch e mergear pelo card. Com mais de uma organização configurada, cada PR mostra um selo com a cor da organização.
- **Time:** PRs das pessoas que você acompanha, agrupados por pessoa, mais os que pediram seu review. Os filtros **Pediram meu review** e **Só sem aprovação** podem ser combinados.
- **Respostas:** PRs de outras pessoas em que alguém respondeu um comentário seu.
- **Notificações:** histórico de tudo que mudou.

## Anunciar na guilda

No megafone de um PR seu, o app monta a mensagem com o módulo e a descrição. Você edita o texto como quiser, pode incluir outros PRs seus na mesma mensagem e envia pelo Slack para os canais configurados para cada repositório, ou só copia a mensagem.

## Problemas comuns

- **"Sem resposta do GitHub":** verifique a internet e se `gh auth status` está ok. O app tenta de novo sozinho a cada minuto.
- **Nenhum PR aparece:** confira se a organização certa está nas configurações e se sua conta tem acesso a ela.

## Desinstalar

Saia pelo menu do ícone do radar (botão direito → Sair do PR Radar) e apague o app da pasta Aplicativos.
