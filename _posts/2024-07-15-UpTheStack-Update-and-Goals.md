## Up The Stack: Update & Goals

It has almost been a year since I first started this site and the idea of walking through the graduated and incubating projects on the CNCF landscape. We have covered two of those projects so far in one video along with an intro video, then life and work in general got really busy so I am hitting the reset button and I am going to try and attack this again now. You might have seen that over the last few weeks I have been sharing posts here and actually throughout the past 12 months we have a few blogs covering some areas relevant to the cloud native ecosystem. 

The premise of the project is still the same to shine a light on those projects and provide a way to not only understand the project, the why and what does it do but to also get hands-on with the project and learn more about these building blocks for your cloud native stack. 

All I can say is let's see how we go with the 56 projects now and try and cover more than just the two! 

The one thing that has changed is the ability to at least begin with is to create the videos alongside the written content here. But we will see how that goes too. 


# CNCF Projects
We will use this list below to work through the projects. 


**Provisioning**

Provisioning encompasses tools and services for automating the configuration, management, and scaling of cloud-native environments. This category includes automation, security, container registries, and key management solutions.

*Automation & Configuration*
- [ ] Cloud Custodian (I)
  - [Cloud Custodian](https://cloudcustodian.io/): A tool that allows you to define rules to manage and automate cloud resources.
- [ ] KubeEdge (I)
  - [KubeEdge](https://kubeedge.io/): Extends native containerized application orchestration and device management to hosts at the edge.

*Key Management*
- [ ] Spiffe (G)
  - [Spiffe](https://spiffe.io/): Provides a secure identity framework for distributed systems.
- [ ] Spire (G)
  - [Spire](https://spiffe.io/spire/): Implements the Spiffe specifications to provide identity to services across environments.

*Security & Compliance*
- [ ] Falco (G)
  - [Falco](https://falco.org/): Monitors and detects anomalous activity in your containerized environments.
- [ ] Open Policy Agent (G)
  - [Open Policy Agent](https://www.openpolicyagent.org/): A policy engine that unifies policy enforcement across the stack.
- [ ] TUF (G)
  - [TUF](https://theupdateframework.io/): A framework for securing software update systems.
- [ ] Cert-Manager (I)
  - [Cert-Manager](https://cert-manager.io/): Automates the management and issuance of TLS certificates.
- [ ] in-toto (I)
  - [in-toto](https://in-toto.io/): Provides a framework to protect the integrity of the software supply chain.
- [ ] Keycloak (I)
  - [Keycloak](https://www.keycloak.org/): An open-source identity and access management solution.
- [ ] Kyverno (I)
  - [Kyverno](https://kyverno.io/): A policy engine designed for Kubernetes.
- [ ] Notary (G)
  - [Notary](https://notaryproject.dev/): Provides a way to sign and verify the authenticity of content.

*Container Registry*
- [ ] Harbor (G)
  - [Harbor](https://goharbor.io/): An open-source container image registry that secures images with role-based access control.
- [ ] Dragonfly (I)
  - [Dragonfly](https://d7y.io/): An intelligent P2P-based image and file distribution system.

**Runtime**

Runtime focuses on the execution of containerized applications and includes projects related to container runtimes, networking, and storage. These tools ensure efficient and reliable application performance in cloud-native environments.

*Cloud Native Storage*
- [ ] Rook (G)
  - [Rook](https://rook.io/): A storage orchestrator for Kubernetes that turns storage software into self-managing, self-scaling services.
- [ ] CubeFS (I)
  - [CubeFS](https://cubefs.io/): An open-source cloud-native distributed storage platform.
- [ ] Longhorn (I)
  - [Longhorn](https://longhorn.io/): A distributed block storage system for Kubernetes.

*Container Runtime*
- [ ] ContainerD (G)
  - [ContainerD](https://containerd.io/): An industry-standard core container runtime.
- [ ] cri-o (I)
  - [cri-o](https://cri-o.io/): An open-source lightweight container runtime for Kubernetes.

*Cloud Native Network*
- [ ] Cilium (I)
  - [Cilium](https://cilium.io/): Provides networking, security, and observability for cloud-native environments.
- [ ] CNI (I)
  - [CNI](https://github.com/containernetworking/cni): A container network interface for Kubernetes to ensure consistent network connectivity.

**Orchestration & Management**

Orchestration & Management involves tools that coordinate and manage the deployment, scaling, and operations of containerized applications. This category includes service meshes, API gateways, scheduling, orchestration, and service discovery solutions.

*Coordination & Service Discovery*
- [ ] CoreDNS (G)
  - [CoreDNS](https://coredns.io/): A DNS server that chains plugins and is optimized for Kubernetes.
- [ ] etcd (G)
  - [etcd](https://etcd.io/): A distributed key-value store that provides reliable data management for Kubernetes.

*Service Mesh*
- [ ] Istio (I)
  - [Istio](https://istio.io/): Connects, secures, controls, and observes services.
- [ ] Linkerd (G)
  - [Linkerd](https://linkerd.io/): A lightweight service mesh for Kubernetes.

*API Gateway*
- [ ] Emissary Ingress (I)
  - [Emissary Ingress](https://www.getambassador.io/about/emissary-ingress/): An open-source Kubernetes-native API Gateway.

*Scheduling & Orchestration*
- [ ] Keda (I)
  - [Keda](https://keda.sh/): A Kubernetes-based Event Driven Autoscaler.
- [ ] Kubernetes (G)
  - [Kubernetes](https://kubernetes.io/): An open-source system for automating the deployment, scaling, and management of containerized applications.
- [ ] Crossplane (I)
  - [Crossplane](https://crossplane.io/): Extends Kubernetes to enable the management of services and infrastructure.
- [ ] Karmada (I)
  - [Karmada](https://karmada.io/): A Kubernetes management system that supports multi-cloud and multi-cluster.
- [ ] Knative (I)
  - [Knative](https://knative.dev/): Helps developers build, deploy, and manage modern serverless workloads.
- [ ] KubeFlow (I)
  - [KubeFlow](https://www.kubeflow.org/): A machine learning toolkit for Kubernetes.
- [ ] Volcano (I)
  - [Volcano](https://volcano.sh/): A batch system built on Kubernetes.

*Service Proxy*
- [ ] Envoy (G)
  - [Envoy](https://www.envoyproxy.io/): An open-source edge and service proxy designed for cloud-native applications.
- [ ] Contour (I)
  - [Contour](https://projectcontour.io/): An open-source Kubernetes ingress controller.

*Remote Procedure Call*
- [ ] gRPC (I)
  - [gRPC](https://grpc.io/): A high-performance, open-source universal RPC framework.

**App Definition & Development**

App Definition & Development provides tools for defining, building, and deploying applications. This category includes continuous integration and delivery (CI/CD) tools, databases, application definitions, and image build tools, streamlining the development process.

*Continuous Integration & Delivery*
- [ ] Argo (G)
  - [Argo](https://argoproj.github.io/): An open-source container-native workflow engine for Kubernetes.
- [ ] Flux (I)
  - [Flux](https://fluxcd.io/): A set of continuous and progressive delivery solutions for Kubernetes.
- [ ] Keptn (I)
  - [Keptn](https://keptn.sh/): A control plane for continuous delivery and automated operations.
- [ ] OpenKruise (I)
  - [OpenKruise](https://openkruise.io/): Extends Kubernetes with more powerful and efficient workloads.

*Database*
- [ ] TiKV (I)
  - [TiKV](https://tikv.org/): A distributed key-value database compatible with the Redis API.
- [ ] Vitess (G)
  - [Vitess](https://vitess.io/): A database clustering system for horizontal scaling of MySQL.

*Application Definition & Image Build*
- [ ] Helm (G)
  - [Helm](https://helm.sh/): The Kubernetes package manager.
- [ ] Artifact Hub (I)
  - [Artifact Hub](https://artifacthub.io/): A web-based application that enables finding, installing, and publishing Kubernetes packages.
- [ ] Backstage (I)
  - [Backstage](https://backstage.io/): An open platform for building developer portals.
- [ ] BuildPacks (I)
  - [BuildPacks](https://buildpacks.io/): A framework for building container images from source code.
- [ ] dapr (I)
  - [dapr](https://dapr.io/): A portable, event-driven runtime that makes it easy to build resilient, stateless, and stateful applications.
- [ ] KubeVela (I)
  - [KubeVela](https://kubevela.io/): A modern application delivery platform that makes deploying applications across hybrid, multi-cloud environments easier.
- [ ] KubeVirt (I)
  - [KubeVirt](https://kubevirt.io/): Extends Kubernetes by adding support for running virtual machine workloads.
- [ ] Operator Framework (I)
  - [Operator Framework](https://operatorframework.io/): An open-source toolkit to manage Kubernetes native applications, called Operators.

*Streaming & Messaging*
- [ ] cloudevents (G)
  - [CloudEvents](https://cloudevents.io/): A specification for describing event data in a common way.
- [ ] NATS (I)
  - [NATS](https://nats.io/): A connective technology for adaptive edge and distributed systems.
- [ ] Strimzi (I)
  - [Strimzi](https://strimzi.io/): Provides a way to run Apache Kafka on Kubernetes.

**Observability and Analysis**

Observability and Analysis includes tools for monitoring, logging, and tracing applications and infrastructure. These tools provide visibility into system performance, helping to detect issues, analyze performance, and ensure reliability.

*Observability*
- [ ] FluentD (G)
  - [FluentD](https://www.fluentd.org/): An open-source data collector for unified logging layers.
- [ ] Jaeger (G)
  - [Jaeger](https://www.jaegertracing.io/): An open-source, end-to-end distributed tracing system.
- [ ] Prometheus (G)
  - [Prometheus](https://prometheus.io/): An open-source monitoring system with a dimensional data model and query language.
- [ ] Cortex (I)
  - [Cortex](https://cortexmetrics.io/): A horizontally scalable, highly available, multi-tenant, long-term storage for Prometheus.
- [ ] OpenMetrics (I)
  - [OpenMetrics](https://openmetrics.io/): A project to create an open standard for transmitting metrics at scale.
- [ ] OpenTelemetry (I)
  - [OpenTelemetry](https://opentelemetry.io/): Provides APIs, libraries, agents, and instrumentation to enable observability.
- [ ] Thanos (I)
  - [Thanos](https://thanos.io/): An open-source project that provides highly available Prometheus setups with long-term storage capabilities.

*Chaos Engineering*
- [ ] Chaos Mesh (I)
  - [Chaos Mesh](https://chaos-mesh.org/): A cloud-native Chaos Engineering platform that orchestrates chaos in Kubernetes environments.
- [ ] Litmus (I)
  - [Litmus](https://litmuschaos.io/): Provides tools for practicing chaos engineering in Kubernetes.

*Feature Flagging*
- [ ] OpenFeature (I)
  - [OpenFeature](https://openfeature.dev/): An open standard for feature flag management.


For more detailed information on each project, you can visit the CNCF [incubating projects](https://www.cncf.io/projects/#incubating) and [graduated projects](https://www.cncf.io/projects/#graduated) pages.

 