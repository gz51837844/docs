#ʹ��VMDepot������Azure�Ͽ��ٲ���CKAN#

��ָ��չʾ�����ͨ��VMDepot������ٽ���CKAN����

###ǰ������##
��������Ҫһ�����õ�΢���й�Azure���������й����˻�


### ��Azure�������̨�У�����CKAN���񵽱����ʻ� ##
��Azure����̨��[https://manage.windowsazure.cn](https://manage.windowsazure.cn)
ѡ��virutal machines -> images -> Browse VM Depot:
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/1.PNG)

��Ubuntu������ҵ�CKAN���������Ѿ�������VMdepot��һ��������
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/2.PNG)

������Ҫ���˾��񿽱������û��洢�˻�������ѡ�����еĴ洢�ʻ���Ҳ���½���
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/3.PNG)

�������̽����Ѽ����ӵ�ʱ�䣺
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/4.PNG)

������ɺ󣬱���CKAN�����״̬��Pending registration�����Registerע�᣺
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/6.PNG)

��дע�᾵�����ƣ�
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/7.PNG)

����״̬��ΪAvailable�����ˣ�CKAN�����Ѿ�׼����ϣ�
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/8.PNG)

### ʹ�ñ���CKAN���񴴽���� ##
��Azure�������̨�У�ѡ��Virtual Machines -> Create a Virtual Machine
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/9.PNG)

ѡ��From Gallery��
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/10.PNG)

��My Images����ҵ����Ǹո�ע���CKAN���񣬵����һ����
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/11.PNG)

��д������ƣ��û�������֤��ʽ��ע�������Ĭ���û���Ϊazureuser,�����һ����
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/12.PNG)

����Cloud Service���ڱ����У������ַΪmytestckan.chinacloudapp.cn��
ע����Ҫ����������tcp�˿ڣ��ֱ�Ϊ22��80��443�������һ����
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/13.PNG)

ȷ��VM Agent�Ѿ���װ�������һ����
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/14.PNG)

�ȴ�ֱ�������״̬��ΪRunning������CKAN��������ϣ�
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/15.PNG)

���������������ַ��http://mytestckan.chinacloudapp.cn�����Կ���CKAN�Ż��Ѿ����Է����ˣ�
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/16.PNG)

### ��װ������ã�������ɣ� ##
����CKAN������Ҫ��ÿһ���²���ľ�����Ҫ����ckan.site_url������������������
������ʾ����޸Ĵ˲�����
Windows�û���ͨ����װssh�ͻ��ˣ���PuTTY�����ӵ��½���CKAN�����Linux��Mac�û���ֱ��ͨ��ssh�������ӣ�
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/18.PNG)
���������ǲ����û���������֤��ʽ��¼mytestckan.chinacloudapp.cn

������������,����ǰ��*YOUR-CKAN-DOMAIN-NAME*�滻Ϊ��ʵ�ʵ���վ�������ڱ�����Ϊmytestckan.chinacloudapp.cn
sudo sed -i 's/ckanimage.chinacloudapp.cn/*YOUR-CKAN-DOMAIN-NAME*/' /etc/ckan/default/production.ini

��������Ƿ���Ч��
cat /etc/ckan/default/production.ini |grep ckan.site_url
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/19.PNG)
ע�⣬��Ҳ���Ϊ����CKAN�Ż���վ���벻ͬ���������뽫site_url�滻Ϊʵ���û�����ʹ�õ�������

����apache��nginx����
sudo service apache2 restart && sudo service nginx restart
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/20.PNG)

���ˣ�����CKAN�Ѿ�������ɣ���������ʹ���ˡ�


### �������ĵ�һ�����ݼ� ##
��admin��ݵ�¼CKAN�Ż���վ��Ĭ��������admin����¼���������������룺
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/16.PNG)

��������ݼ��� -> �������ݼ�
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/17.PNG)

�������ݼ����ƣ������һ����
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/21.PNG)

������ϴ�����
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/22.PNG)

ѡ�񱾵�Excel�ĵ���
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/23.PNG)

��ʽѡ��Ϊ��xls���������һ����
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/24.PNG)

����ѡ�񲹳����ݼ��Ķ�����Ϣ���������ɡ���
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/25.PNG)

���ˣ�CKAN���Զ�����Excel��񣬲�ͬʱ����OData��ʽ���ݷ���API��Ӧ�ó�����ʡ�
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/26.PNG)

ѡ�������->��Ԥ�������Բ鿴��������ݣ�
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/27.PNG)
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/28.PNG)

���ݵ�����ɺ󣬿���CKAN�Ż���ҳ�������������ݼ���
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/29.PNG)


### ��������CKAN ##
��Ҳ��ϣ���ı�˾���Ĭ�ϵ���������վ���⣬�������ֵȣ�
������admin��¼�󣬵����ҳ���Ͻǡ�ϵͳ����Ա���á���
ѡ�����á�ѡ���https://raw.githubusercontent.com/msopentechcn/docs/master/images/��
![](https://raw.githubusercontent.com/msopentechcn/docs/master/images/30.PNG)
����������Զ���վ�������ֽ��ж��ơ�
