---
description: >-
  Here, you will find find all initial information about Horusec before getting
  deeper on the project.
---

# Overview

## **What is Horusec?**

It is an open source tool that orchestrates other security tools and identifies security flaws or vulnerabilities in projects and put all results in a database for analysis and generation of metrics.

The languages ​​and tools that we currently use are:

* **Python**
  * \*\*\*\*[**Bandit**](https://github.com/PyCQA/bandit)\*\*\*\*
  * \*\*\*\*[**Safety**](https://github.com/pyupio/safety)\*\*\*\*
  * \*\*\*\*[**Semgrep**](https://github.com/returntocorp/semgrep)\*\*\*\*
* **Ruby**
  * \*\*\*\*[**Brakeman**](https://github.com/presidentbeef/brakeman)\*\*\*\*
* **Javascript/Typescript**
  * \*\*\*\*[**Npm Audit**](https://docs.npmjs.com/cli/audit)\*\*\*\*
  * \*\*\*\*[**Yarn Audit**](https://yarnpkg.com/lang/en/docs/cli/audit/)\*\*\*\*
  * \*\*\*\*[**Semgrep**](https://github.com/returntocorp/semgrep)\*\*\*\*
  * \*\*\*\*[**HorusecNodeJS**](https://github.com/ZupIT/horusec/tree/master/horusec-nodejs)\*\*\*\*
  * \*\*\*\*[**EsLint**](https://github.com/eslint/eslint)\*\*\*\*
* **GoLang**
  * \*\*\*\*[**Gosec**](https://github.com/securego/gosec)\*\*\*\*
  * \*\*\*\*[**Semgrep**](https://github.com/returntocorp/semgrep)\*\*\*\*
* **C\#**
  * \*\*\*\*[**SecuriyCodeScan**](https://security-code-scan.github.io)\*\*\*\*
  * \*\*\*\*[**HorusecCSharp**](https://github.com/ZupIT/horusec/tree/master/horusec-csharp)\*\*\*\*
  * \*\*\*\*[**Flawfinder**](https://github.com/david-a-wheeler/flawfinder)\*\*\*\*
* **Java**
  * \*\*\*\*[**HorusecJava**](https://github.com/ZupIT/horusec/tree/master/horusec-java)\*\*\*\*
  * \*\*\*\*[**Semgrep**](https://github.com/returntocorp/semgrep)\*\*\*\*
* **Kotlin**
  * \*\*\*\*[**HorusecKotlin**](https://github.com/ZupIT/horusec/tree/master/horusec-kotlin)\*\*\*\*
* **Kubernetes**
  * \*\*\*\*[**HorusecKubernetes**](https://github.com/ZupIT/horusec/tree/master/horusec-kubernetes)\*\*\*\*
* **Terraform**
  * \*\*\*\*[**Tfsec**](https://github.com/liamg/tfsec)\*\*\*\*
* **Leaks**
  * \*\*\*\*[**HorusecLeaks**](https://github.com/ZupIT/horusec/tree/master/horusec-leaks)\*\*\*\*
* **Leaks\(optional search in git history\)**
  * \*\*\*\*[**GitLeaks**](https://github.com/zricethezav/gitleaks)\*\*\*\*
* **PHP**
  * \*\*\*\*[**Semgrep**](https://github.com/returntocorp/semgrep)\*\*\*\*
  * \*\*\*\*[**PHP Code Sniffer**](https://github.com/FloeDesignTechnologies/phpcs-security-audit)\*\*\*\*
* **C**
  * \*\*\*\*[**Semgrep**](https://github.com/returntocorp/semgrep)\*\*\*\*
  * \*\*\*\*[**Flawfinder**](https://github.com/david-a-wheeler/flawfinder)\*\*\*\*
* **HTML**
  * \*\*\*\*[**Semgrep**](https://github.com/returntocorp/semgrep)\*\*\*\*
* **JSON**
  * \*\*\*\*[**Semgrep**](https://github.com/returntocorp/semgrep)\*\*\*\*
* **Dart**
  * \*\*\*\*[**HorusecDart**](https://github.com/ZupIT/horusec/tree/master/horusec-dart)\*\*\*\*

## **How does Horusec work?**

There are two main tasks in Horusec: accessing the Dashboard and generating analysis.

### **1.  Dashboard access**

To access Horusec, it is necessary to create a login and password. After that, you can browse the Dashboard and perform actions such as:

* Set permissions for other users;
* Create repositories;
* Generate tokens to perform a project analysis.

### **2.** Analysis Process

To perform the analysis, you must use the CLI \(Command Line Interface\). If you want to check the result, you can also access a web interface, which guarantees a more analytical and detailed view.

If there is a security breach in the code, Horusec points the file, the severity level and tells you the best way to correct it. See the example below:

###  **CLI view** 

![](.gitbook/assets/image%20%285%29.png)

### **Interface Web view** 

![](https://lh3.googleusercontent.com/9ETkR59CP7wF9LJ8-cLunT-6jU93pmGq3nwXkNdg2T6g3FH9M6oZ7k5d4OCbR2e6Ph1v2EvBERgWHHUoCVKp_Df-0e7Zgp_uoKygRq7fcTC36VzmjcKJI77iR1n75ST7HeZE8ZuO)

\*\*\*\*

![](https://lh3.googleusercontent.com/FsOq3UQckswg7aCTszEP7lECRhk8q286ngGl2NV9Y_rL6zrTOYh61HON_8hhLnUlyeok1qPrlMQcJWjcfp1lIQ56TsuV_E0fbiFwrmSm4RZfdQnvQw8Ql_heTs2-xP6kV5XV29fD)

Examples of vulnerabilities

```text
Language: Leaks
Severity: HIGH
Line: 1
Column: 27
SecurityTool: HorusecLeaks
Confidence: MEDIUM
File: deployments/certs/server-cert.pem
Code: -----BEGIN CERTIFICATE-----
Details: Asymmetric Private Key
Found SSH and/or x.509 Cerficates among the files of your project, make sure you want this kind of information inside your Git repo, since it can be missused by someone with access to any kind of copy.  For more information checkout the CWE-312 (https://cwe.mitre.org/data/definitions/312.html) advisory.
Type: Vulnerability
ReferenceHash: 178bf5090b749f5eb7b081bccb0112eadac3d9ed3229d813e727ede62a3c6f15
```

## **Why use Horusec?**

* **Promotes the culture of secure development by applying the logic of “security by design”** 

It brings you security, ensuring that possible unknown vulnerabilities will be found by analyzing Horusec.

* **Improves your experience**

It ensures the safety of projects in the CI and CD process and, thus, reduces the costs of correcting a vulnerability.

## **Horusec analysis' types**

Horusec performs 3 types of performance analysis to identify if there are any security flaws:

1. **SAST \(Static Application Security Testing\)**  


   The SAST does static code vulnerability analysis. They can be done in source code, byte code or binary.  
   ****

2. **Leaks**   
   The "Leaks checks the source code for possible leaks of credentials, private keys or hard coded passwords. 

3.  **Dependency audit** You analyze the project's dependencies to check for vulnerabilities in third-party libraries.   in third-party libraries.

