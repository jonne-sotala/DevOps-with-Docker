FROM node

EXPOSE 5000
WORKDIR = /usr/app/src
COPY . . 

ENV REACT_APP_BACKEND_URL=http://localhost:8080

RUN npm install
RUN npm run build
RUN npm install -g serve

RUN useradd -m user
USER user

CMD ["serve", "-s", "-l", "5000", "build"]
