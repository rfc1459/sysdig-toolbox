# sysdig-toolbox

Quick'n'dirty way to run Sysdig as a privileged Pod on every worker node in a k8s cluster using containerd as its runtime.

## Usage

Apply the manifest with `kubectl apply -f sysdig-toolbox.yaml`, the scap driver *will not be built and loaded by default*.
You'll have to `kubectl exec` into every pod and run `scap-driver-loader` with whatever flag you like.

Then use `sysdig` or `csysdig` as you see fit.
