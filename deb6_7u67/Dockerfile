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

# Make src directory
RUN mkdir /src

# Add jre tar file to src folder
ADD ./jre /src/jre

# Create jvm (Java Virtual Machine) directory
RUN mkdir -p /usr/lib/jvm

# Uncompress jre to jvm folder
RUN tar -xzf jre-7u67-linux-x64.tar.gz -C /usr/lib/jvm

# Inform the system about the new Java Runtime
RUN update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/jre1.7.0_67/bin/java" 1

# Set the system default Java Runtime
RUN update-alternatives --set java /usr/lib/jvm/jre1.7.0_67/bin/java
