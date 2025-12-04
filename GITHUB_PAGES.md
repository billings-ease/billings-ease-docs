# Como Publicar no GitHub Pages

## Configuração Inicial

1. **Crie o repositório `billings-ease-docs` na organização:**
   - Acesse: https://github.com/organizations/billings-ease/repositories/new
   - Nome do repositório: `billings-ease-docs`
   - Selecione **Public** ou **Private** conforme necessário
   - **Não** inicialize com README, .gitignore ou licença (já temos os arquivos)

2. **Configure o GitHub Pages:**
   - No repositório `billings-ease-docs`, vá em **Settings** > **Pages**
   - Em **Source**, selecione a branch principal (geralmente `main` ou `master`)
   - Em **Folder**, selecione `/` (raiz) ou `/docs` se a estrutura estiver na pasta docs
   - Clique em **Save**

3. **Aguarde alguns minutos** para o GitHub processar

4. **Acesse sua documentação em:**
   - `https://billings-ease.github.io/billings-ease-docs/`

## Configurando o Repositório Local

1. **Inicialize o git na pasta docs:**
   ```bash
   cd docs
   git init
   git add .
   git commit -m "docs: adiciona documentação inicial"
   ```

2. **Conecte ao repositório remoto:**
   ```bash
   git remote add origin https://github.com/billings-ease/billings-ease-docs.git
   git branch -M main
   git push -u origin main
   ```

## Atualizando a Documentação

1. Faça as alterações nos arquivos Markdown
2. Commit e push para o repositório:
   ```bash
   git add .
   git commit -m "docs: atualiza documentação"
   git push
   ```
3. O GitHub Pages atualiza automaticamente (pode levar alguns minutos)

## Estrutura de Arquivos

```
docs/
├── _config.yml          # Configuração do Jekyll
├── index.md             # Página principal
├── README.md            # Documentação adicional
├── .nojekyll            # Desabilita Jekyll (se necessário)
└── images/
    └── screenshots/     # Imagens da documentação
```

## Notas

- **Organização GitHub**: `billings-ease`
- **Repositório**: `billings-ease-docs`
- **URL da Documentação**: `https://billings-ease.github.io/billings-ease-docs/`
- O arquivo `.nojekyll` está presente para garantir que o GitHub Pages não processe arquivos Jekyll desnecessários
- Se preferir usar Jekyll, remova o `.nojekyll` e use o `_config.yml`
- As imagens devem estar em caminhos relativos (ex: `images/screenshots/...`)
- Para organizações, a URL do GitHub Pages segue o padrão: `https://[organizacao].github.io/[nome-do-repo]/`

## Alternativas

Se preferir uma documentação mais avançada, considere:
- **MkDocs**: Documentação baseada em Markdown
- **Docusaurus**: Framework de documentação do Facebook
- **VitePress**: Gerador de sites estáticos do Vue

