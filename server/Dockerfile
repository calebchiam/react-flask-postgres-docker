FROM python:alpine3.7

ENV CODE_DIR=/code

RUN adduser -D -g '' anon
RUN apk add --no-cache build-base postgresql-dev

COPY --chown=anon:anon . ${CODE_DIR}/

WORKDIR ${CODE_DIR}

RUN pip install -r requirements.txt

USER anon

CMD make dev
