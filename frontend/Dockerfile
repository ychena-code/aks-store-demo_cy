# 使用官方 Node.js 镜像作为构建环境（假设前端是 React 或类似的静态网站）
FROM node:16 AS build

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build

# 使用 nginx 作为生产环境容器，托管静态文件
FROM nginx:alpine

COPY --from=build /app/build /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
