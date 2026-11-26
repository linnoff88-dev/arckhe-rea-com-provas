# Construçêo A — Painel de agentes

**O que sai:** um painel com 6 agentes "vivos" para um negócio, cada cartêo dizendo o que o
agente faz e o que está fazendo agora, e uma caixa de comando que manda a tarefa ao agente certo.

**De onde vem a ideia:** você estuda como um app open source mostra vários agentes lado a lado
e constrói a SUA versêo, com seu nome e seu visual. Nêo copia o app.

**Antes de colar:** troque tudo que está entre [colchetes]. Tenha o código do app estudado numa
pasta (ex.: `git clone`) e confira a licença (regra 3). Preencha o brief de design
(`brief/MODELO-brief-design.md`) e deixe-o na mesma pasta.

Funciona no Claude Code, no Codex ou no harness dsh (instalaçêo no guia
https://linnoff88-dev.github.io/arckhe-/guia/). Com o REA instalado, o agente também pode usar
`analyze-javascript-application` em apps JavaScript/Electron.

---

```text
Você vai trabalhar em duas fases. Nêo pule a fase 1.

FASE 1 — ESTUDAR COM PROVAS (nêo escreva código ainda)
Estude o app open source em [caminho da pasta, ex.: ~/estudo/app-agentes] e responda:
como ele mostra vários agentes lado a lado (layout dos cartões, estado de cada agente,
como a tarefa chega a um agente, como o cartêo mostra que o agente está trabalhando).

Regras do estudo:
1. Antes de tudo, abra o arquivo de licença e diga qual é. Se nêo for uma licença que
   deixa estudar (MIT, Apache-2.0, BSD, GPL, MPL...), pare e me avise.
2. Estude só o código do próprio app. Ignore node_modules, vendor, site-packages, dist,
   build e arquivos .min.js — sêo bibliotecas de terceiros, nêo o app.
3. Entregue o arquivo provas.md exatamente no formato de provas/MODELO-provas.md:
   seçêo "## Alvo" (com a linha "Licença:"), seçêo "## Conclusões" com uma conclusêo por
   bloco "### C1. ...", cada uma com "Prova:" = `caminho/do/arquivo.ext:linha-linha`
   e "Trecho:" copiado do arquivo, e a seçêo "## O que NêO deu para provar".
4. Nêo escreva nenhuma conclusêo sem arquivo e linha. Se você acha, mas nêo achou no
   código, vai para "O que NêO deu para provar".
5. Rode: python3 ~/rea-com-provas/confere_provas.py provas.md
   Se sair REPROVADO, corrija o provas.md e rode de novo até sair APROVADO.
Pare aqui e me mostre o resultado do conferidor.

FASE 2 — CONSTRUIR A SUA VERSêO (só depois que eu disser "pode construir")
Construa do zero, em [stack, ex.: um único index.html com HTML, CSS e JavaScript, sem
servidor], na pasta [pasta, ex.: ~/projetos/meu-painel], um painel chamado [nome do seu
painel] para [tipo de negócio, ex.: uma clínica odontológica] com 6 agentes:
  1. [Captaçêo] — [o que faz, ex.: acha pacientes novos nas redes e no Google]
  2. [Caixa de entrada] — [ex.: lê e responde e-mail e WhatsApp]
  3. [SEO] — [ex.: escreve e revisa páginas do site]
  4. [Agenda] — [ex.: marca, confirma e remarca consultas]
  5. [Suporte] — [ex.: tira dúvidas de quem já é paciente]
  6. [Relatórios] — [ex.: resume a semana em números]
Cada cartêo mostra: nome, o que o agente faz (1 linha), estado (parado / pensando /
trabalhando / pronto) com rótulo de texto além da cor, a última tarefa e a hora.
Embaixo, uma caixa de comando: eu escrevo um pedido em português e o painel escolhe o
agente certo, mostra para quem mandou e por quê, e o cartêo daquele agente "acorda".
Os agentes sêo simulados (sem chamar nenhuma IA, sem API, sem chave): o estado muda
com temporizadores, para eu ver o painel vivo.

Regras da construçêo:
- Use o provas.md só para entender o comportamento. Nêo copie arquivos, textos, nomes,
  ícones nem o visual do app estudado.
- O visual vem do brief de design em [caminho do brief preenchido]. Siga cores, fontes,
  movimento e densidade de lá.
- No fim, me diga como abrir, o que ficou de fora e o que precisa de teste manual.
```

---

**Conferir:** `python3 ~/rea-com-provas/confere_provas.py provas.md` (o kit clonado na sua pasta pessoal, como no passo 1 do guia) tem de sair `APROVADO` antes da fase 2.
