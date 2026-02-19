# MavenBuild-SpringbootApplication-AKS-Deployment

helm install vault hashicorp/vault \
  --set "global.openshift=true" \
  --set "server.dev.enabled=true" \
  --set "server.image.repository=docker.io/hashicorp/vault" \
  --set "server.image.tag=1.15.2" \
  --set "injector.enabled=false" \
  --set "server.rbac.create=false" \
  --set "server.serviceAccount.create=false" \
  --set "server.route.enabled=true"
