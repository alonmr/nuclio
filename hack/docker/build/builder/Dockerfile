# Copyright 2017 The Nuclio Authors.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

ARG NUCLIO_BASE_IMAGE_NAME
ARG NUCLIO_BASE_IMAGE_TAG

FROM --platform=${BUILDPLATFORM} ${NUCLIO_BASE_IMAGE_NAME}:${NUCLIO_BASE_IMAGE_TAG}

WORKDIR /nuclio

ENV CGO_ENABLED=0

COPY go.* ./

RUN go mod download

COPY . .
