# REA com provas

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![RefaÃ§a com provas](guia/assets/banner.jpg)](https://inematds.github.io/rea-com-provas/guia/)

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

> **A IA diz que entendeu o app. PeÃ§a a prova.**

## O que Ã©

O **REA com provas** Ã© um kit aberto e gratuito para quem usa um agente de IA (Claude Code, Codex ou o harness dsh) para estudar um app e fazer a prÃ³pria versÃ£o. O problema: o agente diz que entendeu como o app funciona e inventa o que nÃ£o viu. O kit traz 4 regras, 3 pedidos prontos (painel de agentes, reator de leads e site refeito) e um conferidor em Python que reprova o arquivo de provas quando falta prova. Para usar, vocÃª precisa de Python 3 e de um agente de IA no terminal.

## ðŸ“– Guia de uso

Guia completo (landing + passo a passo): **https://inematds.github.io/rea-com-provas/guia/**

> [!WARNING]
> **SeguranÃ§a e licenÃ§a.** Use sÃ³ em **software seu** ou **open source cuja licenÃ§a deixa
> estudar** (MIT, Apache-2.0, BSD, GPL, MPLâ€¦). Estudar nÃ£o Ã© copiar: a sua versÃ£o Ã© escrita do
> zero, com seu nome, seus textos e seu visual. Rode o agente numa pasta separada, sem senhas,
> chaves ou dados de clientes. Detalhes em [REGRAS.md](REGRAS.md).

## As 4 regras

1. **Sempre peÃ§a o arquivo de provas `provas.md`**: cada conclusÃ£o com o arquivo/trecho que a prova, mais a seÃ§Ã£o "O que NÃƒO deu para provar".
2. **Foco no cÃ³digo do prÃ³prio app**, nÃ£o nas bibliotecas embutidas (mande ignorar `node_modules`, `vendor`, `site-packages`).
3. **SÃ³ software seu ou open source que a licenÃ§a deixa estudar.** Depois construa a SUA versÃ£o, com seu nome e visual.
4. **Descreva o visual em detalhe** (cores, fontes, movimento) num brief de design.

## O que vem no kit

| Arquivo | Para que serve |
|---|---|
| [`REGRAS.md`](REGRAS.md) | As 4 regras e o aviso de seguranÃ§a e licenÃ§a |
| [`prompts/a-painel-de-agentes.md`](prompts/a-painel-de-agentes.md) | ConstruÃ§Ã£o A: painel com 6 agentes vivos para um negÃ³cio + caixa de comando |
| [`prompts/b-reator-de-leads.md`](prompts/b-reator-de-leads.md) | ConstruÃ§Ã£o B: lead entra â†’ qualificar, responder, agendar, acompanhar â†’ comemora |
| [`prompts/c-site-refeito.md`](prompts/c-site-refeito.md) | ConstruÃ§Ã£o C: mapear o SEU site e refazer numa versÃ£o premium |
| [`provas/MODELO-provas.md`](provas/MODELO-provas.md) | Formato do arquivo de provas |
| [`confere_provas.py`](confere_provas.py) | Conferidor: nota 0â€“10, APROVADO/REPROVADO e o que falta |
| [`brief/MODELO-brief-design.md`](brief/MODELO-brief-design.md) | Brief de design com exemplo preenchido no padrÃ£o INEMA |
| [`exemplos/`](exemplos/) | `provas-boa.md` (aprovada), `provas-ruim.md` (reprovada) e a rodada real |
| [`tests/`](tests/) | Testes do conferidor, sem internet |

O kit vem configurado com o INEMA como exemplo (brief no padrÃ£o INEMA, rodada real no site inema.club). Troque os [colchetes] dos prompts e o brief pelo seu negÃ³cio.

## O conferidor

```bash
python3 confere_provas.py provas.md          # relatÃ³rio em texto
python3 confere_provas.py provas.md --json   # mesmo resultado em JSON
```

Reprova (cÃ³digo de saÃ­da 1) quando falta a seÃ§Ã£o "O que NÃƒO deu para provar" (ou ela estÃ¡ vazia),
quando uma conclusÃ£o nÃ£o cita arquivo/trecho, ou quando todas as referÃªncias apontam para
bibliotecas (`node_modules`, `vendor`, `site-packages`â€¦). Aprova com cÃ³digo 0. NÃ£o conseguiu ler: cÃ³digo 2.
O conferidor checa o formato; abrir 2 ou 3 provas e ver se o trecho estÃ¡ lÃ¡ continua sendo com vocÃª.

## O processo, do inÃ­cio ao fim

Quem faz: ðŸ§  vocÃª (com o agente aberto) Â· âš™ï¸ script Â· ðŸ¤– agente de IA (Claude Code, Codex ou dsh)

| # | Passo | Comando | Quem |
|---|---|---|---|
| 1 | Baixar o kit e rodar os testes | `cd ~ && git clone https://github.com/inematds/rea-com-provas.git && cd rea-com-provas && python3 -m unittest discover tests` | âš™ï¸ |
| 2 | (Opcional) Instalar REA + harness | guia https://inematds.github.io/rea-sem-travas/guia/ | ðŸ§  |
| 3 | Escolher o alvo e conferir a licenÃ§a | `cat ~/estudo/app/LICENSE` | ðŸ§  |
| 4 | Preencher o brief de design | `cp brief/MODELO-brief-design.md ~/estudo/brief.md` | ðŸ§  |
| 5 | Colar uma construÃ§Ã£o de `prompts/` no agente (fase 1: estudar) | `cd ~/estudo && claude` (ou `codex`) | ðŸ§  â†’ ðŸ¤– |
| 6 | Agente entrega o `provas.md` e roda o conferidor atÃ© APROVADO | `python3 ~/rea-com-provas/confere_provas.py provas.md` | ðŸ¤– + âš™ï¸ |
| 7 | Conferir 2 ou 3 provas Ã  mÃ£o e liberar | escrever `pode construir` | ðŸ§  |
| 8 | Agente constrÃ³i a sua versÃ£o (fase 2) | â€” | ðŸ¤– |
| 9 | Abrir, testar e pedir ajustes | abrir o `index.html` gerado | ðŸ§  |

## Teste real (08/11/2026)

A construÃ§Ã£o C rodou no Claude Code (pela assinatura) com o site inema.club no papel de "seu site", jeito 1 (HTML salvo, sem REA), fase 1 e fase 2 de uma vez:

- **23 conclusÃµes** no `provas.md`, conferidor: **NOTA 10/10 â€” APROVADO**;
- **4 de 4** provas abertas Ã  mÃ£o (linhas 72, 113, 144 e 161 do HTML salvo) tinham o trecho citado;
- **472 s** (7 min 52 s) e 42 turnos do agente para as duas fases;
- saiu um `index.html` de 94 KB, sem rolagem lateral em 390 px e 1440 px.

Tudo em [`exemplos/rodada-real/`](exemplos/rodada-real/): o pedido usado, o `provas.md`, o HTML salvo e a versÃ£o nova.

## Testes

```bash
python3 -m unittest discover tests     # ou: pytest
```

Sem internet. Cobrem: falta a seÃ§Ã£o "nÃ£o deu para provar", seÃ§Ã£o vazia, conclusÃ£o sem
referÃªncia, referÃªncias sÃ³ em `node_modules`/`vendor`, tÃ­tulos em EN/ES, modelo em branco e os
dois exemplos pela linha de comando.

## Veja tambÃ©m

- [O que Ã© o REA](https://inematds.github.io/rea-engenharia-reversa/guia/) â€” a ferramenta de engenharia reversa por trÃ¡s de tudo.
- [REA sem travas](https://inematds.github.io/rea-sem-travas/guia/) â€” instalar modelo aberto + harness + REA no seu computador.

## LicenÃ§a

MIT. ConteÃºdo aberto e gratuito do [INEMA.CLUB](https://inema.club).

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>