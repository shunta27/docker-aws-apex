FROM mhart/alpine-node:6.11

RUN apk add --update jq curl python py-pip make bash \
  libc6-compat python-dev gcc musl-dev libffi-dev openssl-dev git
# apex
RUN curl https://raw.githubusercontent.com/apex/apex/master/install.sh | sh && apex upgrade
# awscli
RUN pip install --upgrade pip \
    && pip install awscli \
    && pip install awscurl
# workspace
RUN mkdir /usr/share/workspace
WORKDIR /usr/share/workspace
