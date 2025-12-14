FROM node:20-alpine

WORKDIR /usr/src/app

# Install dependencies
COPY package.json yarn.lock* ./
RUN if [ -f yarn.lock ]; then yarn install --frozen-lockfile --production; else npm install --production; fi

# Copy source
COPY . .

ENV NODE_ENV=production
EXPOSE 3001

CMD ["node", "server.js"]
