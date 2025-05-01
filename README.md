# Setting Up the 'new-project' Repository and Development Branch

This guide provides step-by-step instructions on how to:
1. Create a new repository named `new-project` on GitHub.
2. Clone the repository to your local machine.
3. Create a `development` branch for working on new features.
4. Push the `development` branch to GitHub.

---

## Step-by-Step Instructions

Follow these steps to set up your project repository and development branch:

### 1. Create the Repository on GitHub

* Go to [GitHub](https://github.com).
* Log in to your account.
* Click the **+** icon in the top-right corner and select **New repository**.
* Enter the **Repository name**: `new-project`.
* Choose **Public** or **Private** visibility according to your needs.
* **Recommended:** Check the box to **Add a README file**. You can also add a `.gitignore` (e.g., for your specific programming language/framework) and choose a license if needed.
* Click **Create repository**.

### 2. Clone the Repository Locally

* On your new GitHub repository page (`github.com/<your-username>/new-project`), click the green **<> Code** button.
* Copy the **HTTPS** or **SSH** URL provided.
* Open your terminal or command prompt (like Git Bash, PowerShell, or Terminal).
* Navigate to the directory on your computer where you want to store the project using the `cd` command.
    ```bash
    # Example: Navigate to your development projects folder
    cd path/to/your/projects
    ```
* Clone the repository using the URL you copied:
    ```bash
    # Replace <repository_url> with the actual URL
    git clone <repository_url>
    ```
* Change your current directory to the newly cloned project folder:
    ```bash
    cd new-project
    ```

### 3. Create the `development` Branch Locally

* Inside the `new-project` directory, create a new branch named `development` and switch to it using a single command:
    ```bash
    git checkout -b development
    ```
    * This command performs two actions:
        1.  `git branch development` (creates the new branch)
        2.  `git checkout development` (switches your working environment to that branch)
* You are now working on the `development` branch locally. You can verify this by running:
    ```bash
    git branch
    ```
    (The current branch will have an asterisk `*` next to it).

### 4. Push the `development` Branch to GitHub

* To make the `development` branch available on the remote GitHub repository and set up tracking, run:
    ```bash
    git push -u origin development
    ```
    * `origin` refers to your remote repository on GitHub.
    * `-u` (or `--set-upstream`) links your local `development` branch to the remote `development` branch. This allows you to use `git pull` and `git push` without specifying `origin development` in the future for this branch.

---

## You're All Set!

Now you have:
* A GitHub repository called `new-project`.
* A local copy of the repository.
* A `main` branch (usually the default for production-ready code).
* A `development` branch (both locally and on GitHub) where you can work on new features without directly affecting `main`.

**Typical Workflow:**
* Make your changes while on the `development` branch.
* Add and commit your changes:
    ```bash
    git add .
    git commit -m "Your descriptive commit message"
    ```
* Push your changes to the remote `development` branch:
    ```bash
    git push origin development
    # Or just 'git push' if upstream is set
    ```
* When features are ready, you can merge the `development` branch into `main` (often done via Pull Requests on GitHub).
* To switch between branches:
    ```bash
    git checkout main
    git checkout development
    ```
