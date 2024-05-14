# MyK8Project_VotingApp
This repo is about the very popular voting application which has be hosted by the use of the kubernetes. 

Kubernetes Microservice Project: Voting App
In my recent project, I delved into the world of Kubernetes, focusing on orchestrating multiple containers and managing them effectively. The centerpiece of my exploration was the popular open-source GitHub project known as “The Voting App.” I successfully deployed this application using Kubernetes and Docker concepts, gaining valuable insights along the way.

Key Learnings:

1.Microservice Architecture:
	- The Voting App comprises two frontend components: the “Vote App” and the “Result App.”
	- Users interact with the Vote App to cast their votes, while the Result App displays the percentage of votes cast.
	- Redis, acting as an in-memory database, stores user-casted data.
	- A backend worker, written in .NET, retrieves votes from Redis and updates a PostgreSQL database that maintains the overall vote count.
	- The Result App, developed in Node.js, presents the vote percentage in the user interface.
2. YAML Definition Files:
	- I meticulously crafted YAML definition files for each component of the application, ensuring seamless deployment and management.
3. Service Definitions
	- I created service definition files to establish connectivity between pods spawned by deployments.
	- Explored different service types, including NodePort and ClusterIP.
4. Docker Images
	- I grasped the art of incorporating Docker images within the Kubernetes definition files.
5. External Access:
	- I configured external access from the host environment, allowing seamless interaction with the deployed application.
6. Kubectl Mastery:
	- Leveraging Kubectl commands, I orchestrated the creation of deployments, services, pods, and replica sets.
	- Skillfully scaled pods up and down within the replica set.
	- Made necessary adjustments by editing the definition files.

Tools Utilized:

Docker Desktop: My development environment for containerization.
Kubernetes Minikube Cluster: A single-node cluster for local testing and experimentation.
VS Code: My trusty code editor for writing YAML definitions.
PowerShell: Used for various administrative tasks.
Kubectl: The command-line utility for interacting with the Kubernetes cluster.
Minikube Dashboard: The built-in dashboard for monitoring and managing the Minikube cluster.

Overcoming Challenges:
1. Resource Limit Issue:
	- I encountered resource limit issues during pod creation.
	- To address this, I explored the QoS Class structure, defining resource properties in the YAML files.
 	- Additionally, I adjusted the YAML extension configuration in VS Code by disabling resource limit linters.

2. Worker Pod CrashLoopBackOff:
	- Troubleshooting the issue, I discovered that an incorrect image was specified in the definition file.
	- Verifying the liveness property settings helped resolve the problem.

3. Windows OS Limitation (VoteApp and Result App Access):
	- Windows Docker environments posed limitations regarding IP addresses and ports for the VoteApp and Result App.
	- While ignoring the NodePort service, I worked around this constraint.

In summary, my Kubernetes microservice project provided hands-on experience in container orchestration, service definitions, and effective utilization of Kubernetes tools. I look forward to applying these learnings in future endeavors.
