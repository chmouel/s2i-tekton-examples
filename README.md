Build templates for tekton.

* Configure your secret in `s2i.secrets.yaml` the dockerconfig part specially
* Apply the files `s2i.secrets.yaml`, `serviceaccount-s2i.yaml`, `task-s2i-*.yaml`

There is multiple task and taskruns for the different language, use the appropriate one.

if you need to use a custom builder you can do directly from your taskrun, for
example if you want a specific nodejs tag for the nodejs image you can
add this to your inputs :

```json
    - name: Builder
      value: nodeshift/centos7-s2i-nodejs:11.x
```

which would override the default builder,

Limitations: Only works when you are allowed to access to the docker socket (i.e: not openshfit atm)
