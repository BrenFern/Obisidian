- **Low-level container runtimes:** runc and crun.
- **Sandboxed Low-level container runtimes:** gVisor and Kata
- **High-level container runtimes:** CRI-O, containerd, Podman and Docker.

	Container runtimes are fundamental components of Kubernetes. It is responsible for managing the execution and lifecycle of containers, and it is necessary to choose and install a container runtime into each worker node in the Kubernetes cluster to run PODs.
	
	The Container Runtime Interface (CRI) is the specification in charge of the communication between the kubelet and the high-level runtimes. The CRI defines gRPC APIs that allow the kubelet to interact as a client with different runtimes. CRI performs an abstraction layer for high-level runtimes.
	
	The high-level runtimes use a lower-level container runtime to run and manage the components required to deploy and operate containers. Open Container Initiative (OCI) specifications allow the integration of different high- and low-level runtimes.

	The OCI Runtime Specification is one of the three specifications defined by OCI. It describes the requirements for the runtime environment, the interfaces for containers, and the minimum set of functionalities that high and low-level runtimes must provide to be considered OCI compliant.
	
- **Managed Kubernetes service :** 