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

![checking terraform code](src)




You can use the [editor on GitHub](https://github.com/arencibiafrancisco/devops/edit/main/README.md) to maintain and preview the content for your website in Markdown files.





Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/arencibiafrancisco/devops/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
