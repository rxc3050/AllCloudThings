# Kubernetes

Kubernetes Overview:
1. Nodes:

Nodes are the individual machines (VMs or physical servers) in a Kubernetes cluster.
Each node runs container runtime software (e.g., Docker) and communicates with the control plane.
Nodes can be categorized as "worker nodes" responsible for running application workloads.
2. Pods:

Pods are the smallest deployable units in Kubernetes.
They can contain one or more containers that share network and storage resources.
Pods are scheduled onto nodes, and they can be replicated for scalability.
3. Services:

Services define a network endpoint for a set of pods.
They enable load balancing and provide a stable DNS name for accessing pods.
There are different types of services, including ClusterIP, NodePort, and LoadBalancer, for various use cases.
4. Controllers:

Controllers manage the desired state of pods and ensure that the actual state matches the desired state.
Common controllers include ReplicaSets, Deployments, and StatefulSets.


## Getting started with Kubernetes

- Install 

Deployment Steps using IAC (Infrastructure as Code):
To deploy applications on Kubernetes using IAC principles, you can follow these steps:

1. Set up a Kubernetes Cluster:
Use a tool like kubeadm, managed Kubernetes services (e.g., EKS, AKS, GKE), or a Kubernetes distribution to create a cluster.
Define the cluster infrastructure in IAC (e.g., Terraform or AWS CloudFormation templates) if needed.

2. Define Kubernetes Manifests:
Write Kubernetes YAML manifests (IAC) for your application components, including Deployments, Services, ConfigMaps, and Secrets.
Manifests describe the desired state of your application and how it should be deployed.

3. Version Control:
Store your Kubernetes manifests in version control (e.g., Git) to track changes and collaborate with your team.
Use version control best practices, including branches, pull requests, and code reviews.

4. Apply Manifests:
Use the kubectl apply command to apply your manifests to the Kubernetes cluster.
This will create and manage the desired resources (pods, services, etc.) in the cluster.

5. Continuous Integration (CI) and Continuous Deployment (CD):
Set up CI/CD pipelines using tools like Jenkins, GitLab CI/CD, or others.
Automate the testing, building, and deployment of your application containers and manifests.

6. Monitor and Scale:
Use Kubernetes-native monitoring tools (e.g., Prometheus, Grafana) to monitor the health of your applications.
Implement autoscaling for your application pods to handle increased traffic.

7. Rollout Updates:
Use Kubernetes controllers like Deployments to manage application updates and rollbacks gracefully.
Apply new manifests with updated versions of your application containers.

8. Backup and Disaster Recovery:
Implement backup and disaster recovery strategies for persistent data and configurations.
Regularly back up critical resources, such as Persistent Volumes and ConfigMaps.

9. Security:
Implement Kubernetes RBAC (Role-Based Access Control) to manage access and permissions.
Use network policies to control traffic between pods and secure your cluster.


10. Documentation and Collaboration:
- Maintain clear and up-to-date documentation for your Kubernetes resources and configurations.
- Collaborate with development and operations teams to ensure smooth application deployment and management.


# Code Examples:

- [frontend-app-example](kubernetes/frontend-app-example.md)
- Deploy using following command:
    - ```yaml 
        kubectl apply -f frontend-app.yaml
    ```

## Tips&Tricks

- 


