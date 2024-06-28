# podman-tanzu-build
Quick setup after intalling Podman to configure it to successully run tanzu buid cli.

# Add custom cert:
  ```
  podman machine ssh
  cd /etc/pki/ca-trust/source/anchors
  vi harbor-h2o-4-11809.pem <<--- your cert
  update-ca-trust
  exit
  ```
  Restart podman
  
# Define the alias and the symbolic link:
  ```
  alias docker=podman`
  ln -s docker.sock /var/folders/2m/xfk1bkhs4pg4k_wsck1zjc400000gq/T/podman/podman-machine-default-api.sock <<---fetch this from podman dashboard
  ```

# Now you can tanzu build cli!
