# useful-links
contains some useful websites and url


https://www.cidevops.com/2018/08/devops-faqs-page.html  Troubleshooting issues

How to configure nginx/apache/iis –webservers on premises https://github.com/miztiik
Ansible===> https://www.golinuxcloud.com/getting-started-with-ansible/

https://dev.to/apium_hub/top-16-devops-blogs-you-should-be-reading-1je2
https://www.digitalocean.com/community/tutorials?subtype=-tech_talk&q=a

https://code.visualstudio.com/download
https://github.com/kunchalavikram1427/YouTube_Series/tree/main/Linux

https://www.middlewareinventory.com/?s=datadog


https://github.com/in28minutes/devops-master-class/tree/master/terraform/backup


dev.to/medium articles
https://www.smartr.me/public/profiles/satish.gawande
linkedin.com/in/satish-gawande-30a58b116
https://my.recruit.net/5c2595e3b9964f0

when docker file runs command inside it, i will create layer oe each command, when you run container image tope of layesrs thin writable con. layer is created
each of the layer adds size to container(when you command it will show in OP as exporitng layers)..
docker history name of image--to see layer,most of space is taken by base image, to reduce layer sizes/reudce no of layers..we used to fetch latest alpine images
in mutistage build we have can multiple stages 1.large base image 2. code 3. depencies--compile--crete executable next stage just copy small base image & final create final doc cont.
1. step --From base imaeg RUN command, in second step From alpine.latest & copy compiled code from previous stage.

https://github.fcom/nemonik/hands-on-DevOps
https://www.linode.com/docs/guides/ansible-adhoc-commands/
https://www.javatpoint.com/powershell-vs-bash-shell
https://github.com/DeekshithSN/Ansible

Extensiv experienc in setting up CI/CD pipeline using tools such Git,Jenkins,Maven,Docker and Ansible.
Experience in working with version control system such as Git.
Good knowledge on working with automation tools used for building,integrating and
deploying software releases to multiple environments.
Good knowledge of virtulization and container technology like Docker.
Experience in creating Dockerfile and working with Docker containers.
Have good knowledge in orchestration tool Kubernetes.
Automated application build and deployment,driving efficiency of code development process.
Have exposure to configuration management tools such Ansible and chef.

Proven experience on a version control system GIT, build tool MAVEN.
Good knowledge of an automation tool for CI/CD pipeline JENKINS
Hands on experience on creating playbook(configuration management tool) CHEF
Hands on experience on creating EC2 instance in AWS
Good knowledge of virtulization and container technology like Docker.
Have exposure to configuration management tools such Ansible and chef.
Have good knowledge in orchestration tool Kubernetes.


   





IPv4--Internet protocol

32 bit logical address
4 octeet
0-255
Ip address-->Network ID + Host ID

Class A---1.0.0.0 to 126.0.0.0--Large NW ---127.0.0.0--look back address..to check If NAC card is working or not--Ping 127.0.0.0 on CMD
Class B---128.0.0.0 to 191.255.0.0
Class C---192.0.0.0 to 223.255.255.0--Small NW

Class D---224-239--use for multitask
Class E---240-255--Research

to check in which class IP add is lying just check first octet of IP eg:-137.20.20.10 is Class B  

Class A--N H H H
B-- N N H H
C-- N N N H --N NW bit-1 H Host bit-0
eg--115.10.0.15--- NW ID--115.0.0.0 just check NW host reserve for resp. classes
196.10.10.10--- NW ID --196.10.10.0

Subnet mask
eg : 115.10.10.20-- 11111111 0000000000 00000000 00000000-- Subnet mask 255.0.0.0

160.10.20.10---255.255.0.0  

128 64 32 16 8 4 2 1
192
1 1 0 0 0 0 0 0

Private IP ranges--Class C 192.168.--,Class A 10---,Class B 172.16--,172.31--

q ? 150.10.20.30
150.10.0.0--NW ID--RESERVE FOR SPECIAL PURPOSE
150.10.255.255--BROADCAST ID--TO USE FOR ALL USERS  
NO OF USABLE IP--2*16-2=65534

11.200.200.200
11.0.0.0
11.255.255.255
2*24-2=


IPv4 Header--20 bytes header(minimum)
20 to 40 --60 bytes(max)
 

IPv4--Limited addresses
to avoid use private ips,Ipv6 or Subnetting

Subnetting--NW within a NW or Logical division of IP addresses

