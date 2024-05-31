ARG VARIANT=1.22-bookworm
FROM golang:${VARIANT}

# [Optional] Uncomment the next line to use go get to install anything else you need
RUN go get -x <your-dependency-or-tool>

# [Optional] Uncomment this section to install additional OS packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
     && apt-get -y install --no-install-recommends curl tar zsh git neovim

# Install oh-my-zsh
RUN sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" || true

# Set zsh as the default shell
RUN chsh -s $(which zsh)

