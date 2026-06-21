# nginx-шлюз стэка: вшитый конфиг + отдача SPA-статики.
#
# В образ вшивается nginx.conf — на деплое больше не нужен bind-mount
# ./nginx/nginx.conf (а значит и checkout репо ради одного файла).
#
# SPA-статика по-прежнему приходит из named volume `frontend-dist`,
# который заполняет init-контейнер showcase-frontend, монтируется в
# /usr/share/nginx/html (см. docker-compose.yml).
FROM nginx:1.27-alpine

COPY nginx.conf /etc/nginx/conf.d/default.conf
