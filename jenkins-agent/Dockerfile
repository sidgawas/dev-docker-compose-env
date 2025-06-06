FROM jenkins/inbound-agent

USER root
# Install Python and pip (Debian-based example)
RUN apt-get update && \
    apt-get install -y curl && \
    rm -rf /var/lib/apt/lists/

# Install uv (Astral's uv tool) and move to /usr/local/bin
RUN curl -LsSf https://astral.sh/uv/install.sh | sh && \
    mv /root/.local/bin/uv /usr/local/bin/uv

# Or for the full-featured version:
# RUN pip3 install 'uvicorn[standard]'

USER jenkins