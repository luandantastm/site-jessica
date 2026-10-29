# Handoff

**Última atualização:** 2026-10-29

## Estado atual

- Versão inicial do site pronta e aprovada pelo Luan: `index.html` (one-page) + `404.html`, foto da Dra. Jéssica no hero, botão flutuante de WhatsApp, layout responsivo.
- Repositório público no GitHub; prévia publicada via GitHub Pages em https://luandantastm.github.io/site-jessica/ (cada push na `main` atualiza a prévia).
- Checklist de dados para a Dra. publicado em https://claude.ai/artifact/S6iD86SkHYKh85U8kLMxGJ. Ainda sem respostas (verificado: coleção `respostas` vazia).

## Pendências

- [ ] Luan compartilhar o checklist com a Dra. (convite por e-mail como Editora, sem link público)
- [ ] Dra. preencher o checklist. Essenciais para publicar:
  - [ ] Número real do WhatsApp (substituir `5500000000000` e `(00) 00000-0000`)
  - [ ] CRM/UF e RQE reais (confirmar especialidade do RQE)
  - [ ] Endereço do consultório e link do Google Maps
  - [ ] Horários de atendimento (confirmar ou corrigir)
- [ ] Demais itens do checklist: bio, frase de destaque, graduação, residência, TEGO, cursos, lista de atendimentos, obstetrícia, DIU/implante, procedimentos, teleconsulta, convênio, revisão do FAQ, Instagram, foto em alta resolução, fotos do consultório, domínio
- [ ] Aplicar as respostas no `index.html` (e no JSON-LD do `<head>`)
- [ ] Domínio e publicação na AWS (S3 + CloudFront + certificado)
- [ ] Imagem para compartilhamento (og:image) com URL absoluta após definir o domínio
- [ ] Na prévia do GitHub Pages, o "Voltar ao início" do `404.html` aponta para `/` (raiz do github.io) — some na AWS com domínio próprio

## Próximo passo

Ler as respostas do checklist (`ArtifactData` → `list` na coleção `respostas` do artifact acima; ou o texto que a Dra. mandar pelo WhatsApp) e aplicar no site, começando pelos 5 essenciais.
