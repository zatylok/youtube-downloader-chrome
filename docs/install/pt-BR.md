# Instalar o VidoZavr 1.2.60

**[Русский](ru.md) · [English](en.md) · [Deutsch](de.md) · [Español](es.md) · [Português do Brasil](pt-BR.md)**

Todas as funções são gratuitas: vídeos do YouTube, Shorts, canais, playlists,
transmissões ao vivo, recorte e gerenciamento de downloads. O processamento é local.
Você precisa de **Windows 11 x64, Chrome 127+ e Internet na primeira instalação**.
Não precisa de Python, Rust nem Node.js. O componente Windows conecta o Chrome às
ferramentas locais por Native Messaging. **A extensão sozinha não basta.**

## Instalação recomendada: nove passos

1. **Baixe [VidoZavr.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr.exe).**
   Não é preciso baixar o ZIP também. Use a versão oficial e compare
   o [SHA-256](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/SHA256SUMS.txt).
2. **Execute o EXE e instale os componentes Windows.** O Setup está em russo:
   **Далее = Avançar**, **Готово = Concluir**. Aguarde **Компоненты Windows установлены**
   (componentes Windows instalados). As ferramentas fixadas que faltam são baixadas e
   verificadas; arquivos válidos já instalados são reutilizados. O Setup não abre
   o Chrome nem testa uma conexão ativa com o navegador.
3. **Leia a última tela antes de fechá-la.** O campo de caminho mostra a pasta permanente
   da extensão. **Папка расширения = Pasta da extensão** abre essa pasta;
   **Инструкция = Instruções** abre o guia instalado. Guarde o caminho exato para o passo 7.
4. **Abra `chrome://extensions`** no perfil do Chrome que você usa para o YouTube.
   Digite na barra de endereços: é uma página interna, não um site.
5. Ative o **Modo do desenvolvedor** no canto superior direito.
6. Clique em **Carregar sem compactação**. O seletor de pastas do Windows será aberto.
7. **Selecione exatamente a pasta instalada `extension` do passo 3.**
   Navegue até ela ou cole o caminho exato do Setup no campo **Pasta** e confirme
   com **Selecionar pasta** (Windows em russo: **Папка**, **Выбор папки**).
   O arquivo `manifest.json` deve estar diretamente dentro dela. Selecione a pasta,
   não o arquivo, Downloads, a pasta superior da instalação nem um ZIP.
8. **Confira um único cartão V1D0Z@VR 🦖 ativado**, versão **1.2.60**.
   No modo do desenvolvedor, o ID é `bkihgeeibbodemeibfdcglojjkiepnlf`.
9. **Abra o menu Extensões do Chrome, com o ícone de peça de quebra-cabeça → V1D0Z@VR.**
   Procure **Downloader connected** se a extensão estiver em inglês, ou **Загрузчик подключён**
   em russo: significa “componente de download conectado”. Você pode fixar o ícone.
   Só o cartão não comprova a conexão Native.

Pasta padrão:

`%LOCALAPPDATA%\Programs\YouTube Video & Shorts Downloader\extension`

**Uma instalação personalizada pode usar outro caminho. O caminho exato mostrado
na última tela do Setup é a referência.** Mantenha essa pasta permanente e o modo
do desenvolvedor ativado. Se você já fechou o Setup, as instruções estão no menu
Iniciar; use a pasta escolhida na instalação e sua subpasta `extension`.

### Identificar os controles

A captura está em **inglês**: **1 Developer mode = Modo do desenvolvedor**,
**2 Load unpacked = Carregar sem compactação**. Chromium 149 real, sem janela visível;
a captura exclui a área sem uso.

![Controles em inglês com os números 1 e 2](images/chrome-controls-en.png)

O cartão real mostra nome, versão, ID e interruptor ativado.

![Cartão do VidoZavr no Chromium em inglês](images/extension-card-en.png)

<details>
<summary>Exemplo de conexão confirmada (interface russa)</summary>

**1** indica “Загрузчик подключён”, equivalente a “componente de download conectado”.
A imagem existente mostra uma resposta Native real e isolada, não um novo teste de
instalação manual.

![Conexão Native verificada no menu real](images/connected.png)

</details>

As imagens são de perfis isolados do **Chromium 149 sem janela visível**, não do
Chrome 156 nem de uma instalação limpa do Windows. O cartão é uma ilustração;
a [imagem completa original](images/chrome-extensions.png) foi mantida.
Não há imagens simuladas da conclusão do Setup ou do seletor de pastas.

## Outras opções

