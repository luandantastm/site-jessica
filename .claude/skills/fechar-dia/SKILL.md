---
name: fechar-dia
description: Fecha a sessão de trabalho do site da Dra. Jéssica Coli — registra as decisões do dia em docs/DECISOES.md, atualiza docs/HANDOFF.md e faz commit + push para o GitHub. Use quando o usuário disser "fechar o dia", "encerrar", "salvar tudo".
---

# Fechar o dia

Objetivo: nada que foi decidido ou feito na sessão pode se perder. A próxima sessão (via `/retomar`) deve conseguir continuar só lendo os docs.

## Passos

1. **Levantar o que mudou:** revisar a conversa da sessão + `git status` + `git diff` para listar decisões tomadas e trabalho feito.
2. **Atualizar `docs/DECISOES.md`:** adicionar ao final uma seção `## AAAA-MM-DD` (data de hoje) com uma linha por decisão, no formato `- **Tema:** decisão — motivo`. Não apagar nem reescrever decisões antigas; se uma decisão substituir outra, dizer isso explicitamente ("substitui a decisão de AAAA-MM-DD sobre X").
3. **Reescrever `docs/HANDOFF.md`** (este arquivo é sobrescrito, não acumulado):
   - Data da última atualização
   - Estado atual (o que está pronto)
   - Pendências (checklist `- [ ]`), incluindo dados que faltam da Dra. Jéssica
   - Próximo passo recomendado
4. **Atualizar `CLAUDE.md`** só se alguma regra permanente do projeto mudou.
5. **Commit e push:**
   - `git add -A` (conferir antes que não entrou nada indesejado)
   - Mensagem no padrão `tipo: resumo` em português (ex.: `feat: seção de convênios`, `docs: fechamento do dia 2026-10-29`). Se a sessão teve várias frentes, um commit por frente é melhor que um commit gigante.
   - `git push` para `origin main`.
6. **Confirmar ao usuário:** hash do(s) commit(s), link do repositório e o próximo passo do handoff.

Se o push falhar, reportar o erro exato e não tentar forçar (`--force` é proibido sem pedido explícito).
