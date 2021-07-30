## Welcome to DevSecOps notes.

# Auditing your code preventing misconfigurations

[Checkov](https://github.com/bridgecrewio/checkov) is an amazing tool than can prevent cloud misconfigurations during build-time for Terraform, Cloudformation, Kubernetes.


## Terraform

In this quick example we are going to audit a terraform code. In this case I'm using Ubuntu 20.04 but in the official documentation 
you can check all available options. So lets install checkov in our system, this could be done using a pipeline like Gitlab and run this checkov test before merging terraform code, this would like the best use  we could do of this tool.


```markdown
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt install python3.7
sudo apt install python3-pip
sudo python3.7 -m pip install -U checkov
```
Next step would just enter inside de directory that has the code we want to audit and run 
checkov -d . 

This would the result:

![checking terraform code](https://github.com/arencibiafrancisco/devops/blob/main/terraform%20audit.png)




You can use the [editor on GitHub](https://github.com/arencibiafrancisco/devops/edit/main/README.md) to maintain and preview the content for your website in Markdown files.





