---
description: >-
  In this section, you will find guidelines for installing Horusec according to
  your operating system.
---

# Installing Horusec

### **MAC or Linux**

Installation: 

```text
curl -fsSL https://horusec.io/bin/install.sh | bash
```

### **Windows**

Installation: 

```bash
curl "https://horusec.io/bin/latest/win_x64/horusec.exe" -o "./horusec.exe" && ./horusec.exe version
```



{% hint style="info" %}
If you need to download for a specific version / operating system. In this case, the supported operating systems are:



* linux\_x86
* linux\_x64
* mac\_x64
* win\_x86
* win\_x64



👉[**Latest version available**](https://horusec.io/bin/version-cli-latest.txt)

\*\*\*\*👉\*\*\*\*[**All versions available** ](https://horusec.io/bin/all-version-cli.txt)
{% endhint %}



### **Manual installation**

Download manually choosing your operating system and the version you want. 

**MAC or Linux:**

```text
https://horusec.io/bin/$versão/$sistema_operacional/horusec
```

**Windows:**

```text
https://horusec.io/bin/$versão/$sistema_operacional/horusec.exe

```

**Example:** https://horusec-cli.s3.amazonaws.com/v1-1-0/win\_x64/horusec.exe

## Using Horusec with image docker

Another way to carry out your analysis is through a docker image that you can run locally or use in your pipeline. See some examples below:

#### Starting image with run command:

Quando você inicializa a imagem com o comando de `run` seu ponto de entrada já será por padrão:`horusec start` sendo assim basta você adicionar suas flags para executar o comando

When you initialize the image with the `run` command, your entry point will already be by default: `horusec start`, so you just need to add your flags to execute the command.

```text
docker run --privileged -v /path/of/my/project/local:/project -it horuszup/horusec-cli:latest -p /project
```

#### Starting image in your pipeline:

This is an example using the pipeline of [**aws code build**](adding-horusec-in-the-pipeline.md).

{% hint style="danger" %}
ATTENTION! When using Horusec in a docker image, some features will not work as:

* Export files;

It is recommended to use the Horusec executable in your environment!
{% endhint %}

## **Next Steps** 

On this section, you accomplished the Horusec installation. To keep reading about the product: 

\*\*\*\*👉 ****Go to ****[**using Horusec** ](using-horusec.md)section if you want to know how to use the tool. 

👉 Go to [**adding Horusec in the pipeline**](adding-horusec-in-the-pipeline.md) ****if you want to go directly to the tool's application on your development pipeline. 

