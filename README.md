# PR Radar — instalação

App da barra do Mac que acompanha seus PRs e os do time no GitHub: status de review, CI, conflito, cycle time, respostas aos seus comentários e notificações.

## Antes de instalar

Você precisa do GitHub CLI logado na sua conta. O PR Radar usa o login dele, não pede senha nem token.

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

1. Clique na engrenagem e configure:
   - **Organizações do GitHub:** já vem com `capimbr`. Adicione outras da lista, se quiser.
   - **Pessoas acompanhadas:** logins do GitHub de quem você quer acompanhar na aba Time.
   - **Cycle time:** o prazo do seu time, contado a partir do primeiro commit do PR.
   - **Iniciar com o Mac:** para o radar abrir sozinho ao ligar o computador.
2. Clique em **Salvar**.

Permissões que o macOS vai pedir:

- **Notificações:** permita, para receber os avisos de aprovação, CI, comentários e respostas.

## O que cada aba mostra

- **Meus:** seus PRs abertos, do mais recente para o mais antigo. O trilho mostra Review, CI, Base e Merge, e a borda do card mostra o cycle time.
- **Time:** PRs das pessoas que você acompanha, agrupados por pessoa, mais os que pediram seu review.
- **Respostas:** PRs de outras pessoas em que alguém respondeu um comentário seu.
- **Notificações:** histórico de tudo que mudou.

## Problemas comuns

- **"Sem resposta do GitHub":** verifique a internet e se `gh auth status` está ok. O app tenta de novo sozinho a cada minuto.
- **Nenhum PR aparece:** confira se a organização certa está nas configurações e se sua conta tem acesso a ela.

## Desinstalar

Saia pelo menu do ícone do radar (botão direito → Sair do PR Radar) e apague o app da pasta Aplicativos.
