# Install Compose on Linux systems

### Prerequisites
- On Linux systems, first install the [Docker Engine](https://github.com/genral73/docker#install-docker-engine-on-ubuntu-or-debian), then come back here for instructions on installing Compose on Linux systems.

### Install Compose
1. Run this command to download the current stable release of Docker Compose:
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

2. Apply executable permissions to the binary:
```bash
sudo chmod +x /usr/local/bin/docker-compose
```

3. If the command docker-compose fails after installation, check your path. You can also create a symbolic link to /usr/bin or any other directory in your path.
```bash
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

4. Test the installation.
```bash
docker-compose --version
```
> output: docker-compose version 1.25.5, build 1110ad01

5. Optionally, install command completion for the bash and zsh shell, place the completion script in /etc/bash_completion.d/.
```bash
 sudo curl -L https://raw.githubusercontent.com/docker/compose/1.25.5/contrib/completion/bash/docker-compose -o /etc/bash_completion.d/docker-compose
```
