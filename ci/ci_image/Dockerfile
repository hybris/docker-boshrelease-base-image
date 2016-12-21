FROM alpine

# Install required tools:
RUN apk --no-cache add bash git

# Install Ruby and BOSH gem:
RUN apk --no-cache add ruby \
    && gem install bosh_cli --no-rdoc --no-ri --source http://rubygems.org

# Install spruce:
ADD https://github.com/geofffranks/spruce/releases/download/v1.8.6/spruce-linux-amd64 /usr/bin/spruce
RUN chmod +x /usr/bin/spruce

# Cleanup:
RUN rm -rf /var/cache/apk/*