Router--interNetworking device

Switch--use when you want device to communicate within same NW(ID)
 
interfaces of router should have diff-diffrent NW ID

K8s secrets :--
A Secret is an object that contains a small amount of sensitive data such as a password, a token, or a key. Such information might otherwise be put in a Pod specification or in a container image. Using a Secret means that you don't need to include confidential data in your application code.

How to check disk space. 2.Write any python script.
3.Describe the type of load balance and the difference between them. 4.Explain CI/CD process. 5.Question from monitoring tools you are using in a project
ps -ef | grep java
Tell me the code/template to create 2 VM's without auto scaling group and launch configuration where a VM goes down it should automatically create a new on spot instance

kubernetes deployment with readiness and liveliness probe.

deployed Kubernetes cluster and how many nodes I have created and
what are their specifications

apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  selector:
    matchLabels:
      app: nginx
  replicas: 2 # tells deployment to run 2 pods matching the template
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.14.2
        ports:
        - containerPort: 80

Explain cicd pileline Using kubernetes and docker

Round Robin algorithm Subnetting

Serverless architechture

Linux boot process



K8s::
K8s-­-> YAML--> appversion/kind/metadata/sepc: template/status

NS--default/kube-system/kube-public/kube-node-lease

Services-This is used for port mapping and network load balancing. 1. Target port -  It’s is pod or container port 2. port - Refers to service port. 3. hostPort -  Refers to host machine port to make it accessible from external network.
ClusterIP/Node-port/LB/ExternalName/headless/ingress.
Cluster ip--pod to pod comm within cluster
Node-port- Access pods from an external network and performs network load balancing. ie Even if a pod is running on a specific slave, we can access it from other slave in the cluster.

LB--external conectivity. assigns a public ip for all the nodes combined together.

DC - RC/RS/key-value,Equility( = !=) setbased(IN , NOT IN) with key

vol. node local memory--emptydir(for conts. within a pod can share vol)/hostpath(pod within a cluster can share)
cloud vol - aws EBS
file-sahring ; NFS
distributed file-systems-CephFS/GlusterFS
Specail vol-pvc/secrets/configMap

NodeSelector and Affinity focus on attracting the pods to a certain set of nodes. On the other hand they are opposite. Taints and Tolerations used to repel a set of pods from the nodes i.e they allow a node to repel a set of pods

persistent volume (PV) is the "physical" volume on the host machine that stores your persistent data. A persistent volume claim (PVC) is a request for the platform to create a PV for you, and you attach PVs to your pods via a PVC

kubectl api-resources | grep -iE 'KIND|replication'
k explain pod(to get api version)

inspect pods--k get pods/k decrsibe pods pod-name/k logs podname
Deployment---
•Replicas: how many copies Pod
strategy: how Pods should be updated
Recreate/Rollingupdate
•selector: to identify how labels are matched against the Pod
template: Pod spec.

RC -- label sel./replica count/pod template

if we are updating the pod with 4 replicas, DaemonSets are used to ensure that some or all of your K8s nodes run a copy of a pod, which allows you to run a daemon on every node. using rolling update stra. and mentioned maxunav.=1 n maxsurge =1 then while updating we have atleast 3 n max 5 of running pods.

apiVersion: v1
kind: Pod
metadata:
 name: nginx-pod
 labels:
  author: sunil
  type: reverse-proxy
spec:
 containers:
  - name: appserver
    image: nginx

/=]]ateful set manage stateful applications. it manages the deployment and scaling of a set of Pods and provides guarantees about the ordering and uniqueness of these Pods.unlike deployments, it doesn’t create ReplicaSet rather it creates the Pod with a unique naming convention. eg . If you create a StatefulSet with name counter, it will create a pod with name counter-0, counter-1, counter-2, etc
Deployments are used for stateless applications whereas StatefulSets for stateful applications
The pods in a deployment are interchangeable whereas the pods in a StatefulSet are not.
In statefulset pod`s names are in sequential order on the other hand in deployment pod`s names are unique.
A headless service handles the pods’ network ID in StatefulSets, while deployments require a service to enable interaction with pods
In a deployment, the replicas all share a volume and PVC, while in a StatefulSet each pod has its own volume and PVC.


