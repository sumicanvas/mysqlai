# mysqlai
MySQL AI Installation guide

## 0. 설치 환경
오라클 클라우드(OCI) VM 환경  

OS : OL 8 - 현재는 리눅스 8 버전이 지원 버전입니다.  
OCI VM은 이미 생성했다고 가정합니다.  
(compartment를 mysql ai를 위한 것으로 새로 만들어주세요. 그리고 시큐리티 rule 에 8000, 8080, 8443 을 추가해주면 됩니다.

  
## Object Store에서 rpm tar 및 cert tar 파일을 다운로드
```
mkdir mysqlairpms  
  
cd mysqlairpms  
  
curl --output mysqlairpms.tar "https://objectstorage.us-ashburn-1.oraclecloud.com/p/v4EB7Ep3mbrhAaBjgrN_qVYSKtosXzoO-dSDdtACP2Awbm1oj0CPAvP1FIP6Gjhs/n/idv7j37dc1rt/b/mysqlairpms/o/airpm.tarmysql-ai-9.4.1-1.2.el8.x86_64.rpm-bundlesept.tar"  
  
tar xvf mysqlairpms.tar
  
cd ~ 
  
curl  --output certs.tar "https://objectstorage.us-ashburn-1.oraclecloud.com/p/V9jHtM8o9eAvx-D2-cyN6qXh5rvGaIFgZbFUxgO5mrA49NMEAy7sF0RMIPDkDjpn/n/idv7j37dc1rt/b/mysqlairpms/o/certsforaiworkingcerts.tar"  
  
tar xvf certs.tar
```

## MySQL AI 설치
```
cd ~/mysqlairpms/

sudo dnf localinstall mysql-ai-setup-9.4.1-1.2.el8.x86_64.rpm

cd ~/mysqlairpms/

sudo mysql-ai-setup
```

  
<img width="730" height="514" alt="image" src="https://github.com/user-attachments/assets/71354682-1e89-4057-a125-b2c1201fc67b" />  
  
  
<img width="730" height="514" alt="image" src="https://github.com/user-attachments/assets/de16d2c2-f945-4280-9393-e96f62dc6bed" />  

    
<img width="730" height="514" alt="image" src="https://github.com/user-attachments/assets/7bf33dfb-602d-44af-bec0-bc2b5ad128fc" />  


  
<img width="730" height="514" alt="image" src="https://github.com/user-attachments/assets/a301800e-a5c7-401d-9ed9-1bfcc448c3fa" />  
  
  
### Hit the space bar – or this will not get installed – make sure port is showing  
<img width="730" height="514" alt="image" src="https://github.com/user-attachments/assets/f4358636-5257-4675-b256-9c4bb5677943" />  


  
### You can take the default here – or type in your own – fine both ways  
<img width="730" height="514" alt="image" src="https://github.com/user-attachments/assets/3b18688e-e3fb-41b1-8b36-24787ca7de6f" />  

  

### You will use this directory in the next tutorial  
The default here is - /var/lib/mysql-files  

  
<img width="730" height="514" alt="image" src="https://github.com/user-attachments/assets/d9e8023b-0aa7-432c-85e6-3a4b90469328" />  


  
### Take default self signed  

  <img width="730" height="514" alt="image" src="https://github.com/user-attachments/assets/75a75112-0352-4215-879a-322200458436" />


  
  <img width="730" height="514" alt="image" src="https://github.com/user-attachments/assets/3880e27d-c5d1-4549-a356-e3896c981eac" />


    
<img width="727" height="512" alt="image" src="https://github.com/user-attachments/assets/d72c31c3-8e80-4d4c-a14b-6e4564cc2331" />  

  
 
### This could take around 15-20 minutes  
<img width="730" height="514" alt="image" src="https://github.com/user-attachments/assets/01d47b4f-4f92-49f4-a638-3ee441568fb0" />

  

### 설치완료
  
<img width="733" height="510" alt="image" src="https://github.com/user-attachments/assets/dfd8f3c0-982b-4b3d-a6a9-e9b68956f294" />  
  
```
==============================================================================
Installation finished.
==============================================================================

To access MySQL Studio, navigate to the following
URL in a web browser:

    https://mysqlaiVM:8080/

To access a SQL shell for this MySQL AI instance, navigate to the following
URL in a web browser:

    https://mysqlaiVM:8000/

The MySQL REST Service endpoint is:

    https://mysqlaiVM:8443/
```


  

###   
  
<img width="992" height="286" alt="image" src="https://github.com/user-attachments/assets/28cc5fba-c75f-4cc2-8a01-8e459de3bcdb" />


    
### The AI service is on 40008 – again name will change going forward   
  
<img width="901" height="39" alt="image" src="https://github.com/user-attachments/assets/7efd226f-ecdc-47b7-a028-d8c12e8b4d78" />

### Once you finished the installation, here is mysql studio   
<img width="1324" height="585" alt="image" src="https://github.com/user-attachments/assets/f8ec8bca-c1fc-4a5a-aa19-9afa5c57366b" />  

### mysql shell gui  

#### Login with ID/PWD
<img width="1914" height="1262" alt="image" src="https://github.com/user-attachments/assets/76d53b18-6a9a-4691-bcf8-308f37588473" />  

#### 
<img width="1197" height="510" alt="image" src="https://github.com/user-attachments/assets/2ae5804e-cd97-4b58-b8d3-68c2f9a6dbd6" />

