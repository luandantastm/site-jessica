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
- **Versionamento:** repositório `luandantastm/site-jessica` no GitHub, branch `main` (criado privado; tornado público no mesmo dia, ver abaixo).
- **Prévia pública:** repositório tornado público e GitHub Pages ativado (branch `main`, raiz) em https://luandantastm.github.io/site-jessica/ para mostrar à Dra. Jéssica. É só prévia; a hospedagem definitiva continua sendo AWS.
- **Fluxo de trabalho:** skills `/retomar` e `/fechar-dia` para continuidade entre sessões.
- **Layout aprovado:** Luan aprovou a versão inicial do site ("o site ficou bom") — segue como base para os próximos ajustes de conteúdo.
- **Coleta de dados com a Dra.:** via checklist interativo em https://claude.ai/artifact/S6iD86SkHYKh85U8kLMxGJ (22 itens em 5 grupos; 5 essenciais para publicar), em vez de lista solta por mensagem — respostas ficam salvas na coleção `respostas` do artifact, onde o Claude lê direto. Alternativa: botão "Copiar respostas" gera texto para WhatsApp.
- **Acesso ao checklist:** a Dra. deve ser convidada por e-mail como Editora, sem link público — só assim ela consegue gravar as respostas (convidados de fora da organização via link público só leem).
