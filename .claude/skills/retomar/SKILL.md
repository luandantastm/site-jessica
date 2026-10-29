---
name: retomar
description: Retoma o projeto do site da Dra. Jéssica Coli lendo as decisões já tomadas, o último handoff e o histórico do git. Use no início de uma sessão ou quando o usuário disser "retomar", "onde paramos", "continuar o projeto".
---

# Retomar o projeto

Objetivo: em poucos segundos, deixar claro onde o projeto parou e qual é o próximo passo, sem refazer decisões já tomadas.

## Passos

1. Ler `docs/HANDOFF.md` (estado atual, pendências, próximo passo).
2. Ler `docs/DECISOES.md` (todas as decisões, em ordem cronológica). Decisões mais recentes prevalecem sobre as antigas quando conflitarem.
3. Rodar `git status --short` e `git log --oneline -15` para ver mudanças não commitadas e o que foi feito desde o último handoff.
4. Se houver mudanças não commitadas, avisar — podem ser trabalho de uma sessão que não rodou `/fechar-dia`.

## Saída

Responder em português, curto, neste formato:

- **Onde paramos:** 1–3 linhas.
- **Decisões em vigor:** só as que importam para o próximo passo (não listar todas).
- **Pendências:** a lista do handoff, marcando o que parece já resolvido pelo git log.
- **Próximo passo sugerido:** uma ação concreta.

Não alterar arquivos nesta skill. Tratar as decisões registradas como já acordadas com o usuário: não reabrir a discussão a menos que o usuário peça.
