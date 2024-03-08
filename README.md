# Instructions to install specific Python versions on your Raspberry Pi

>**Note:** Be sure your Raspberry Pi is up to date. To do so, run below command in terminal.
>```bash
>sudo apt-get update
>```
>```bash
>sudo apt-get upgrade
>```
## Step1: **Install `pyenv`:**
   Use the `pyenv` yet, you can do so using a package manager or by cloning the GitHub repository. Here, I'll provide instructions for using the installation script:

   ```bash
   curl https://pyenv.run | bash
   ```

   Follow the instructions provided after the installation script completes.

## Step2: **Add pyenv to shell configuration file(.bashrc):**
   Follow the instructions provided by the script to add pyenv to your shell configuration file (e.g., .bashrc or .zshrc). After that, restart your shell or run source ~/.bashrc (or source ~/.zshrc) to apply the changes.

   ```bash
   echo 'export PATH="$HOME/.pyenv/bin:$PATH"' >> ~/.bashrc
   echo 'eval "$(pyenv init --path)"' >> ~/.bashrc
   echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.bashrc
   exec "$SHELL"
   ```

## Step3: **Install dependencies:**

   ```bash
   sudo apt-get install --yes libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev llvm libncurses5-dev libncursesw5-dev xz-utils tk-dev libgdbm-dev lzma lzma-dev tcl-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev wget curl make build-essential openssl
   ```

   On other systems, the dependencies might be different. Refer to the [pyenv wiki](https://github.com/pyenv/pyenv/wiki/Common-build-problems) for more information.

## Step4: **Install a specific Python version:**
   Use the `pyenv install` command to install the Python version you want. For example, to install Python 3.9.12:

   ```bash
   pyenv install 3.9.12
   ```

   Replace `3.9.12` with the version you want to install.

## Step5: **Set the global or local Python version:**
   After the installation is complete, you can set the global Python version or set it locally in a specific directory. For example, to set the global version:

   ```bash
   pyenv global 3.9.12
   ```

   To set the version locally in a specific directory, navigate to the directory and run:

   ```bash
   pyenv local 3.9.12
   ```

   Adjust the version number accordingly.

## Step6: **Verify the installation:**
   You can verify that the correct Python version is being used by running:

   ```bash
   python --version
   ```

   It should display the version you installed.

## That's it! You have successfully installed a specific Python version using `pyenv`.
