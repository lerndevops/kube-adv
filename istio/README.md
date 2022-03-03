// Istio Setup

kubectl create -f https://raw.githubusercontent.com/lerndevops/kube-adv/master/istio/istio-init-1.10.3.yml

kubectl get all -n istio-system    --> see all are up


kubectl create -f https://raw.githubusercontent.com/lerndevops/kube-adv/master/istio/kiali.yml

kubectl create -f https://raw.githubusercontent.com/lerndevops/kube-adv/master/istio/jaeger.yaml

kubectl apply -f https://raw.githubusercontent.com/lerndevops/kube-adv/master/istio/prometheus.yaml

kubectl create -f https://raw.githubusercontent.com/lerndevops/kube-adv/master/istio/grafana.yaml

kubectl apply -f https://raw.githubusercontent.com/lerndevops/kube-adv/master/istio/label-default-namespace.yml



// Deploy App

kubectl apply -f https://raw.githubusercontent.com/lerndevops/kube-adv/master/istio/1-fleemanapp-full-stack.yml

access app using service fleetman-webapp


Access Kiali and Jaeger Dashboards for UI and Tracing (both are nodePort services)


// Resolution



kubectl apply -f https://raw.githubusercontent.com/lerndevops/kube-adv/master/istio/resolution-1-fleemanapp-full-stack.yml


Now check kiali and jaeger response times. App also loads faster
