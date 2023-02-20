# Authenticating with the command line
<!-- q: hot to add url in md -->
<!-- a: [text](url) -->
1. For windows users I suggest to download [Git for Windows](https://gitforwindows.org/) and install it (preferably the bash version and not the gui one).

2. Authenticate using [Github CLI tool](https://cli.github.com/)
    ```
    gh auth login
    ```
    ```
    ? What account do you want to log into? GitHub.com
    ? What is your preferred protocol for Git operations? HTTPS
    ? Authenticate Git with your GitHub credentials? Yes
    ? How would you like to authenticate GitHub CLI? Login with a web browser
    ? Press Enter to open gi
    [...]

3. Without the CLI tool, you can use the [Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) to authenticate with the command line.
    <br/>
    Once you setup the token, you can use it to authenticate with the command line like a password.
    With the following command, you will store your credentials globally on your computer in plain text.
    ```
    git config --global credential.helper store
    ```
    With the following command, you will store your credentials in memory for 15 minutes (default).
    You can change the timeout by setting the `credential.helper` value to `cache --timeout=3600` (1 hour).
    ```
    git config --global credential.helper cache
    git config --global credential.helper 'cache --timeout=3600'
    ```

4. Without the CLI tool, you can use the [SSH Key Pair](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

5. After that you are all set to use git commands, without having to enter your username and password every time you want to push or pull.
    