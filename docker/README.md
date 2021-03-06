<!--
  ~ Licensed to the Apache Software Foundation (ASF) under one or more
  ~ contributor license agreements.  See the NOTICE file distributed with
  ~ this work for additional information regarding copyright ownership.
  ~ The ASF licenses this file to You under the Apache License, Version 2.0
  ~ (the "License"); you may not use this file except in compliance with
  ~ the License.  You may obtain a copy of the License at
  ~
  ~      http://www.apache.org/licenses/LICENSE-2.0
  ~
  ~ Unless required by applicable law or agreed to in writing, software
  ~ distributed under the License is distributed on an "AS IS" BASIS,
  ~ WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  ~ See the License for the specific language governing permissions and
  ~ limitations under the License.
  -->
# Building Docker images

You can build the docker image provided in this directory by using the following command:

```
docker build -t unomi .
```

# Unomi Docker Image

## Running Unomi
Unomi requires ElasticSearch so it is recommended to run Unomi and ElasticSearch using docker-compose:
```
docker-compose up
```
You will need to wait while Docker builds the containers and they boot up (ES will take a minute or two). Once they are up you can check that the Unomi services are available by visiting http://localhost:8181/cxs in a web browser.

## Environment variables

When you start the `unomi` image, you can adjust the configuration of the Unomi instance by passing one or more environment variables on the `docker run` command line.

- **`ELASTICSEARCH_HOST`** - The IP address of hostname for ElasticSearch
- **`ELASTICSEARCH_PORT`** - The port for ElasticSearch
