### �������� ������ Active Directory
1. ������������ � ������� � ������� ������� RDP
2. ���������� �� ������� ���� **Active Directory Domain Services**
3. ��������� ������ ����������� ������� �� ������ ����������� ������
   * ������� ����� ��� `corp.example.com`
   * ��������� ����� ������ ��� �������������� ������
4. ������������� ������ � ����� ������������ �� ���
### ����������� ����������� ���������� � ������ AD
1. ������� ������� DNS, ������� �������� ������� DNS, ������� ������� forwarders � �������� DNS-������� ��� ��������� �������� (���� ����� �� �������, �� ���������� ���������� ����� �������������� DNS-������� � �.4 �� ������ �������� ������ � ��������):
   * 1.1.1.1
   * 8.8.8.8
   * 8.8.4.4
   * 9.9.9.9
2. ���������� ��������� IP-����� ������� (`ipconfig /all`)
3. ������������ � ����������� ���������� � ������� ������� RDP
4. �������� DNS-������ � ���������� �������� ����������� �� IP-����� �������
5. ������� ��������� �������, ����� ���� ��������� ����� ���������� � �������� ������� ������ �� ����� corp.example.com
6. ������������� ���������� ���������
7. �� ������� ������� ������� **Active Directory Users and Computers** � ��������� ��� ���������� ��������� ����� � �����
### ���� �� ���������� ���������� � ������� �������� ������� ������
1. �� ���������� ���������� ������� ������� **Computer Management**, ������� � ������ **Local Users and Groups, Groups**
2. � ������ **Remote Desktop Users** �������� ������ **Domain Users** (��� ����� ����� ����� ���� ��������� �.4)
3. �� ������� � ������� ������� Active Directory Users and Computers:
   * ������� ����� ������ ������������ (����������) `RoleManager` � `RoleDeveloper`
   * ������� ����� ������ ������������ (��������� � ������) `ShareRO` � `ShareFC`
   * �������� ������ `RoleManager` � ������ `ShareRO`
   * �������� ������ `RoleDeveloper` � ������ `ShareFC`
   * ������� ���� ����� ������������� � �������� ������ � ������ `RoleManager`, � ������� � ������ `RoleDeveloper`
4. ����������� �� ����������� ���������� � ����� �� ���� � ������� �������� ������� ������.
5. **������� ��������� ������ ��������� ������� hostname � whoami. ������� �������� ��� ����� ���� ����� ��������� RDP-������� � ��������� ������ � ������������ ������.**
### ��������� ��������� �������
1. �� ������� �������� ������� Group Policy Management
   * �������� ��� `corp.example.com`
   * �������� ����� `corp.example.com`
2. �������� � ������ corp.example.com �������� Disable browser
   * � ����������� ���� �������� �������� Edit
   * �������� ��������:![�������������� �����](/images/adgroup2.png)
   * �������� �������� `msedge.exe`.
   * �������� ��������.
   * �������� ��������� �������� � � ������� **Security Filtering** �������� ������ ������������� RoleManager.
   * �������� ����� `corp.example.com` � �� ������� **Linked Group Policy Object (GPO)** ����������� ��������� ��������� �������� �� ������� �������.
   * **��������� ������ ��������� ��������, �������� �������� ����������� ������**
3. �������� �� ������� ������� **Share** � ��������� �� ��� ������� ������:
   * �� ������� **Sharing** ������ ������ **Advanced Sharing**, �������� ������� **Share this folder**, ������ ������ **Permissions** � ��������� **Full Control** ��� ���� (Everyone)
   * �� ������� **Security** ������ ������ **Advanced**, ��������� ������������ (������������� ������������ ����� � ����� �����), ������� ����� ������ **Domain Users**, �������� ����� �� ������ ��� ������ **ShareRO**, �������� ����� �� ������ ������ ��� ������ **ShareFC**
   * **�������� �������� �������**
4. �������� � ������ `corp.example.com` �������� **Startup script**
   * �������� ������� � � ����� ����� �������� �������: `net use s: \\<��� �������>\share`
   * ��������� ��� ������ `startup.bat` (���������, � ��� ��� ���������� ����� - bat)
   * � ����������� ���� �������� �������� **Edit**
   * �������� ��������:![�������������� �����](/images/adgroup4.png)
   * ��������� � �������� ������� `startup.bat `
   * �������� ����� `corp.example.com` � �� ������� **Linked Group Policy Object (GPO)** ����������� ��������� ��������� �������� ���� ��� **Default Domain Policy**.
   * ��������� ������ ��������� ��������
