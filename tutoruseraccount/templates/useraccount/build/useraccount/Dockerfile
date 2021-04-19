FROM debian

LABEL MAINTAINER=MP
RUN apt-get update && apt-get -y upgrade

# Installing python packages with nano, vim and telnet
RUN apt-get -y install python3-dev default-libmysqlclient-dev build-essential nano vim telnet

RUN apt-get -y install python3-pip  git curl 
RUN pip3 install mysqlclient

# Installing node and React dependencies
RUN apt-get -y install node-gyp nodejs npm && npm install npm@latest -g

# Making directory
RUN mkdir -p /openedx/useraccount
WORKDIR /openedx/useraccount

# cloning the MFA repository
RUN git clone https://github.com/edx/frontend-app-account /openedx/useraccount

COPY package.json /openedx/useraccount/package.json
COPY env.development /openedx/useraccount/.env.development
COPY env /openedx/useraccount/.env
RUN cd /openedx/useraccount
## Installing and building app
RUN npm install && npm run build 


CMD ["npm", "start" ]










