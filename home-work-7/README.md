# Запуск
create and set namespace

    kubectl create namespace order
    kubectl config set-context --current --namespace=order

install app

    helm install order ./order-app-chart/
     