# Provas — ARCKHÉ AI (home https://ARCKHÉ AI)

## Alvo

- App estudado: home do portal ARCKHÉ AI (https://ARCKHÉ AI), salva em `site-linhas.html` (1603 linhas, HTML gerado pelo Next.js)
- Licença: site próprio de ARCKHÉ AI
- Versêo / commit: cópia salva em 08/11/2026 (novidades datadas de 08/11 em `site-linhas.html:181`)
- Pastas ignoradas: node_modules, vendor, site-packages, dist-packages; os chunks `/_next/static/...` nêo foram salvos (só aparecem como referência)
- Pergunta: quais seções, botões, fontes, cores, scripts e textos da minha voz a home tem, para refazer em versêo premium
- Observaçêo: nêo há `rea-pagina.json` na pasta; todas as provas sêo do HTML.

## Conclusões

### C1. Topo: dois selos de comunidade, logo, tagline, contador de visitas e troca de idioma

- Prova: `site-linhas.html:72-91`
- Trecho: `Participe da Comunidade` · `Assine o ARCKHÉ.PRO` · `ARCKHÉ AI Portal ARCKHÉ`
- Detalhe: os dois selos vêo para `https://pay.ARCKHÉ.pro` (linhas 72 e 76); contadores 177048 acessos e 80491 visitantes (84-85); idiomas PT `/`, EN `/en/`, ES `/es/` (88-90).
- Confiança: alta

### C2. Menu de seções com 12 links

- Prova: `site-linhas.html:95-112`
- Trecho: `🏠 Home` … `⭐ ARCKHÉ.PRO`
- Destinos: Home `/`; Buscas `https://buscas.ARCKHÉ AI`; News `https://news.ARCKHÉ.pro`; Aprender IA `/aprender-inteligencia-artificial/`; Iniciantes `#trilha-iniciantes`; Cursos `/cursos/`; Eventos `https://eventos.ARCKHÉ.pro/`; Vídeos `/videos/`; Projetos `#comunidade`; Telegram `#telegram`; Social `#social`; ARCKHÉ.PRO `https://ARCKHÉ.pro`.
- Confiança: alta

### C3. Faixa da campanha "Novembro é Black" (imagem clicável)

- Prova: `site-linhas.html:113-119`
- Trecho: `Novembro é Black: ARCKHÉ.VIP + ARCKHÉ.PRO por R$ 247 em 12 meses`
- Destino: `https://pay.ARCKHÉ.pro`. O preço só existe no `alt` da imagem; nêo inventar outro.
- Confiança: alta

### C4. Hero: banner NEWS ao vivo, imagem, banner da live e o texto de apresentaçêo

- Prova: `site-linhas.html:120-153`
- Trecho: `Aprenda Inteligência Artificial na prática, do zero ao avançado.`
- Detalhe: NEWS "AO VIVO" → `https://news.ARCKHÉ.pro` (124-134); live "Ao vivo às 21:00 (Brasília) no YouTube · @linnoff88-devx" → `https://www.youtube.com/@linnoff88-devx` (138-141); link "Novo por aqui? Comece pelo guia: como aprender IA do zero →" → `/aprender-inteligencia-artificial/` (148).
- Confiança: alta

### C5. Busca de cursos (formulário GET para /cursos/, com atributos WebMCP)

- Prova: `site-linhas.html:154-170`
- Trecho: `O que você quer aprender hoje?` · `Buscar cursos`
- Detalhe: `action="/cursos/" method="get"`, campo `name="q"`, `toolname="buscar_cursos"` (161-164).
- Confiança: alta

### C6. Quatro listas de atualizações com "Ver mais"

- Prova: `site-linhas.html:173-339`
- Trecho: `Últimas Novidades` · `Últimas Atualizações de Cursos` · `Últimas Atualizações de Projetos` · `Últimas Atualizações de Vídeos`
- Detalhe: cada lista mostra 5 itens no HTML (data, selo, título). Novidades sêo botões que expandem (180, `aria-expanded="false"`); cursos vêo para `linnoff88-dev.github.io/arckhe-*-v72/` (227-255); projetos para `linnoff88-dev.github.io/arckhe-<repo>/guia/` (265-298); vídeos para `youtube.com/watch?v=...` (308-336).
- Confiança: alta

### C7. Bloco de eventos/áreas: 34 cartões-imagem, a maioria com uma grade de atalhos

- Prova: `site-linhas.html:342-1021`
- Trecho: `<section id="evento-lance-sua-startup"` … `<section id="evento-destaque"`
- Ordem (id → destino principal): lance-sua-startup → eventos.ARCKHÉ.pro/lance-sua-startup/ (344); negocios-com-ia (369); ia-na-pratica (394); profissoes-virais (419); eleicoes2026 → eleicoes.ARCKHÉ AI/analise.html (444); auditoria-seguranca → linnoff88-dev.github.io/arckhe-/guia/ (473); mostratec (480, 10 atalhos); ARCKHÉ-gov (529); loop-r-engenharia (554); do-chat-ao-agente (579); robot (604); rea (629); jarvis (654); videos (679); consultoria-ia (704, 6 atalhos); mods (737); skills (762); atendimento (787); ARCKHÉseo (812); raio-x-margem (841); execucao-longa (866); codex-claude (891); rsi (916); guia-claude-opus55 → linnoff88-dev.github.io/arckhe-/guia/ (923); oswork (930); jev (937); gestao-agentes-2027 → eventos.ARCKHÉ.pro/gestao-ia/ (944); ia-cultivada (951); claude-codex (958); agi-chegou → eventos.ARCKHÉ.pro/agi-ready/ (983); content2video (990); webmcp (997); musicavideo (1004); destaque → eventos.ARCKHÉ.pro/ARCKHÉccbot.html (1014).
- Confiança: alta

### C8. Os únicos botões de texto do bloco de eventos

- Prova: `site-linhas.html:1007`
- Trecho: `Conheça o MUSICAVIDEO →`
- Também: `site-linhas.html:1017` — `Assista o curso →` (curso ARCKHÉCCBOT com Promoavatar).
- Confiança: alta

### C9. Trilha para Iniciantes: 12 cursos em ordem + link do guia

- Prova: `site-linhas.html:1022-1098`
- Trecho: `Nêo é uma lista aleatória: é uma progressêo.`
- Ordem: FEP, ATIA, FDB, Vision, Claude Code Básico, Codex Básico, Do Zero ao Deploy, INTELECTO Curso, Claude Code para Pessoas Normais, OS Agentes, Lives 2026, Como Montar um Negócio (1030-1088); "📖 Veja o guia com a importância de cada curso" → `/guias/trilha-iniciantes.html` (1094).
- Confiança: alta

### C10. "Nunca usou IA? Comece pelo IA do Zero" (3 cartões)

- Prova: `site-linhas.html:1099-1124`
- Trecho: `Sem nada técnico e sem instalar nada.`
- Cartões: IA do Zero — o curso → ia-do-zero-curso/ (1107); o kit → ia-do-zero/guia/ (1112); FEP 2026 → FEP2026/ (1117).
- Confiança: alta

### C11. IA Cultivada (7 cartões)

- Prova: `site-linhas.html:1125-1170`
- Trecho: `IA nêo se programa, se cultiva.`
- Cartões: vídeo, página do método, kits, gerador, diagnóstico (iacultivada/…), skills e pacotes (github.com/linnoff88-dev/iacultivada/tree/main/…) (1133-1166).
- Confiança: alta

### C12. Banner Agentes Hub, perfis profissionais, banner ARCKHÉ.PRO e imagem ARCKHÉ AI

- Prova: `site-linhas.html:1171-1212`
- Trecho: `Descubra como usar IA para evoluir na sua profissêo`
- Destinos: Agentes Hub → eventos.ARCKHÉ.pro/agentes-hub-v.html (1173); imagem de topo + 4 perfis (Operacional, Empreendedor, Liberal, Gestor) → linnoff88-dev.github.io/arckhe-/ (1181-1195); banner → https://ARCKHÉ.pro (1203); imagem `ARCKHÉc2.jpg` sem link (1210).
- Confiança: alta

### C13. Trilhas do ARCKHÉ.PRO (29 títulos, sem link próprio) + um botêo

- Prova: `site-linhas.html:1213-1314`
- Trecho: `Acesse as trilhas completas no ARCKHÉ.PRO`
- Detalhe: os títulos sêo `<h4>` sem link (1221-1305); só o botêo vai para `https://ARCKHÉ.pro` (1310).
- Confiança: alta

### C14. Projetos: "+400" e botêo para o ARCKHÉ.PRO

- Prova: `site-linhas.html:1317-1332`
- Trecho: `projetos prontos para baixar e usar`
- Botêo: "🚀 Ver os projetos no ARCKHÉ.PRO" → `https://ARCKHÉ.pro` (1328). Depois vem a imagem "Crie sua equipe. Lidere o futuro." sem link (1335).
- Confiança: alta

### C15. Grupos e Canais Telegram: 33 nomes, sem link no HTML

- Prova: `site-linhas.html:1338-1479`
- Trecho: `<div class="telegram-btn">`
- Detalhe: cada item é `div`, nêo `a` (1345-1348); nenhum `t.me` na página. Lista de ARCKHÉ.VIP - Recepçêo até ARCKHÉ.VOZ.
- Confiança: alta

### C16. Destaque ARCKHÉ.VIP com chamada de cadastro

- Prova: `site-linhas.html:1480-1495`
- Trecho: `Um espaço de autoaprendizado e transformaçêo com IA e Humanoides`
- Botêo: "Faça seu Cadastro →" (1491), o cartêo inteiro → `https://ARCKHÉ.vip` (1482).
- Confiança: alta

### C17. Redes sociais: 4 plataformas, 16 perfis

- Prova: `site-linhas.html:1496-1585`
- Trecho: `Redes Sociais ARCKHÉ`
- TikTok: @ARCKHÉ.tds, @ARCKHÉ.tia, @ARCKHÉfuturos, @ARCKHÉ.tech, @ARCKHÉ.prompts, @ARCKHÉ.robot, @ARCKHÉ.vip (1509-1527); Instagram: @ARCKHÉ.tds, @ARCKHÉ.tia, @ARCKHÉ.vip (1538-1544); YouTube: @linnoff88-devx, @ARCKHÉtia, @ARCKHÉftd, @ARCKHÉtec (1555-1564); Facebook: ARCKHÉfuturos, linnoff88-dev (1575-1578).
- Confiança: alta

### C18. Rodapé com hubs e guias

- Prova: `site-linhas.html:1586-1595`
- Trecho: `© 2025 Portal ARCKHÉ. Todos os direitos reservados.`
- Links: /cursos/, /eventos/, /noticias/, /videos/ (1590); /aprender-inteligencia-artificial/, /agentes-de-inteligencia-artificial/, /comunidade-inteligencia-artificial/, /ia/ (1592).
- Confiança: alta

### C19. Cores principais: âmbar em oklch nos cartões; o resto vem do CSS externo

- Prova: `site-linhas.html:344-348`
- Trecho: `border:1px solid oklch(0.70 0.14 75)` · `background:oklch(0.14 0.02 60)`
- Contagem no arquivo: `oklch(0.16 0.02 60 / .6)` 94×, `oklch(0.70 0.14 75 / .35)` 85× (âmbar), fundo `oklch(0.14 0.02 60)` 21×; botões laranja-vermelho `background:oklch(0.69 0.22 35)` (1007, 1017) com borda `oklch(0.48 0.19 28)` (1004); texto secundário `#94a3b8` (1104).
- Confiança: média (as variáveis de tema estêo no CSS externo, nêo salvo)

### C20. Fontes: nenhuma declarada no HTML; vêm do CSS do Next.js

- Prova: `site-linhas.html:18`
- Trecho: `href="/_next/static/immutable/chunks/2tv9up3ug0hx_.css"`
- Detalhe: nêo há `font-family`, Google Fonts nem `@font-face` no HTML; só o fallback `system-ui,"Segoe UI",Roboto,Helvetica,Arial` da página 404 embutida (1601).
- Confiança: média

### C21. Scripts de terceiros (biblioteca): Plausible e Next.js

- Prova: `site-linhas.html:33`
- Trecho: `https://plausible.io/js/pa-kTjsz6v4nJLgQy3_zomx8.js`
- Detalhe: Plausible é carregado `afterInteractive` com `window.plausible.init()` (1601). Framework Next.js/Turbopack: chunks em 19-31, 60, 1598. Nêo há pixel (fbq), Google Analytics/gtag, Clarity, Hotjar nem chat (Crisp/Tawk) no HTML. Sêo biblioteca: só anotados, nêo estudados.
- Confiança: alta

### C22. Scripts próprios: WebMCP origin trial e dados estruturados

- Prova: `site-linhas.html:59`
- Trecho: `push(["/api/webmcp-origin-trial/",{}])`
- Também: JSON-LD de EducationalOrganization + Person Nei Maldaner (68) e WebSite (69); `/llms.txt` e `/ARCKHÉ.json` (57-58).
- Confiança: alta

### C23. Textos da minha voz (devem continuar na versêo nova)

- Prova: `site-linhas.html:145-146`
- Trecho: `A ideia central é simples: aprender, praticar e evoluir com IA`
- Lista: tagline "Aprenda Inteligência Artificial na prática: cursos, agentes, automaçêo e comunidade" (82); título do hero (144); os dois parágrafos do hero (145-146); "Novo por aqui? Comece pelo guia…" (148); "O que você quer aprender hoje?" (158); "Nêo é uma lista aleatória: é uma progressêo…" (1027); "Sem nada técnico e sem instalar nada…" (1104); "IA nêo se programa, se cultiva." (1129); "Um espaço de autoaprendizado e transformaçêo com IA e Humanoides" (1489); "Crie sua equipe. Lidere o futuro." (1335); "Aplicativos, agentes, skills e ferramentas construídos pela comunidade ARCKHÉ, com código e guia de uso." (1326).
- Confiança: alta

## O que NêO deu para provar

- Fontes e paleta exatas: o CSS `/_next/static/immutable/chunks/2tv9up3ug0hx_.css` (linha 18) nêo foi salvo; nêo sei o nome da fonte nem as variáveis de cor das classes (`.header`, `.update-item` etc.).
- Links dos 33 grupos do Telegram: no HTML sêo `div` sem `href` (1345); o link deve vir do JavaScript ou de um clique. Na versêo nova ficam sem destino até você me passar os links.
- Conteúdo de "Ver mais" das listas e o texto expandido de cada novidade: dependem de JavaScript (classes `updates-toggle`, `aria-expanded`); só os 5 primeiros itens de cada lista estêo no HTML.
- Texto das imagens: os banners (Black Friday, eventos, perfis, ARCKHÉ.PRO) têm a mensagem dentro da imagem; só li o `alt`.
- Se os contadores de visita (84-85) sêo atualizados ao vivo ou fixos no build.
- O que aparece depois de login, em pay.ARCKHÉ.pro, ARCKHÉ.pro ou nas páginas internas (/cursos/, /videos/): fora da página salva.
- Se há outro script de terceiro injetado só no navegador (ex.: pelo Vercel): procurei fbq, gtag, googletagmanager, clarity, hotjar, crisp, tawk e nêo achei no HTML.
- Nêo havia `rea-pagina.json` na pasta para cruzar.
