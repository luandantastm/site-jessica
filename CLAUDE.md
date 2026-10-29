# Site da Dra. Jéssica Coli — Ginecologista

Site institucional da Dra. Jéssica Coli (médica ginecologista, irmã do Luan, dono do repositório).
Repositório: https://github.com/luandantastm/site-jessica (público)
Prévia: https://luandantastm.github.io/site-jessica/ (GitHub Pages, atualiza a cada push na `main`; hospedagem definitiva será AWS)

## Regras do projeto

- **100% HTML estático.** Sem build, sem framework, sem Node. CSS fica inline no `<style>` de cada página; JS só o mínimo (hoje: fechar menu mobile e ano no rodapé). O site precisa funcionar abrindo o `index.html` direto no navegador.
- **Hospedagem: AWS simples** (S3 static website, opcionalmente com CloudFront). Documento de índice `index.html`, documento de erro `404.html`. Usar sempre caminhos relativos (`assets/img/...`) para funcionar local e no S3.
- **Idioma:** português do Brasil em todo o conteúdo e nos comentários.
- **WhatsApp:** todos os botões usam `https://api.whatsapp.com/send?phone=<NUMERO>&text=<mensagem>`. O número está como placeholder `5500000000000` — trocar em todas as ocorrências (formato: 55 + DDD + número, só dígitos). O botão flutuante fica fixo no canto inferior direito (`.whatsapp-flutuante`).
- **Publicidade médica (Resolução CFM nº 2.336/2023):** manter sempre visível nome, CRM e RQE; não usar antes/depois, promessas de resultado, preços promocionais ou linguagem sensacionalista. O aviso "não substitui a consulta médica" fica no rodapé.
- **Acessibilidade:** manter link "Pular para o conteúdo", `alt` nas imagens, `aria-label` em botões só com ícone, foco visível e `prefers-reduced-motion`.

## Identidade visual

Paleta tirada da plaquinha do consultório na foto: vinho `#7a1f2b`, dourado `#b8925a`, creme `#f7f1ea`. Tipografia: Fraunces (títulos, serifada) + Manrope (texto), via Google Fonts. Tokens de cor em `:root` no `index.html`.

A foto original (`assets/img/foto-jessica.jpg`) tem um ícone de captura de tela no canto inferior esquerdo; ele é escondido via CSS (`object-position` + `aspect-ratio` em `.hero-foto img`). Se trocar a foto, revisar essa regra.

## Estrutura

```
index.html          página única (seções: início, sobre, atendimentos, consulta, dúvidas, contato)
404.html            página de erro para o S3
assets/img/         imagens
docs/DECISOES.md    registro de decisões do projeto (append-only, com data)
docs/HANDOFF.md     estado atual + pendências + próximo passo
.claude/skills/     skills do projeto (retomar, fechar-dia)
```

## Skills

- `/retomar` — lê `docs/DECISOES.md`, `docs/HANDOFF.md` e o git log recente e resume onde o projeto parou.
- `/fechar-dia` — consolida as decisões e o handoff da sessão nos docs e faz commit + push para o GitHub.

Sempre que uma decisão relevante for tomada na conversa (conteúdo, design, hospedagem, domínio), ela deve acabar em `docs/DECISOES.md` — no máximo até o `/fechar-dia`.

## Validar localmente

Abrir `index.html` no navegador. No WSL: `explorer.exe index.html` ou o caminho `\\wsl.localhost\...`.
