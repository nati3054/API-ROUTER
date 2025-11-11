# Meu Estudo de Caso — CRUD de Produtos (Web + Mobile)

Este repositório contém duas aplicações que implementam um CRUD de produtos consumindo uma API REST pública:

- `web/` — Frontend em React com Vite e Material UI (aplicação para browser).
- `mobile/` — App móvel em React Native com Expo (aplicação para dispositivos móveis).

O objetivo deste projeto é demonstrar navegação entre telas/rotas e consumo de API em duas plataformas.

---

## API utilizada

Base: `https://proweb.leoproti.com.br/produtos`

Formato esperado de um produto:

```json
{
  "id": 0,
  "nome": "string",
  "preco": 0
}
```

---

## Estrutura do repositório

```
meu-estudo-caso/
├── web/      # Projeto React + Vite (frontend web)
└── mobile/   # Projeto Expo + React Native (app mobile)
```

Cada pasta (`web` e `mobile`) possui seu próprio README com instruções específicas. Este README consolida as instruções essenciais para rodar e fazer o deploy.

---

## Web — React + Vite

Descrição: Aplicação web que lista produtos, permite criar, editar e excluir usando Material UI e React Router.

Onde está: `web/`

Principais rotas:

 - `/` → Lista de produtos
 - `/novo` → Formulário para novo produto
 - `/editar/:id` → Editar produto existente

Como rodar localmente (na pasta `web/`):

```bash
cd web
npm install
npm run dev
```

Abra: http://localhost:5173

Observações de deploy:

- Hospede a pasta `web/` no Vercel. Ao adicionar novo projeto no Vercel escolha o repositório e configure o "Root Directory" como `web` (se necessário o Vercel normalmente detecta Vite automaticamente).

Exemplo de passos no Vercel:

1. Login/Crie conta em vercel.com
2. Add New Project → selecione o repositório GitHub
3. Configure Root Directory = `web` (se não detectado)
4. Deploy

---

## Mobile — Expo + React Native

Descrição: App mobile com Expo Router que implementa as mesmas operações de CRUD consumindo a mesma API.

Onde está: `mobile/`

Principais rotas (Expo Router):

 - `/` → Tela inicial
 - `/produtos` → Lista de produtos
 - `/produtos/novo` → Criar produto
 - `/produtos/[id]` → Editar produto

Como rodar localmente (na pasta `mobile/`):

```bash
cd mobile
npm install
expo start
```

Abra o app usando o Expo Go (QR code) ou emulador Android/iOS.

Observações de deploy:

- O app mobile não é hospedado no Vercel. Para distribuição use Expo Application Services (EAS), builds nativas ou publique nas stores (Apple App Store / Google Play) conforme necessidade.

---

## Exemplos de requisições à API

```js
// Listar
axios.get('https://proweb.leoproti.com.br/produtos');

// Criar
axios.post('https://proweb.leoproti.com.br/produtos', { nome: 'Produto', preco: 10 });

// Atualizar
axios.put('https://proweb.leoproti.com.br/produtos/1', { nome: 'Atualizado', preco: 20 });

// Deletar
axios.delete('https://proweb.leoproti.com.br/produtos/1');
```

---

## Qualidade e comportamento

- Tratamento de estados de carregamento e erros implementado nas duas aplicações.
- Validações básicas nos formulários (web e mobile).
- Mobile em TypeScript; Web em JavaScript com MUI.

---

## Créditos e referências

- Doc React: https://react.dev/
- Vite: https://vitejs.dev/
- Material UI: https://mui.com/
- React Router: https://reactrouter.com/
- Expo: https://expo.dev/
- Axios: https://axios-http.com/

---

## Autor(a)

Natalia Ferreira

Projeto desenvolvido como atividade da disciplina "Desenvolvimento Profissional: Estudo de Caso com Rotas e Consumo de API".

---

## Próximos passos sugeridos

- Adicionar CI para deploy automático do `web/` no Vercel (GH Actions).
- Incluir screenshots no README para ilustrar as telas.
- Adicionar instruções de build/distribuição para o app mobile com EAS.

I need to see the README files from your `web` and `mobile` directories to create a proper merged version. Please share those files so I can:

1. Extract the key information from both
2. Identify overlapping sections
3. Consolidate unique features from each
4. Create a unified README with proper structure

Once you provide the content from `/web/README.md` and `/mobile/README.md`, I'll generate the appropriate merged content for the `$SELECTION_PLACEHOLDER$.`


Instalação
1. Clone o repositório:
    git clone <url-do-repositorio>
2. Instale dependências:
    npm install (ou pip install -r requirements.txt)

Uso
- Como iniciar:
  npm start (ou comando equivalente)
- Exemplos de uso:
  Explique rapidamente comandos ou endpoints principais.

Testes
- Rodar testes:
  npm test (ou pytest, etc.)
- Cobertura e recomendações.

Contribuição
- Abra uma issue antes de iniciar alterações significativas.
- Fork > branch com nome descritivo > PR com descrição clara.
- Siga o padrão de lint e testes.

Licença
- Indique a licença desejada (ex.: MIT). Substitua conforme necessário.

Contato
- Autor: Natalia Ferreira

Notas finais
- Substitua os placeholders (item-1, item-2, comandos, URLs) pelas informações reais do seu projeto. Ajuste seções conforme necessário.