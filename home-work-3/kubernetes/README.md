# Зпуск
create and set namespace

    kubectl create namespace monitoring
    kubectl config set-context --current --namespace=monitoring

install prometheus

    helm install prom stable/prometheus-operator -f prometheus.yaml --atomic
    
install nginx-ingress

    helm install nginx stable/nginx-ingress -f nginx-ingress.yaml

port-forward to grafana

    kubectl port-forward service/prom-grafana 9000:80

install app

    helm install mywork ./crud-app-chart/