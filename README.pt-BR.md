# PhotoCraft — documentação em português do Brasil (pt-BR)

**Edição de imagens; uma reimplementação open-source e clean-room do Adobe Photoshop, reconstruída em Rust puro.**

Feito em Rust puro, funciona nativamente em macOS, Windows e Linux e também no navegador via WebAssembly.

## Recursos

- Round-trip fiel: abrir e re-salvar um documento reproduz o mesmo resultado para 307 de 309 arquivos do conjunto de teste psd-tools; blocos não modelados são preservados, não descartados.
- Pixels que batem: um oráculo de composição compara a renderização com a imagem mesclada do próprio Photoshop.
- Documentos grandes: PSB, arquivos de 16 e 32 bits e CMYK/Lab abrem nativamente.
- Dois compositores (CPU como referência e wgpu na GPU), testados um contra o outro; tiles 256² com copy-on-write para undo barato.

## Português do Brasil

Este fork detecta automaticamente pt-BR pelo locale do sistema (LANG/LC_ALL) — sem configuração extra.

O catálogo pt-BR foi aceito no upstream (PR #637, fechado; catálogo #700 mergeado; correções de rótulos no PR #833).

## A suíte ArtCraft

A ArtCraft é um conjunto de 7 aplicativos open-source que reimplementam, de forma clean-room e em Rust puro, as ferramentas de criação da Adobe — nativos para macOS, Windows e Linux, com a mesma interface no navegador via WebAssembly:

| Aplicativo | Propósito | Reimplementação de |
|---|---|---|
| PhotoCraft | Edição de imagens | Adobe Photoshop |
| FilmCraft | Edição de vídeo, cor e som | Adobe Premiere Pro |
| LightCraft | Biblioteca de fotos e revelação RAW | Adobe Lightroom |
| EffectCraft | Motion graphics e efeitos visuais | Adobe After Effects |
| PrintCraft | Workbench de PDF | Adobe Acrobat |
| DesignCraft | Layout de página e publicação | Adobe InDesign |
| VectorCraft | Ilustração vetorial | Adobe Illustrator |

- Site: <https://getartcraft.com> · Discord: <https://discord.gg/artcraft>

## Este fork

Adiciona **leitura desta documentação em português do Brasil** e, no código, a **tradução pt-BR da interface** — sem alterar nada do comportamento do aplicativo original.


## Instalar no Linux (x86_64)

Baixe o tarball da release e extraia (sem precisar de sudo):

```bash
wget https://github.com/storytold/photocraft/releases/download/v0.3.0/photocraft-0.3.0-linux-x86_64.tar.gz
mkdir -p ~/Programas/photocraft
tar -xzf photocraft-0.3.0-linux-x86_64.tar.gz -C ~/Programas/photocraft --strip-components=1
~/Programas/photocraft/bin/photocraft
```

> Consulte a página de releases do repositório upstream para a versão e o nome do asset atuais.

## Compilar do código

```bash
git clone https://github.com/storytold/<repositorio-upstream>.git
cd <repositorio-upstream>
# (opcional, para as fontes CJK do release) export CRAFT_FONTS_DIR=~/craft-fonts CRAFT_FONTS_REQUIRED=1
cargo build --release
```

## Comunidade

Suporte, feedback e novidades da suíte no Discord: <https://discord.gg/artcraft>.

---

Documentação original (inglês): [`README.md`](README.md).

