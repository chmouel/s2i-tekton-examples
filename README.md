Build templates for tekton.

* Configure your secret in `s2i.secrets.yaml` the dockerconfig part specially
* Apply the files `s2i.secrets.yaml`, `serviceaccount-s2i.yaml`, `task-s2i.yaml`
* Use the examples in taskruns/* and apply to yours, for example for a nodejs
  based project edit the file and modify the `Source` parameters to your own
  source and `ImageOutput` to your own docker registry output (which match with your secrets's dockerconfig)

Limitations: Only works when you are allowed to access to the docker socket (i.e: not openshfit atm)
