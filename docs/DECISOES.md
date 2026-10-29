# Registro de decisões

Append-only. Cada sessão adiciona uma seção com a data. Decisões novas que substituem antigas devem dizer isso explicitamente.

## 2026-10-29

- **Tecnologia:** site 100% HTML estático, CSS inline, JS mínimo — hospedagem simples na AWS (S3), sem etapa de build.
- **Estrutura:** página única (one-page) com seções Início, Sobre, Atendimentos, A consulta, Dúvidas e Contato, mais `404.html` para o S3.
- **Contato:** agendamento centralizado no WhatsApp via `api.whatsapp.com/send` com mensagem pré-preenchida; botão flutuante no canto inferior direito.
- **Identidade visual:** paleta vinho/dourado/creme derivada da plaquinha "Dra. Jessica Coli – Ginecologista" da foto; tipografia Fraunces + Manrope; estilo editorial e acolhedor.
- **Nome exibido:** "Dra. Jéssica Coli" (com acento), conforme informado pelo Luan.
- **Conformidade:** seguir a Resolução CFM 2.336/2023 (nome + CRM + RQE visíveis, sem sensacionalismo, aviso de caráter informativo).
- **Conteúdo provisório:** textos de bio, formação, atendimentos e FAQ são rascunhos a validar com a Dra. Jéssica.
- **Versionamento:** repositório privado `luandantastm/site-jessica` no GitHub, branch `main`.
- **Fluxo de trabalho:** skills `/retomar` e `/fechar-dia` para continuidade entre sessões.
