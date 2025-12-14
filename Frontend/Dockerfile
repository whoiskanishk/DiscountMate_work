FROM node:20-alpine

WORKDIR /app

ENV CI=true

# Install dependencies
COPY package.json yarn.lock* ./
RUN if [ -f yarn.lock ]; then yarn install --frozen-lockfile; else npm install; fi

# Copy source
COPY . .

EXPOSE 19006

# Start expo in web mode (serves on 19006 by default)
CMD ["yarn", "web"]
