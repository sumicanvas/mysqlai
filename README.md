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

  
## 2.Mysql 관련 라이브러리 설치 전 GPG 키 설치 (mysql8.4에서는 반드시 필요함)
sudo rpm --import https://repo.mysql.com/RPM-GPG-KEY-mysql-202


## 3.Mysql 관련 라이브러리 설치
- MySQL 을 테스트할 것이기 때문에 이 부분이 필요
