ДЗ к лекции 2
- Создан Dockerfile c кастомным образом nginx
- Создан манифест web-pod.yaml для деплоя контэйнера с nginx
- Создан манифест frontend-pod.yaml для деплоя контейнера frontend
- Создан исправленный манифест rontend-pod-healthy.yaml с добавленными переменными окружения

ДЗ к лекции 3
- Созданы манифесты replicaset и deployment для сервисов frontend, paymentservice
- Созданы манифесты paymentservice-deployment-bg.yaml и paymentservice-deployment-reverse.yaml в них реализованы сценарии Blue-Green Deployment и Reverse Rolling Update
- Создан манифест node-exporter-daemonset.yaml с возможностью запуска на мастер-нодах