
KUBERNETES-CURVE                                    
Creating a cluster using KinD          
Note: Docker should be installed

Install Kind on Linux -               
Use the curl command to download Kind.       
curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.14.0/kind-linux-amd64           
Change the binary's permissions to make it executable.           
chmod +x ./kind             
Move kind to an application directory, such as /bin:           
sudo mv ./kind /bin/kind                 
Using Kind to Create a Development Environment                  
To create a cluster with a different name, use the --name option.       
kind create cluster --name=[cluster-name]                
Confirm the cluster deployment with kubectl:               
kubectl get nodes                
note: if returns, ""kubectl" command not found" then install kubectl using snap        

 snap install kubectl                      

 snap install kubectl --classic                    
Check the Created Cluster with get                  
 kind get clusters                
To Delete the Cluster                    
 kind delete cluster                   
Pulling a docker image                    
 docker pull ravikantmaurya/mydocker:1.0            
using KinD to load the docker image to the cluster            
 kind load docker-image ravikantmaurya/mydocker:1.0             
