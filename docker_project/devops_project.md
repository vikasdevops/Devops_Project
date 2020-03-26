# Devops Project CI/CD Through Docker
## Layout Project:

<img src="imagesdocker/layout.png" width="410" height="402">

***

- Launch The EC2 instance

<img src="imagesdocker/Selection_002.png" width ="755" height="190">

***


- Install Jenkins in EC2 webjenins

<img src="imagesdocker/Selection_004.png" width ="500" height="100">

***

- Install docker in EC2 Docker

<img src="imagesdocker/Selection_003.png" width ="600" height="100">

***

- create the dir.
 - Assign permission

 ```
 $ chown -R dockeradimin:dockeradimin /opt/docker
```


  <img src="imagesdocker/Selection_020.png" width ="400" height="20">

***

- create dockerfile

<img src="imagesdocker/Selection_021.png" width ="600" height="80">

***

- ADD Jenkins plugins ssh


<img src="imagesdocker/Selection_012.png" width ="800" height="300">

***

<img src="imagesdocker/Selection_013.png" width ="800" height="90">

***

- Add new jobs

<img src="imagesdocker/Selection_006.png" width ="500" height="100">

***

- Add the credentials SSH

<img src="imagesdocker/Selection_007.png" width ="700" height="400">

***

<img src="imagesdocker/Selection_008.png" width ="700" height="400">

***

- Build jobs

 <img src="imagesdocker/Selection_010.png" width ="700" height="400">

 ***

<img src="imagesdocker/Selection_011.png" width ="600" height="300">

***

<img src="imagesdocker/Selection_017.png" width ="790" height="200">

***
- check the browser

<img src="imagesdocker/web.PNG" width ="400" height="200">

***


<img src="imagesdocker/webnew.png" width ="400" height="210">

***
