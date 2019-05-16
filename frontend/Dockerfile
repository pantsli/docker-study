# multi-step builds
# Build Phase
# 1. Use node:alpine
FROM node:alpine as builder
WORKDIR /app
# 2. Copy the package.json file
COPY package.json .
# 3. Install dependencies
RUN npm install
COPY . .
# 4. Run 'npm run build'
RUN npm run build
# Run Phase
# 1. Use nginx
FROM nginx
# 2. Copy over the result of 'npm run build'
COPY --from=builder /app/build /usr/share/nginx/html
# 3. Start nginx
