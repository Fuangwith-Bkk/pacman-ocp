oc login
oc new-project apacman
cd pacman-ocp/helm
helm install pacman ./pacman/ --namespace apacman 
helm uninstall pacman