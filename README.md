   Copyright 2016 ThoughtWorks, Inc

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.

#Find me in Kakuma Frontend local dependencies.

Vagrant boxes for Elasticsearch and Postgres which we used for local development and testing without having to connect to AWS hosted environments.

The vagrant file for Postgres has been designed to accept a password from an external environment variable. An example of the syntax to invoke vagrant up with the correct variable set is in the postgres/provisionPostgres.sh
The goal is to never save the DB password in the git repository, but set it from outside somehow (for secrets management, we were using consumer password vaults, and sharing passwords through those.)

We copied the Elasticsearch .deb (Ubuntu install file) into the repo for convenience, and to avoid repeatedly downloading it. The deb will probably need updating from time to time. Start by checking here: https://www.elastic.co/downloads/elasticsearch
