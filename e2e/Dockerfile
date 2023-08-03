# SPDX-FileCopyrightText: 2023 The Pion community <https://pion.ly>
# SPDX-License-Identifier: MIT

FROM golang:1.17-alpine3.13

RUN apk add --no-cache \
  chromium \
  chromium-chromedriver

ENV CGO_ENABLED=0

COPY . /go/src/github.com/tihomirptotev/webrtc
WORKDIR /go/src/github.com/tihomirptotev/webrtc/e2e

CMD ["go", "test", "-tags=e2e", "-v", "."]
