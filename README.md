ï»¿# REA com provas

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![RefaêÂ§a com provas](guia/assets/banner.jpg)](https://inematds.github.io/rea-com-provas/guia/)

**ê°Å¸â¡Â§ê°Å¸â¡Â· [PortuguêÂªs](README.md) êÂ· ê°Å¸â¡Âºê°Å¸â¡Â¸ [English](README.en.md) êÂ· ê°Å¸â¡Âªê°Å¸â¡Â¸ [EspaêÂ±ol](README.es.md)**

> **A IA diz que entendeu o app. PeêÂ§a a prova.**

## O que êÂ©

O **REA com provas** êÂ© um kit aberto e gratuito para quem usa um agente de IA (Claude Code, Codex ou o harness dsh) para estudar um app e fazer a prêÂ³pria versêÂ£o. O problema: o agente diz que entendeu como o app funciona e inventa o que nêÂ£o viu. O kit traz 4 regras, 3 pedidos prontos (painel de agentes, reator de leads e site refeito) e um conferidor em Python que reprova o arquivo de provas quando falta prova. Para usar, vocêÂª precisa de Python 3 e de um agente de IA no terminal.

## ê°Å¸ââ Guia de uso

Guia completo (landing + passo a passo): **https://inematds.github.io/rea-com-provas/guia/**

> [!WARNING]
> **SeguranêÂ§a e licenêÂ§a.** Use sêÂ³ em **software seu** ou **open source cuja licenêÂ§a deixa
> estudar** (MIT, Apache-2.0, BSD, GPL, MPLê¢â¬Â¦). Estudar nêÂ£o êÂ© copiar: a sua versêÂ£o êÂ© escrita do
> zero, com seu nome, seus textos e seu visual. Rode o agente numa pasta separada, sem senhas,
> chaves ou dados de clientes. Detalhes em [REGRAS.md](REGRAS.md).

## As 4 regras

1. **Sempre peêÂ§a o arquivo de provas `provas.md`**: cada conclusêÂ£o com o arquivo/trecho que a prova, mais a seêÂ§êÂ£o "O que NêÆO deu para provar".
2. **Foco no cêÂ³digo do prêÂ³prio app**, nêÂ£o nas bibliotecas embutidas (mande ignorar `node_modules`, `vendor`, `site-packages`).
3. **SêÂ³ software seu ou open source que a licenêÂ§a deixa estudar.** Depois construa a SUA versêÂ£o, com seu nome e visual.
4. **Descreva o visual em detalhe** (cores, fontes, movimento) num brief de design.

## O que vem no kit

| Arquivo | Para que serve |
|---|---|
| [`REGRAS.md`](REGRAS.md) | As 4 regras e o aviso de seguranêÂ§a e licenêÂ§a |
| [`prompts/a-painel-de-agentes.md`](prompts/a-painel-de-agentes.md) | ConstruêÂ§êÂ£o A: painel com 6 agentes vivos para um negêÂ³cio + caixa de comando |
| [`prompts/b-reator-de-leads.md`](prompts/b-reator-de-leads.md) | ConstruêÂ§êÂ£o B: lead entra ê¢â â qualificar, responder, agendar, acompanhar ê¢â â comemora |
| [`prompts/c-site-refeito.md`](prompts/c-site-refeito.md) | ConstruêÂ§êÂ£o C: mapear o SEU site e refazer numa versêÂ£o premium |
| [`provas/MODELO-provas.md`](provas/MODELO-provas.md) | Formato do arquivo de provas |
| [`confere_provas.py`](confere_provas.py) | Conferidor: nota 0ê¢â¬â10, APROVADO/REPROVADO e o que falta |
| [`brief/MODELO-brief-design.md`](brief/MODELO-brief-design.md) | Brief de design com exemplo preenchido no padrêÂ£o INEMA |
| [`exemplos/`](exemplos/) | `provas-boa.md` (aprovada), `provas-ruim.md` (reprovada) e a rodada real |
| [`tests/`](tests/) | Testes do conferidor, sem internet |

O kit vem configurado com o INEMA como exemplo (brief no padrêÂ£o INEMA, rodada real no site inema.club). Troque os [colchetes] dos prompts e o brief pelo seu negêÂ³cio.

## O conferidor

```bash
python3 confere_provas.py provas.md          # relatêÂ³rio em texto
python3 confere_provas.py provas.md --json   # mesmo resultado em JSON
```

Reprova (cêÂ³digo de saêÂ­da 1) quando falta a seêÂ§êÂ£o "O que NêÆO deu para provar" (ou ela estêÂ¡ vazia),
quando uma conclusêÂ£o nêÂ£o cita arquivo/trecho, ou quando todas as referêÂªncias apontam para
bibliotecas (`node_modules`, `vendor`, `site-packages`ê¢â¬Â¦). Aprova com cêÂ³digo 0. NêÂ£o conseguiu ler: cêÂ³digo 2.
O conferidor checa o formato; abrir 2 ou 3 provas e ver se o trecho estêÂ¡ lêÂ¡ continua sendo com vocêÂª.

## O processo, do inêÂ­cio ao fim

Quem faz: ê°Å¸Â§Â  vocêÂª (com o agente aberto) êÂ· ê¢Å¡â¢ê¯Â¸Â script êÂ· ê°Å¸Â¤â agente de IA (Claude Code, Codex ou dsh)

| # | Passo | Comando | Quem |
|---|---|---|---|
| 1 | Baixar o kit e rodar os testes | `cd ~ && git clone https://github.com/inematds/rea-com-provas.git && cd rea-com-provas && python3 -m unittest discover tests` | ê¢Å¡â¢ê¯Â¸Â |
| 2 | (Opcional) Instalar REA + harness | guia https://inematds.github.io/rea-sem-travas/guia/ | ê°Å¸Â§Â  |
| 3 | Escolher o alvo e conferir a licenêÂ§a | `cat ~/estudo/app/LICENSE` | ê°Å¸Â§Â  |
| 4 | Preencher o brief de design | `cp brief/MODELO-brief-design.md ~/estudo/brief.md` | ê°Å¸Â§Â  |
| 5 | Colar uma construêÂ§êÂ£o de `prompts/` no agente (fase 1: estudar) | `cd ~/estudo && claude` (ou `codex`) | ê°Å¸Â§Â  ê¢â â ê°Å¸Â¤â |
| 6 | Agente entrega o `provas.md` e roda o conferidor atêÂ© APROVADO | `python3 ~/rea-com-provas/confere_provas.py provas.md` | ê°Å¸Â¤â + ê¢Å¡â¢ê¯Â¸Â |
| 7 | Conferir 2 ou 3 provas êÂ  mêÂ£o e liberar | escrever `pode construir` | ê°Å¸Â§Â  |
| 8 | Agente constrêÂ³i a sua versêÂ£o (fase 2) | ê¢â¬â | ê°Å¸Â¤â |
| 9 | Abrir, testar e pedir ajustes | abrir o `index.html` gerado | ê°Å¸Â§Â  |

## Teste real (08/11/2026)

A construêÂ§êÂ£o C rodou no Claude Code (pela assinatura) com o site inema.club no papel de "seu site", jeito 1 (HTML salvo, sem REA), fase 1 e fase 2 de uma vez:

- **23 conclusêÂµes** no `provas.md`, conferidor: **NOTA 10/10 ê¢â¬â APROVADO**;
- **4 de 4** provas abertas êÂ  mêÂ£o (linhas 72, 113, 144 e 161 do HTML salvo) tinham o trecho citado;
- **472 s** (7 min 52 s) e 42 turnos do agente para as duas fases;
- saiu um `index.html` de 94 KB, sem rolagem lateral em 390 px e 1440 px.

Tudo em [`exemplos/rodada-real/`](exemplos/rodada-real/): o pedido usado, o `provas.md`, o HTML salvo e a versêÂ£o nova.

## Testes

```bash
python3 -m unittest discover tests     # ou: pytest
```

Sem internet. Cobrem: falta a seêÂ§êÂ£o "nêÂ£o deu para provar", seêÂ§êÂ£o vazia, conclusêÂ£o sem
referêÂªncia, referêÂªncias sêÂ³ em `node_modules`/`vendor`, têÂ­tulos em EN/ES, modelo em branco e os
dois exemplos pela linha de comando.

## Veja tambêÂ©m

- [O que êÂ© o REA](https://inematds.github.io/rea-engenharia-reversa/guia/) ê¢â¬â a ferramenta de engenharia reversa por trêÂ¡s de tudo.
- [REA sem travas](https://inematds.github.io/rea-sem-travas/guia/) ê¢â¬â instalar modelo aberto + harness + REA no seu computador.

## LicenêÂ§a

MIT. ConteêÂºdo aberto e gratuito do [INEMA.CLUB](https://inema.club).

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>