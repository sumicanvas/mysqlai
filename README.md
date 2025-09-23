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

tar xvf mysqlairpms.tarcd ~ 

curl  --output certs.tar "https://objectstorage.us-ashburn-1.oraclecloud.com/p/V9jHtM8o9eAvx-D2-cyN6qXh5rvGaIFgZbFUxgO5mrA49NMEAy7sF0RMIPDkDjpn/n/idv7j37dc1rt/b/mysqlairpms/o/certsforaiworkingcerts.tar"

tar xvf certs.tar
```

## MySQL AI 설치
```
cd ~/mysqlairpms/

sudo dnf localinstall mysql-ai-setup-9.4.1-1.2.el8.x86_64.rpm

cd ~/mysqlairpms/

sudo mysql-ai-setup<img width="229" height="59" alt="image" src="https://github.com/user-attachments/assets/8a2af823-afc5-4003-90e4-915e61fbc20c" />
```
<img width="730" height="514" alt="image" src="https://github.com/user-attachments/assets/71354682-1e89-4057-a125-b2c1201fc67b" />  

  
<img width="1444" height="1030" alt="image" src="https://github.com/user-attachments/assets/de16d2c2-f945-4280-9393-e96f62dc6bed" />  

  
<img width="1458" height="1018" alt="image" src="https://github.com/user-attachments/assets/7bf33dfb-602d-44af-bec0-bc2b5ad128fc" />  

<img width="1462" height="1032" alt="image" src="https://github.com/user-attachments/assets/a301800e-a5c7-401d-9ed9-1bfcc448c3fa" />  

  
### Hit the space bar – or this will not get installed – make sure port is showing  
<img width="1456" height="1024" alt="image" src="https://github.com/user-attachments/assets/f4358636-5257-4675-b256-9c4bb5677943" />  

  - You can take the default here – or type in your own – fine both ways  
<img width="1464" height="1028" alt="image" src="https://github.com/user-attachments/assets/3b18688e-e3fb-41b1-8b36-24787ca7de6f" />  


### You will use this directory in the next tutorial  
The default here is - /var/lib/mysql-files  
<img width="1458" height="1018" alt="image" src="https://github.com/user-attachments/assets/d9e8023b-0aa7-432c-85e6-3a4b90469328" />  

### Take default self signed
  <img width="1468" height="1032" alt="image" src="https://github.com/user-attachments/assets/75a75112-0352-4215-879a-322200458436" />

  <img width="730" height="507" alt="image" src="https://github.com/user-attachments/assets/3880e27d-c5d1-4549-a356-e3896c981eac" />

  <img width="727" height="512" alt="image" src="https://github.com/user-attachments/assets/d72c31c3-8e80-4d4c-a14b-6e4564cc2331" />

  
### This could take around 15-20 minutes  
<img width="1478" height="1030" alt="image" src="https://github.com/user-attachments/assets/01d47b4f-4f92-49f4-a638-3ee441568fb0" />


### 설치완료





## 

