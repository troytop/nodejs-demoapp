FROM dp.apps.rancher.io/containers/nodejs:20-dev
# Needs authentication - see https://apps.rancher.io/settings/access-tokens

RUN zypper --non-interactive install -y git openssh make awk
RUN useradd -ms /bin/bash node

ARG USERNAME=node
ARG NPM_GLOBAL=/usr/local/share/npm-global

# Add NPM global to PATH.
ENV PATH=${NPM_GLOBAL}/bin:${PATH}

USER node 
WORKDIR /home/node
EXPOSE 3000