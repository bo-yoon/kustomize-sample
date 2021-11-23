# kustomize-sample
kustomize yaml 파일 샘플



<br>

## mac os


```
brew install kustomize
```
<br>

## linux kustomize-install.sh 실행

```

sh kustomize-install.sh 

```


<br>

## yaml 파일 생성

```

### kustomization.yaml 생성
kustomize create --namespace=metallb-system --resources namespace.yaml,metallb.yaml,metallb-config.yaml



### yaml 내용
kustomization.yaml


apiVersion: kustomize.config.k8s.io/v1beta1
kind: Kustomization
resources:
- namespace.yaml
- metallb.yaml
- metallb-config.yaml
namespace: metallb-system


### yaml 내용
kustomize build | kubectl apply -f -

```


<br>

