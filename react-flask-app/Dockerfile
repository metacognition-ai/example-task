FROM alpine

WORKDIR /app
COPY . /app
RUN rm -rf /app/node_modules

RUN apk add npm yarn python3 py3-pip bash
RUN npm install
RUN pip install --break-system-packages flask python-dotenv

ENTRYPOINT ["/bin/bash", "-c"]
CMD ["yarn start-api & yarn start"]

