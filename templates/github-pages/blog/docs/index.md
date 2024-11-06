# **Guia de Preenchimento do Template: Github Pages Simple Blog Template**

Este template automatiza a criação de um blog básico no GitHub Pages, com publicação e registro no Backstage. Siga estas instruções para completar os campos necessários e configurar seu blog com sucesso.

## **Preenchendo os Campos do Template**

### 1. **Provide some simple information**
   **Descrição**: Nesta seção, você fornecerá informações básicas sobre o blog, como o nome, a descrição e o proprietário do repositório.

   - **nome-do-repositorio (Obrigatório)**: Nome único do blog, usado como identificador do componente.
     - **Formato**: Letras minúsculas, números, `.` (ponto), `_` (underline) e `-` (hífen).
     - **Exemplo**: `meu_blog_simples`

   - **description (Opcional)**: Descrição curta sobre o objetivo ou conteúdo do blog.
     - **Exemplo**: "Blog sobre tutoriais e novidades da área de DevOps".

   - **owner (Obrigatório)**: Proprietário do componente no formato "group:grupo/nome". Esse campo é pré-preenchido como `group:default/demo`, mas você pode alterá-lo para o proprietário desejado.
     - **Exemplo**: `group:default/engenharia`

### 2. **Input your Github PAT token**
   **Descrição**: Forneça o seu Personal Access Token (PAT) do GitHub. Este token é necessário para criar e gerenciar o repositório no GitHub.

   - **PERSONAL_GITHUB_TOKEN (Obrigatório)**: Um token com permissões para criação e publicação de repositórios.
     - **Dicas**: Certifique-se de que o token tem as permissões necessárias para ler e escrever em repositórios. Configure-o pelo GitHub com permissões mínimas recomendadas (repositório e GitHub Pages).
     - **Onde encontrar**: [Link para gerar token](https://github.com/settings/tokens)

### 3. **Choose a location**
   **Descrição**: Defina o local de criação do repositório e vincule-o ao seu GitHub.

   - **repoUrl (Obrigatório)**: URL do repositório GitHub onde o blog será hospedado.
     - **Formato**: Use o campo de seleção para escolher o host (somente `github.com` é permitido). O valor será preenchido automaticamente com o `nome-do-repositorio`.
     - **Exemplo**: `https://github.com/seu-usuario/meu_blog_simples`

---

## **Passos de Execução**

Após o preenchimento dos parâmetros, o Backstage irá executar automaticamente os seguintes passos:

1. **Fetch Skeleton + Template**
   - Faz o download do esqueleto e aplica os dados fornecidos aos arquivos do template.

2. **Publicação no GitHub**
   - Publica o repositório no GitHub com o `nome-do-repositorio` e define o repositório como `public`. **Observação**: Todos os repositórios criados por este template serão públicos.

3. **Habilitar GitHub Pages**
   - O Backstage habilitará automaticamente o GitHub Pages para o repositório, configurando a branch principal (`main`) como fonte e o diretório `root` como diretório de origem.
   - **Endpoint Gerado**: O endereço do blog será:
     ```
     https://<seu-usuario>.github.io/<nome-do-repositorio>/
     ```
     **Exemplo**: Se o `nome-do-repositorio` for `meu_blog_simples` e seu nome de usuário GitHub for `seu-usuario`, o endereço do blog será:
     ```
     https://seu-usuario.github.io/meu_blog_simples/
     ```

4. **Registro no Catálogo do Backstage**
   - Registra o repositório e adiciona o componente no catálogo do Backstage usando o caminho `/catalog-info.yaml`.

---

## **Links de Saída**

Após a conclusão dos passos, o Backstage irá gerar links úteis:

- **Repository**: Link direto para o repositório GitHub do blog.
- **Open in Catalog**: Link para acessar o componente no catálogo do Backstage.
- **Blog Endpoint**: Link direto para o blog no GitHub Pages:
  ```
  https://<seu-usuario>.github.io/<nome-do-repositorio>/
  ```

