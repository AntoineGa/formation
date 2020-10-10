# using arkade

in case of issues for finding elements in PATH, chage permission:

```bash
nano ~/.profile
```

Add the following to your profile.

```bash
if [ -d "$HOME/.arkade/bin" ] ; then
    PATH="$HOME/.arkade/bin:$PATH"
fi
```

Check if your directory is accessible, and modify permission ([blog post about permissions number](http://linuxcursor.com/linux/linux-file-permission-drwxr-xr-x)) if not:

```bash
ll $HOME/.arkade/

sudo chmod 755 $HOME/.arkade
sudo chmod 755 $HOME/.arkade/bin

source ~/.profile
```
if you have trouble with $HOME/.kube/config.lock
change the permission for $HOME/.kube by doing

```bash
sudo chmod 777 $HOME/.kube
```

```bash
kind create cluster --config kind-config.yaml --name formation

tilt up

go to http://localhost:8080/


kind delete cluster --name formation
```
or

```bash
cd kind
 ./kind-with-registry.sh 
kind get clusters
kind get nodes
kind delete cluster --name kind
```