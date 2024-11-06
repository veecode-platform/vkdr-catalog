# **Template Filling Guide: Spec Project**

This template facilitates the creation of an automation pipeline in GitHub, allowing the generation of Kong/Kubernetes artifacts from an OpenAPI 3 specification file. The configuration is integrated with Backstage, with customization options for repository, visibility, and project details.

## **Filling in the Template Fields**

### 1. **Catalog Details**
   **Description**: In this section, provide basic project information, including the name and owner.

   - **componentId (Required)**: A unique project name. It must be a valid identifier for use in systems, consisting of lowercase letters, numbers, `.` (dot), `_` (underscore), and `-` (hyphen).
     - **Example**: `viacep_app`

   - **description (Optional)**: A brief description of the project to help others understand its purpose.
     - **Example**: "Generation of Kong and Kubernetes artifacts for Viacep APIs."

   - **owner (Required)**: The name of the group or team responsible for the project in the format "group:team_name".
     - **Example**: `group:default/engineering`

### 2. **Upload Openapi 3 File**
   **Description**: Select or upload the OpenAPI 3 specification file to be used to generate the artifacts.

   - **UploadSpec**: Upload the OpenAPI 3 file. This file will be processed to generate Kong/Kubernetes-specific artifacts.
     - **Recommended Format**: YAML
     - **Tips**: Ensure that the OpenAPI specification complies with version 3 to avoid compatibility issues.

### 3. **Spec Configuration**
   **Description**: Add tags to categorize and organize the project.

   - **specTags**: Enter tags separated by commas to classify the project.
     - **Example**: `api, kubernetes, kong`

### 4. **Input your Kubeconfig**
   **Description**: Enter the contents of your `kubeconfig` file, which will be used to connect to the Kubernetes cluster.

   - **VKDR_LOCAL_KUBECONFIG (Required)**: Paste the contents of your `kubeconfig` in this field. 
     - **Tips**: Keep this file updated and secure, as it contains sensitive access information for the Kubernetes cluster.

### 5. **Choose a location**
   **Description**: Choose the location and visibility of the GitHub repository where the project will be stored.

   - **repoUrl (Required)**: The GitHub repository URL where the pipeline will be created. Use the selector to define the URL based on the `componentId`.
     - **Example**: `https://github.com/your-username/viacep_app`

   - **visibility**: Select the repository visibility between `public` and `private`.
     - **Default**: `private`

---

## **Output Links**

After completing the steps, Backstage will generate the following links:

- **Repository**: Direct link to the GitHub repository of the project.
- **Open in Catalog**: Link to access the component in the Backstage catalog.
