#ʹ��VMDepot������Azure�Ͽ��ٲ���CKAN#

��ָ��չʾ�����ͨ��VMDepot������ٽ���CKAN����

###ǰ������##
��������Ҫһ�����õ�΢���й�Azure���������й����˻�


### ��Azure�������̨�У�����CKAN���񵽱����ʻ� ##
��Azure����̨��[https://manage.windowsazure.cn](https://manage.windowsazure.cn)
ѡ��virutal machines -> images -> Browse VM Depot:
![](aaaa1.png)

��Ubuntu������ҵ�CKAN���������Ѿ�������VMdepot��һ��������
![](aaaa2.png)

������Ҫ���˾��񿽱������û��洢�˻�������ѡ�����еĴ洢�ʻ���Ҳ���½���
![](aaaa3.png)

�������̽����Ѽ����ӵ�ʱ�䣺
![](aaaa4.png)

������ɺ󣬱���CKAN�����״̬��Pending registration�����Registerע�᣺
![](aaaa6.png)

��дע�᾵�����ƣ�
![](aaaa7.png)

����״̬��ΪAvailable�����ˣ�CKAN�����Ѿ�׼����ϣ�
![](aaaa8.png)

### ʹ�ñ���CKAN���񴴽���� ##
��Azure�������̨�У�ѡ��Virtual Machines -> Create a Virtual Machine
![](aaaa9.png)

ѡ��From Gallery��
![](aaaa10.png)

��My Images����ҵ����Ǹո�ע���CKAN���񣬵����һ����
![](aaaa11.png)

��д������ƣ��û�������֤��ʽ��ע�������Ĭ���û���Ϊazureuser,�����һ����
![](aaaa12.png)

����Cloud Service���ڱ����У������ַΪmytestckan.chinacloudapp.cn,
ע����Ҫ����������tcp�˿ڣ��ֱ�Ϊ22��80��443�������һ����
![](aaaa13.png)

ȷ��VM Agent�Ѿ���װ�������һ����
![](aaaa14.png)

�ȴ�ֱ�������״̬��ΪRunning������CKAN��������ϣ�
![](aaaa15.png)

���������������ַ��http://mytestckan.chinacloudapp.cn,���Կ���CKAN�Ż��Ѿ����Է����ˣ�
![](aaaa16.png)

### ��װ������ã�������ɣ� ##
����CKAN������Ҫ��ÿһ���²���ľ�����Ҫ����ckan.site_url������������������
������ʾ����޸Ĵ˲�����
Windows�û���ͨ����װssh�ͻ��ˣ���PuTTY�����ӵ��½���CKAN�����Linux��Mac�û���ֱ��ͨ��ssh�������ӣ�
![](aaaa18.png)
���������ǲ����û���������֤��ʽ��¼mytestckan.chinacloudapp.cn

������������,����ǰ��YOUR-CKAN-DOMAIN-NAME�滻Ϊ��ʵ�ʵ���վ�������ڱ�����Ϊmytestckan.chinacloudapp.cn
sudo sed -i 's/ckanimage.chinacloudapp.cn/YOUR-CKAN-DOMAIN-NAME/' /etc/ckan/default/production.ini

��������Ƿ���Ч��
cat /etc/ckan/default/production.ini |grep ckan.site_url
![](aaaa19.png)
ע�⣬��Ҳ���Ϊ����CKAN�Ż���վ���벻ͬ���������뽫site_url�滻Ϊʵ���û�����ʹ�õ�������

����apache��nginx����
sudo service apache2 restart && sudo service nginx restart
![](aaaa20.png)

���ˣ�����CKAN�Ѿ�������ɣ���������ʹ���ˡ�


### �������ĵ�һ�����ݼ� ##
��admin��ݵ�¼CKAN�Ż���վ��Ĭ��������admin����¼���������������룺
![](aaaa16.png)

��������ݼ��� -> �������ݼ�
![](aaaa17.png)

�������ݼ����ƣ������һ����
![](aaaa21.png)

������ϴ�����
![](aaaa22.png)

ѡ�񱾵�Excel�ĵ���
![](aaaa23.png)

��ʽѡ��Ϊ��xls���������һ����
![](aaaa24.png)

����ѡ�񲹳����ݼ��Ķ�����Ϣ���������ɡ���
![](aaaa25.png)

���ˣ�CKAN���Զ�����Excel��񣬲�ͬʱ����OData��ʽ���ݷ���API��Ӧ�ó�����ʡ�
![](aaaa26.png)

ѡ�������->��Ԥ�������Բ鿴��������ݣ�
![](aaaa27.png)
![](aaaa28.png)

���ݵ�����ɺ󣬿���CKAN�Ż���ҳ�������������ݼ���
![](aaaa29.png)


### ��������CKAN ##
��Ҳ��ϣ���ı�˾���Ĭ�ϵ���������վ���⣬�������ֵȣ�
������admin��¼�󣬵����ҳ���Ͻǡ�ϵͳ����Ա���á���
ѡ�����á�ѡ���
![](aaaa30.png)
����������Զ���վ�������ֽ��ж��ơ�
