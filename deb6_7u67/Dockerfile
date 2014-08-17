# Copyright 2014 Jimmy Beaudoin

# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at

# http://www.apache.org/licenses/LICENSE-2.0

# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# By using this file, you accept the Oracle Binary Code License Agreement
# for Java SE available at http://www.oracle.com/technetwork/java/javase/terms/license/index.html

FROM debian:6.0

MAINTAINER Jimmy Beaudoin <contact@jim-beaudoin.com>

# Update the system
RUN apt-get update
RUN apt-get -y upgrade

# Install wget
RUN apt-get -y install wget

# Make src directory
RUN mkdir /src

# Add jre tar file to src folder
ADD ./jre /src/jre
