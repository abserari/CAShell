# CAShell
shell to create root CA cert file from Rancher

## Exec
note to give permission by this command in shell file  directory
` chmod +x create.sh ` 

## 脚本说明
复制以上代码另存为create.sh或者其他您喜欢的文件名。

脚本参数

        --ssl-domain: 生成ssl证书需要的主域名，如不指定则默认为www.rancher.local，如果是ip访问服务，则可忽略；
        --ssl-trusted-ip: 一般ssl证书只信任域名的访问请求，有时候需要使用ip去访问server，那么需要给ssl证书添加扩展IP，多个IP用逗号隔开；
        --ssl-trusted-domain: 如果想多个域名访问，则添加扩展域名（TRUSTED_DOMAIN）,多个TRUSTED_DOMAIN用逗号隔开；
        --ssl-size: ssl加密位数，默认2048；
        --ssl-date: ssl有效期，默认10年；
        --ca-date: ca有效期，默认10年；
        --ssl-cn: 国家代码(2个字母的代号),默认CN；

 使用示例:

```bash
./create_self-signed-cert.sh --ssl-domain=www.test.com --ssl-trusted-domain=www.test2.com --ssl-trusted-ip=1.1.1.1,2.2.2.2,3.3.3.3 --ssl-size=2048 --ssl-date=3650
 ```