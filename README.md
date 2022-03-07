# ChainlinkKubernetes-aws
README.md
ellan Chainlink Kubernetes Deployment
This repo is the ellan Kubernetes setup for deploying Chainlink nodes. Each deployment deploys 2 Chainlink nodes and a postgresql databse to be used by the nodes



##create configmap
kubectl create configmap node-env --from-literal ROOT=/chainlink --from-literal LOG_LEVEL=debug --from-literal ETH_CHAIN_ID=1 --from-literal CHAINLINK_TLS_PORT=0 --from-literal SECURE_COOKIES=false --from-literal ALLOW_ORIGINS=* --from-literal ETH_URL=<INSERT-ETH-WSS> --from-literal DATABASE_URL=<INSERT-DATBASE-URL> --from-literal DATABASE_TIMEOUT=0 -n chainlink-ocr
  

#deploy
 
  kubectl apply -f deploy.yaml
  kubectl get all -n namesapce
  kubectl logs -n kube-system pod
  
  
