FROM node:12-alpine

ENV PORT=80 

# Metadata as defined in OCI image spec annotations - https://github.com/opencontainers/image-spec/blob/master/annotations.md
LABEL org.opencontainers.image.title="Team_1_challenge_1" \
      org.opencontainers.image.description="Let's_do_some_linux" \
      org.opencontainers.image.authors="Bezawit_Kendie" \
      org.opencontainers.image.vendor="Vender_here"

# add debugging utilities
RUN apk --no-cache add \
  curl \
  ca-certificates \
  jq \
  less \
  vim

# bundle app and install dependencies 
COPY . /app
WORKDIR /app
RUN npm install

# run application
EXPOSE $PORT
CMD npm start
