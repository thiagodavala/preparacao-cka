# Preparação CKA

Anotações com comandos úteis e pontos de atenção para a preparação da certificação CKA

Filtro em uma linha

```
cat ~/.kube/config | grep current | sed -e "s/current-context: //"
```

Schedule in Controlplane

```
tolerations:
- effect: NoSchedule
key: node-role.kubernetes.io/control-plane
nodeSelector:
node-role.kubernetes.io/control-plane: ""
```
