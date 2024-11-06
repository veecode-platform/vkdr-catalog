# **Guide to Filling Out the Template: GitHub Pages Simple Blog Template**

This template automates the creation of a basic blog on GitHub Pages, including publishing and registration in Backstage. Follow these instructions to complete the required fields and successfully set up your blog.

## **Filling Out the Template Fields**

### 1. **Provide Some Basic Information**
   **Description**: In this section, you'll provide basic information about the blog, such as its name, description, and repository owner.

   - **repository-name (Required)**: Unique blog name, used as the component identifier.
     - **Format**: Lowercase letters, numbers, `.` (dot), `_` (underscore), and `-` (hyphen).
     - **Example**: `my_simple_blog`

   - **description (Optional)**: A short description about the purpose or content of the blog.
     - **Example**: "Blog on DevOps tutorials and updates."

   - **owner (Required)**: Component owner in the format "group:group/name". This field is pre-filled as `group:default/demo`, but you can change it to the desired owner.
     - **Example**: `group:default/engineering`

### 2. **Input Your GitHub PAT Token**
   **Description**: Provide your GitHub Personal Access Token (PAT). This token is necessary to create and manage the repository on GitHub.

   - **PERSONAL_GITHUB_TOKEN (Required)**: A token with permissions to create and publish repositories.
     - **Tips**: Ensure that the token has the necessary permissions to read and write to repositories. Configure it on GitHub with the minimum recommended permissions (repository and GitHub Pages).
     - **Where to find it**: [Link to generate token](https://github.com/settings/tokens)

### 3. **Choose a Location**
   **Description**: Set the repository creation location and link it to your GitHub.

   - **repoUrl (Required)**: GitHub repository URL where the blog will be hosted.
     - **Format**: Use the selection field to choose the host (only `github.com` is allowed). The value will be automatically filled with the `repository-name`.
     - **Example**: `https://github.com/your-username/my_simple_blog`

---

## **Execution Steps**

After filling out the parameters, Backstage will automatically execute the following steps:

1. **Fetch Skeleton + Template**
   - Downloads the skeleton and applies the provided data to the template files.

2. **Publish to GitHub**
   - Publishes the repository on GitHub with the `repository-name` and sets the repository as `public`. **Note**: All repositories created by this template will be public.

3. **Enable GitHub Pages**
   - Backstage will automatically enable GitHub Pages for the repository, setting the main branch (`main`) as the source and the `root` directory as the source directory.
   - **Generated Endpoint**: The blog address will be:
     ```
     https://<your-username>.github.io/<repository-name>/
     ```
     **Example**: If the `repository-name` is `my_simple_blog` and your GitHub username is `your-username`, the blog address will be:
     ```
     https://your-username.github.io/my_simple_blog/
     ```

4. **Register in the Backstage Catalog**
   - Registers the repository and adds the component in the Backstage catalog using the path `/catalog-info.yaml`.

---

## **Output Links**

After completing the steps, Backstage will generate useful links:

- **Repository**: Direct link to the GitHub blog repository.
- **Open in Catalog**: Link to access the component in the Backstage catalog.
- **Blog Endpoint**: Direct link to the blog on GitHub Pages:
  ```
  https://<your-username>.github.io/<repository-name>/
  ```
