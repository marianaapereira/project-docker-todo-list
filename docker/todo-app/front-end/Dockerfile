# front-end/Dockerfile

# rode a partir da imagem do node na versão 14;
FROM node:14-alpine

# exponha a porta 3000;
EXPOSE 3000

# trabalhe em um diretório denominado app;
WORKDIR /app

# adicione o arquivo node_modules.tar.gz à imagem;
ADD node_modules.tar.gz /app

# copie todos os arquivos da pasta front-end para a imagem. (você pode usar o caminho relativo, lembrando que a Dockerfile está em ./docker/todo-app/front-end/Dockerfile);
COPY . .

# inicie a aplicação com o comando npm start respeitando as seguintes restrições:
# ao subir um container baseado na imagem buildada a partir desse Dockerfile, o comando npm deve ser rodado sempre;
ENTRYPOINT [ "npm" ]

# ao subir um container baseado na imagem buildada a partir desse Dockerfile, deve ser possível sobrescrever o comando start.
CMD [ "start" ]