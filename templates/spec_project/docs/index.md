# **Guia de Preenchimento do Template: Spec Project**

Este template facilita a criação de um pipeline de automação no GitHub, permitindo gerar artefatos Kong/Kubernetes a partir de um arquivo de especificação OpenAPI 3. A configuração é integrada ao Backstage, com opções de customização para repositório, visibilidade e detalhes do projeto.

## **Preenchendo os Campos do Template**

### 1. **Catalog Details**
   **Descrição**: Nesta seção, forneça informações básicas do projeto, incluindo o nome e o proprietário.

   - **componentId (Obrigatório)**: Nome único do projeto. Deve ser um identificador válido para uso em sistemas, com letras minúsculas, números, `.` (ponto), `_` (underline) e `-` (hífen).
     - **Exemplo**: `viacep_app`

   - **description (Opcional)**: Descrição breve do projeto para ajudar outras pessoas a entender o propósito dele.
     - **Exemplo**: "Geração de artefatos Kong e Kubernetes para APIs do Viacep."

   - **owner (Obrigatório)**: Nome do grupo ou equipe responsável pelo projeto no formato "group:nome_grupo".
     - **Exemplo**: `group:default/engenharia`

### 2. **Upload Openapi 3 File**
   **Descrição**: Selecione ou faça o upload do arquivo de especificação OpenAPI 3 que será utilizado para gerar os artefatos.

   - **UploadSpec**: Faça upload do arquivo OpenAPI 3. Este arquivo será processado para gerar artefatos específicos de Kong/Kubernetes.
     - **Formato Recomendado**: YAML
     - **Dicas**: Verifique se a especificação OpenAPI está em conformidade com a versão 3 para evitar problemas de compatibilidade.

### 3. **Spec Configuration**
   **Descrição**: Adicione tags para categorizar e organizar o projeto.

   - **specTags**: Insira tags separadas por vírgula para classificar o projeto.
     - **Exemplo**: `api, kubernetes, kong`

### 4. **Input your Kubeconfig**
   **Descrição**: Insira o conteúdo do seu arquivo `kubeconfig`, que será utilizado para conexão com o cluster Kubernetes.

   - **VKDR_LOCAL_KUBECONFIG (Obrigatório)**: Cole o conteúdo do seu `kubeconfig` neste campo. 
     - **Dicas**: Mantenha este arquivo atualizado e seguro, pois ele contém informações sensíveis de acesso ao cluster Kubernetes.

### 5. **Choose a location**
   **Descrição**: Escolha a localização e a visibilidade do repositório no GitHub onde o projeto será armazenado.

   - **repoUrl (Obrigatório)**: URL do repositório GitHub onde o pipeline será criado. Use o seletor para definir a URL baseada no `componentId`.
     - **Exemplo**: `https://github.com/seu-usuario/viacep_app`

   - **visibility**: Selecione a visibilidade do repositório entre `public` e `private`.
     - **Padrão**: `private`

---

## **Links de Saída**

Após a conclusão dos passos, o Backstage irá gerar os seguintes links:

- **Repository**: Link direto para o repositório GitHub do projeto.
- **Open in Catalog**: Link para acessar o componente no catálogo do Backstage.