- **Avançada — [VidoZavr-Extension.zip](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Extension.zip):**
  instale o componente Windows com o EXE recomendado, extraia o ZIP para uma pasta
  permanente independente e carregue essa pasta **no lugar** da cópia gerenciada.
  O Chrome não carrega um ZIP diretamente. O Setup e as atualizações assinadas não
  mantêm essa cópia: substitua os arquivos com o ZIP oficial correspondente e recarregue
  o cartão existente. Não carregue as duas cópias.
- **Beta/Experimental — [VidoZavr-Experimental.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Experimental.exe):**
  tenta conectar o Chrome automaticamente usando a mesma instalação Windows.
  Pode exigir modo do desenvolvedor, seleção de perfil ou decisões sobre permissões;
  outras extensões podem interromper o processo. Não há garantia de sucesso ou execução
  totalmente automática. A verificação em Windows limpo está incompleta.
  Leia as [limitações](EXPERIMENTAL.md).

## Segurança e ferramentas baixadas

Os EXE **não têm assinatura Windows Authenticode**. O SmartScreen pode mostrar um
fornecedor desconhecido. Confira a fonte oficial e o hash; cancele se houver dúvida.
Não desative proteções. Verificação opcional: `Get-FileHash .\VidoZavr.exe -Algorithm SHA256`.

O Setup obtém yt-dlp **2026.10.21**, Deno **2.9.8** e FFmpeg/FFprobe **9.0.2**, compilação
Windows de Gyan Doshi, diretamente dos fornecedores fixados, verificando tamanho/SHA-256.
Esses EXE de terceiros não estão incluídos nos nossos downloads. A primeira instalação
não é totalmente offline. [Componentes, fontes, licenças e hashes](COMPONENTS.md).
**A assinatura Ed25519 das atualizações é diferente da assinatura do instalador Windows.**

## Atualizar e desinstalar

As atualizações assinadas mantêm a pasta instalada e aguardam enquanto houver trabalho
de mídia protegido. Se o Chrome ainda mostrar uma versão antiga depois disso, clique
em **Recarregar** no cartão existente de `chrome://extensions` e atualize as abas do
YouTube. Preserve o cartão e suas preferências; a ativação automática não é garantida
em todas as versões do Chrome. Pastas ZIP independentes precisam de atualização manual.

Para reparar, execute o Setup após terminar o trabalho e siga os avisos sobre arquivos
em uso. Preserve tarefas pausadas e arquivos parciais.
Desinstale em **Configurações do Windows → Aplicativos → V1D0Z@VR → Desinstalar**;
depois remova o cartão do Chrome. Os vídeos, `native\data` e `.updates` permanecem.
Remover o cartão pode apagar as configurações salvas no navegador.

## Solução de problemas

| Problema | Ação suportada |
|---|---|
| Manifesto ausente / não foi possível carregar | Repita Carregar sem compactação e selecione exatamente `extension` com `manifest.json` dentro. Downloads, a pasta superior e o ZIP não servem. |
| Cartão presente, componente desconectado | Confira o componente Windows para **o mesmo usuário do Windows**, o perfil do Chrome e a pasta exata. `Check.cmd` na instalação verifica arquivos/registro; o menu verifica a conexão ativa. Se necessário, repare com o Setup após terminar o trabalho. |
| Modo do desenvolvedor desativado | Ative-o no perfil correto, mantenha-o ligado e confira se o cartão existente está ativado. |
| Perfil errado ou cópias duplicadas | Identifique o perfil usado e a pasta permanente escolhida. Não adicione outra cópia para reparar a conexão; remover um cartão pode apagar suas preferências. |
| Atualização concluída, versão antiga no Chrome | Após o trabalho protegido terminar, recarregue o **cartão existente** e as abas do YouTube. Não apague dados pausados. |
| Rede, rotas VPN ou falha de download/hash | Verifique a conexão do componente de download, além do Chrome. O túnel dividido pode usar rotas distintas. Tente a fonte oficial novamente; não troque por espelhos, altere hashes nem desative proteções. |
| Aviso do SmartScreen | O instalador não é assinado. Confira fonte e soma; cancele se houver dúvida. |
| Experimental bloqueado por outra extensão | Não aceite solicitações alheias às cegas nem desative outras extensões. Feche seu Setup normalmente e use a instalação manual recomendada. |

Ajuda: [GitHub Issues](https://github.com/zatylok/youtube-downloader-chrome/issues) ou
[@zatylok007](https://t.me/zatylok007). Informe versão, erro exato e passos curtos;
nunca envie cookies, tokens nem perfis privados.
[Permissões e privacidade](../../README.md#windows-warnings-permissions-and-privacy) ·
[Opções e idiomas](README.md)
