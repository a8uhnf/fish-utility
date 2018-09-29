# Display-k8s-cluster

Add below command in fish_prompt function to display kubernetes cluster name in fish command-line.


```console

set CONTEXT (cat ~/.kube/config | grep "current-context:" | sed "s/current-context: //")
set_color purple
printf "k8s: %s" $CONTEXT
printf "\n"
set_color normal

```

PS: normally `fish_prompt` exits in `~/.config/fish/functions/fish_prompt.fish`. If not present you can create `fish_prompt` function and add these lines.
If already exist append above lines in the `fish_prompt` function.
