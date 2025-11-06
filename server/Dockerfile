# 1️⃣ 选择基础镜像
FROM node:20-alpine 

# 2️⃣ 设置工作目录（后续命令都在 /app 下执行）  inside a container
WORKDIR /app

# 3️⃣ 先复制 package.json 和 package-lock.json，用于缓存 npm install
COPY package*.json ./

# 4️⃣ 安装依赖
RUN npm install

# 5️⃣ 再复制项目的全部文件到容器中
COPY . .

# 6️⃣ 声明容器暴露的端口
EXPOSE 5000

# 7️⃣ 容器启动时要执行的命令
CMD ["node", "server.js"]
