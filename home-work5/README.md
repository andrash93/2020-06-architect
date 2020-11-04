# Запуск
create and set namespace

    kubectl create namespace auth
    kubectl config set-context --current --namespace=auth

install app

    helm install account-app ./account-service/account-chart/account-app-chart/
    helm install auth-app ./auth-service/auth-chart/auth-app-chart/
    