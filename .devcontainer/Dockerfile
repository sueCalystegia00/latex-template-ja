FROM ghcr.io/pddg/latex:3.1.0

WORKDIR /workdir

# Avoid warnings by switching to noninteractive
ENV DEBIAN_FRONTEND=noninteractive

# Configure apt and install packages
RUN apt-get update \
&& apt-get -y install --no-install-recommends apt-utils dialog 2>&1 \
&& apt-get -y install git iproute2 procps lsb-release \
&& apt-get -y install latexdiff \
&& curl -fsSL https://deb.nodesource.com/setup_20.x | bash - \
&& apt-get install -y --no-install-recommends nodejs \
&& apt-get autoremove -y \
&& apt-get clean -y \
&& rm -rf /var/lib/apt/lists/*

# Switch back to dialog for any ad-hoc use of apt-get
ENV DEBIAN_FRONTEND=dialog