Imagine you have a Linux server with a web server application which stores the logs inside /var/log/app.log . Later the log entries from this file are processed to generate alarms to a central logging server. Suppose you had to apply some patch to the logging service so even your application gets impacted as both are running on the same server.
So we add a sidecar container along with the main container, now the application will run in the main container while sidecar container will be used for the logging service. So now any patch to be applied to logging service can be done separately and can be re-deployed without any impacts to the main application container.

Volumes are defined at the Pod level and mounted at the container level, which means you can use any type of volume or PVC and make it available for many containers to use. Decoupling the volume definition from the volume mount also allows selective sharing, so one container may be able to see Secrets whereas the others can’t.

A role binding grants the permissions defined in a role to a user or set of users. It holds a list of subjects (users, groups, or service accounts), and a reference to the role being granted. A RoleBinding grants permissions within a specific namespace whereas a ClusterRoleBinding grants that access cluster-wide.

Every pod is associate with a Service-Account, which represents the identity of the app running in the pod. The token file
holds the ServiceAccount’s authentication token. When an app uses this token to connect to the API server, the authentication plugin authenticates the ServiceAccount and passes the ServiceAccount’s username back to the API server core. Service-Account usernames are formatt like this: ServiceAccounts are the way for an application running inside a pod to authenticate itself with the API server.

Helm chart--Package manager/allows to pakage,confgure,deploy app/services onto clusters
client--CLI for deploying, managing repo. interacting with helm-library
chart-- contains necessary def. to run app. /package of pre-configured k8s resources.
release--instance of chart running on cluster.same chart can be deployed mutiliple times in mult.env.
Secrets as default storage driver in helm3(helm2 used ConfigMap)
json schema validatin(port no. mandatory),Release name required
Repo--charts reside and shared with others

liveness probes to know when to restart a container. ... Kubernetes uses readiness probes to decide when the container is available for accepting traffic.The readiness probe is used to control which pods are used as the backends for a service




akash2112gawande@gmail.com

runtime instance of image/actual instantiation of image just ike how an object is an inst or instanc of class. we can create any no of cont from single image..cont can not change their underlying docker image lighter,faster n efficient than VM



111. Where are you in DevOps transformation in your company? What level of maturity team is currently at?
2. What kind of DevOps tools are you using?
3. What level of automation is currently in place in the team?
4. What would be my day to day activities, if I am selected?
5. How are you collaborating within the team? are you using any tools like Slack?

6. Are you completely migrating to cloud such as AWS or Azure or on-prem also
Setup ubuntu ec2 install
set up K8s cluster in ec2--kubectl version & install latest version--& launch ec2 for nodes
create ec2--Ansible server--cd .ssh>>ls-->>cat id_rsa.pub--key genrate copy key to establosh comm with K8s master---cd .shh--ls--autorised keys-- paste keys from ansible serever---
in ansible sever check connection-- ssh -i id_rsa root@ pivate ip of K8s master--
Ansible@ip(we are in k8s master)--cd /opt--ls--we can seee kubenrtes/plybooks etc...
sudo mkdir k8s-lab(after ginpving sudo permission)
Now, create palybook to create docker image--
host--ansible server
Create host file Vi host
[Ansible-sever]
[kubernetes] private ip of K8s matser
Nagios/





CICD-- im using Git as VCM, once dev coomit any code it will be depositeed in Github and once code is ready we we are CI--for builing Maven where there is pom.xml file defined dependicies of the project artificat ID project Id nad if we want run some junit test caess and o/p of jobs where we need to store in pom.xlm..we  configure that in manage Jenkins in Jenkins and we have clone Jenkins with Gihub whenevre new job is configured for particlar project then n brach --jenkinsfile



ew item is maven project and will be haing source code --Git give credential..once hadsharek is done Jenkins will be ready to pull that data while running the job ..Maven home setting --Maven& javen home path and after tht we neeed to give target where all target is rung form pom xmland goal what will be goal from job pakcing or cleanr..post build activity--biul sccuess notification to biuld is succeful..build no  
 

https://github.com/miztiik/server-migration-onprem-to-aws
o The Linux supported file systems are ext2, ext3, ext4, xfs, vfat, cdfs, hdfs, iso9660 ...etc., The ext2, ext3, ext4 file systems are widely used in RHEL-6 and xfs file system is introduced on RHEL-7. The vfat file system is used to maintain a common storage between Linux and Windows O/S.
o The cdfs file system is used to mount the CD-ROMs and the hdfs file system is used to mount DVDs. The iso9660 file system is used to read CD/DVD.iso image format files in Linux O/S.
