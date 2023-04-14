# golang-skaffold
- 2023.04.14 - 팀그릿 백엔드팀에서 진행한 Bazel(Gazelle) + Skaffold(Kubernetes) 스터디입니다.
- 지식을 공유해 주신 주찬님! 감사합니다 :)

## Bazel Build
```bash
$ bazel build //:gazelle
```

## Starting Skaffold 
```bash
$ minikube start
😄  Darwin 13.2.1 의 minikube v1.30.1
✨  기존 프로필에 기반하여 docker 드라이버를 사용하는 중
👍  minikube 클러스터의 minikube 컨트롤 플레인 노드를 시작하는 중
🚜  베이스 이미지를 다운받는 중 ...
🔄  Restarting existing docker container for "minikube" ...
🐳  쿠버네티스 v1.26.3 을 Docker 23.0.2 런타임으로 설치하는 중
🔗  Configuring bridge CNI (Container Networking Interface) ...
🔎  Kubernetes 구성 요소를 확인...
    ▪ Using image gcr.io/k8s-minikube/storage-provisioner:v5
🌟  애드온 활성화 : storage-provisioner, default-storageclass
🏄  끝났습니다! kubectl이 "minikube" 클러스터와 "default" 네임스페이스를 기본적으로 사용하도록 구성되었습니다.
$ skaffold dev
Generating tags...
 - hello-world -> hello-world:c95a1dc-dirty
Checking cache...
 - hello-world: Found Locally
Tags used in deployment:
 - hello-world -> hello-world:6af8a825b6cb86653fb076081372ea00e6009923263f065f1cfee80fbc295390
Starting deploy...
 - deployment.apps/hello-world created
Waiting for deployments to stabilize...
 - deployment/hello-world is ready.
Deployments stabilized in 2.131 seconds
Port forwarding deployment/hello-world in namespace default, remote port 3000 -> http://127.0.0.1:3000
Listing files to watch...
 - hello-world
Press Ctrl+C to exit
Watching for changes...
[hello-world] 
[hello-world]  ┌───────────────────────────────────────────────────┐ 
[hello-world]  │                   Fiber v2.43.0                   │ 
[hello-world]  │               http://127.0.0.1:3000               │ 
[hello-world]  │       (bound on host 0.0.0.0 and port 3000)       │ 
[hello-world]  │                                                   │ 
[hello-world]  │ Handlers ............. 2  Processes ........... 1 │ 
[hello-world]  │ Prefork ....... Disabled  PID ................. 1 │ 
[hello-world]  └───────────────────────────────────────────────────┘ 
[hello-world] 
```