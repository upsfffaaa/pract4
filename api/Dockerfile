# Используем официальный Node.js образ на основе Alpine Linux
FROM node:alpine

# Устанавливаем рабочую директорию внутри контейнера
WORKDIR /time-app

# Копируем package.json и package-lock.json из локальной папки в контейнер
COPY package.json package-lock.json ./

# Устанавливаем зависимости
RUN npm install

# Копируем все остальные файлы в контейнер
COPY ./src ./src
COPY index.mjs ./

# Открываем порт для API
EXPOSE 5000

# Запускаем приложение API
CMD ["npm", "start"]
