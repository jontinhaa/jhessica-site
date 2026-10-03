# Regras de segurança do projeto

Contexto: sites e sistemas web de pequenos negócios no Brasil (Astro, TypeScript), feitos por um desenvolvedor solo. Além do que você já procura, trate como achado:

Segredos
- Chave, token ou senha em código, teste, comentário ou arquivo versionado. Só `.env.example`, sem valores reais, é versionado.
- Segredo em variável com prefixo público (`PUBLIC_`, `NEXT_PUBLIC_`, `VITE_`, `EXPO_PUBLIC_`): ela vai parar no navegador ou no app.

Navegador
- HTML vindo de usuário, URL ou API em `innerHTML`, `outerHTML`, `set:html`, `dangerouslySetInnerHTML` ou `v-html` sem sanitização.
- Script de terceiro sem necessidade clara, ou carregado de CDN sem `integrity`.
- Dado pessoal (nome, telefone, e-mail, CPF, endereço) em URL, query string, analytics, `console.log` ou guardado no `localStorage` sem prazo.

Servidor e rotas
- Rota ou função de servidor sem validação de entrada por schema, sem limite de tamanho do corpo ou sem rate limit quando cria, envia ou cobra algo.
- CORS `*` em rota com efeito; erro que devolve stack, token ou resposta crua de provedor.
- Redirecionamento para URL vinda do usuário sem lista de destinos permitidos.

Configuração e cadeia de suprimentos
- Deploy sem os cabeçalhos Content-Security-Policy, Strict-Transport-Security, X-Content-Type-Options, Referrer-Policy, Permissions-Policy e frame-ancestors.
- Dependência nova desconhecida, com nome parecido com o de pacote famoso, ou com script de instalação estranho.
- Workflow do GitHub com `pull_request_target`, permissões amplas ou segredo impresso em log.
