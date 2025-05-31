# My Personal Blog

# Content on this website is still as the same as shown on the template, I am going to modify in the future.

**Live Site:** [wuweb.westeurope.cloudapp.azure.com](wuweb.westeurope.cloudapp.azure.com)

Welcome to the source code repository for my personal website and blog! This site is built using the static site generator [Hugo](https://gohugo.io/) and is a space where I share my learning experience.

Beyond the content itself, this project also serves as a practical learning ground for implementing DevOps principles and building an automated deployment pipeline.

## About This Site

*   **Content:** Blog posts, articles, and pages written in Markdown.
*   **Static Site Generator:** Hugo
*   **Deployment:** This site is automatically built and deployed to a self-managed Azure Virtual Machine running Nginx, served securely over HTTPS.

## DevOps & CI/CD Demonstration

The real magic behind this site (from a technical perspective) is its automated deployment setup! I've documented the entire CI/CD pipeline, server configuration, Nginx setup, and custom Git hooks in a separate repository dedicated to showcasing these DevOps practices.

👉 **[View Detailed CI/CD Setup & Configuration Files](https://github.com/wusshit/my-hugo-vps-deploy-setup.git)** 👈

This "configuration demo" repository includes:
*   The exact `post-receive` Git hook script used for automation.
*   The Nginx server block configuration (for HTTP and HTTPS).
*   Notes on the Azure VM setup and other server-side configurations.
*   A detailed explanation of the deployment workflow.

This separation helps keep this repository focused on the site's content and the other repository focused on the operational infrastructure.

## Technologies Used (Site Content - This Repo)

*   **Static Site Generation:** Hugo
*   **Content Management:** Markdown, Git
*   **Version Control:** Git & GitHub
*   **HTTPS/SSL:** Let's Encrypt

*(For technologies related to deployment, server, and CI/CD, please see the [CI/CD Setup & Configuration Repository](https://github.com/wusshit/my-hugo-vps-deploy-setup.git)*

## Local Development

To run or contribute to the content of this site locally:

1.  Clone this repository:
    ```bash
    git clone https://github.com/wusshit/My-Blog.git
    ```
2.  Navigate into the project directory:
    ```bash
    cd [Your-Actual-Hugo-Site-Repo-Name]
    ```
3.  Ensure you have [Hugo (Extended version)](https://gohugo.io/installation/) installed.
4.  If the theme is managed as a Git submodule:
    ```bash
    git submodule update --init --recursive
    ```
5.  Run the local Hugo server:
    ```bash
    hugo server -D
    ```
    The site will typically be available at `http://localhost:1313`.

## How to Deploy (Overview)

While the detailed scripts are in the linked configuration repository, the deployment for *this* site is triggered via a `git push` to a specific remote on my Azure VM. The server then automatically builds and deploys the latest version.

1.  Commit local changes to this repository.
2.  Push to `origin` (GitHub).
3.  Push to the `vps-deploy` remote to trigger the live deployment via `ssh` 

## Future Plans

I plan to continue developing both the content of this blog and enhancing its underlying infrastructure:

*   Adding more articles about my understanding and learning experience in my practical exploration
*   Further exploring DevOps tools for automation, configuration management, and containerization. *(Refer to the [CI/CD Setup & Configuration Repository](https://github.com/wusshit/my-hugo-vps-deploy-setup.git) for more specific infrastructure plans.)*
