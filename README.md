# Calculadora de TMB — versão web

Versão em HTML, CSS e JavaScript do aplicativo Android original, pronta para
ser editada no VS Code.

## Compartilhar no Figma

O aplicativo usa o modo local por padrão. Não é preciso configurar chave ou
servidor: qualquer pessoa que receber o link pode entrar com um email válido e
uma senha de pelo menos 6 caracteres. Os cálculos ficam salvos no navegador de
cada visitante.

## Executar no VS Code

Agora também é possível abrir o `index.html` diretamente no navegador ou usar
a extensão **Live Server** do VS Code.

Para usar o Vite, instale as dependências e execute o frontend:

```bash
pnpm install
pnpm dev
```

## Usar o servidor Python (opcional)

1. Execute `python server.py`.
2. No `index.html`, altere `API_MODE` de `local` para `server`.
3. Copie a chave exibida depois de `API_TRANSPORT_KEY=` para
   `API_TRANSPORTE_KEY`.

O Vite encaminha `/api` para `http://localhost:8000`, evitando problemas de
CORS durante o desenvolvimento local. Para usar outro servidor, altere
`API_BASE_URL` no `index.html` e o destino do proxy em `vite.config.ts`.

## Arquivos principais

- `index.html`: estrutura inicial e configuração da API
- `src/styles.css`: visual responsivo, incluindo os temas claro e escuro
- `src/app.js`: autenticação AES-256-GCM, telas, cálculo e histórico local
