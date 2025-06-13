# SonarQube Helm Chart

Helm-чарт для развертывания SonarQube + PostgreSQL на Kubernetes (Minikube и др.)
## Установка

### 1. Клонировать репозиторий
```bash
git clone https://github.com/AlishpanovSultan/sonarqube_postgresql_helm_chart.git
```

### 2. Создать секрет с паролем для PostgreSQL
```bash
kubectl create secret generic sonar-postgres-secret --from-literal=postgres-password=<ваш пароль>
```

### 3. Установить чарт
```bash
helm upgrade --install sonarqube-chart ./sonarqube-chart -f sonarqube-chart/values.yaml
```

### 4. Проверка установки
```bash
kubectl get pods
```
