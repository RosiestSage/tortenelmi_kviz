FROM nginx

WORKDIR /app

COPY . .

RUN npm install
RUN npm run build

FROM nginx AS final

COPY --from=build /app/dist /user/share/nginx/html