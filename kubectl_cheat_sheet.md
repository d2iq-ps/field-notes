# Kubernetes Operations Cheat sheet

## For exams knowg a few quick ways to get some details is crucial


Agnostic to Konvoy

## alias a few commands 
alias k=“kubectl”
alias ka=“kubectl apply -f” 
alias kgp=“kubectl get pods”
alias kcc=“kubectl config current-context”

```fish
alias kcc=“kubectl config current-context”
funcsave kcc
```

## Useful kubectl commands

- Get all images in cluster, use -n \[namespaces\] to parse down

```bash
kubectl get pods -A -o jsonpath="{range .items[*]}{.spec.containers[*].image}{'\n'}{end}"
```

- Similar command to get all iamges.

```bash
kubectl get pods -A -o jsonpath="{.items[*].spec.containers[*].image}"
```

Not as nicely printed.

To nicely print you will need a new line, for the newline you need to get each line separately and print a new line at the end, hence command one.






