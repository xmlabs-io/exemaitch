FROM mcr.microsoft.com/vscode/devcontainers/universal:linux

COPY containers/vscode-linux/requirements.txt /tmp/pip-tmp/
RUN pip3 --disable-pip-version-check --no-cache-dir install -r /tmp/pip-tmp/requirements.txt
RUN sudo su - -c "rm -rf /tmp/pip-tmp"

RUN npm install -g aws-cdk
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "/tmp/awscliv2.zip"
RUN unzip -qq /tmp/awscliv2.zip -d /tmp
RUN sudo /tmp/aws/install
RUN sudo su - -c "rm -rf /tmp/aws /tmp/awscliv2.zip"
RUN sudo su - codespace -c "mkdir -p /tmp/pre-commit-init"
COPY [".pre-commit-config.yaml", "/tmp/pre-commit-init/.pre-commit-config.yaml"]
RUN sudo su - codespace -c "cd /tmp/pre-commit-init && git init && pre-commit install --install-hooks"
