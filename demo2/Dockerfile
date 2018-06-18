FROM centos:centos6

# Enable EPEL for Node.js
RUN rpm -Uvh http://download.fedoraproject.org/pub/epel/6/i386/epel-release-6-8.noarch.rpm

# Install Node.js and nmp
RUN yum install -y -q npm

# Copy source code
ADD src/ /src

# Install app dependencies
RUN npm config set strict-ssl false
RUN cd /src; npm install

# Run the WebServer
CMD ["node", "/src/index.js"]

