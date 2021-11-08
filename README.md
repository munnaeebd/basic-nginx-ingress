# basic-nginx-ingress

~~~
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: mn-ingress
  annotations:
          kubernetes.io/ingress.class: "nginx"
spec:
  rules:
    - host: hello-world.info
      http:
        paths:
          - path: /
            pathType: Prefix
            backend:
              service:
                name: myapp-service
                port:
                  number: 80

~~~
