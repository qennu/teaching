# ����� �����
### �������� ������ Active Directory
1. ������������ � ������� � ������� ������� RDP
2. ���������� �� ������� ���� **Active Directory Domain Services**
3. ��������� ������ ����������� ������� �� ������ ����������� ������.
   * ������� ����� ��� `corp.example.com`
   * ��������� ����� ������ �� ������ �������������� ������.
4. ������������� ������ � ����� ������������ �� ���.
### ����������� ����������� ���������� � ������ AD
5. ��������� � ��������� DNS-������� ��������� (forwarding) �������� � ��������:
   * 8.8.8.8
   * 1.1.1.1
   * 9.9.9.9
   * 8.8.4.4
6. **������� �������� ������� Forwarding �� ������� DNS-�������**
7. ���������� ��������� IP-����� ������� (`ipconfig /all`) � �������� ���.
8. ��������� �� ���������� ���������� � �������� DNS-������� - IP-����� �������
9. ����� � ��������� ������� �� ���������� ����������. ����� ���� ��������� ����� ���������� � �������� ������� ������ �� ����� `corp.example.com`
   * ������ ������ �������������� ������.
   * ������������� ���������� ���������.
   * �� ������� ������� ������� **Active Directory Users and Computers** � ��������� ��� ���������� ��������� ����� � �����.
10. **������� �������� ������� Active Directory Users and Computers � ����������� ���������� �����������**
### ���� �� ���������� ���������� � ������� �������� ������� ������
11. �� ������� � ������� ������� Active Directory Users and Computers ������� ���� �����  �������������
12. �� ���������� ���������� ������� ������� Computer Management, ������� � ������ Local Users and Groups, Groups � �������� ��������� �������� ������������� � ������ Administrators.
13. � ������ **Remote Desktop Users** �������� ������ **Domain Users**, ������ ������ �������������� ������.
14. ����������� �� ����������� ���������� � ����� �� ���� � ������� �������� ������� ������.
15. **�� ���������� ���������� �������� ��������� ������ � ��������� ������� hostname � whoami. �������� �������� ��� ����� ���� ����� ���������� ������� � ��������� ���� ������� RDP.**
### ��������� ������� � ����� �����
https://medium.com/tech-jobs-academy/igdla-and-you-a-fledgling-s-guide-to-nesting-e09b748e3a60

��������� � ������ ������ ������������ � ������������ ��� ���������� ������������ ������� � �������� (������, ������ � ������ ����� ��������) ������ ���� ������, ��� ��� ���� �������. ��������� ������ ������ ������������ � ������ ������� (������ � ��������� ������ ����� ������� ������������ ������� ������). ��������� ������ ����� ������� � ������ ��������� ������, �� �� ����� ������� � ����������.

���������� ������ ������������ � ����� �������������� ��� �������������� ������� � �������� ������� ������. � ��� ������ ����� �������� ������ ������� ������ �� ���� �� ������, � ������� ������� ������. ���������� ������ ����� ������� � ������ ���������� � ��������� ������.

������������� ������ ������������ � ������������� ������������ � ����� �� ��������� �������. � ������� ��� ����� ���������� ���� � ��������� ���������, ������� ������������ �� ���������� �������. � ��� ������, ���� � ����� ���� ������� ����� ��������, ��������� ���������� WAN ��������, ���������� ������������ ������������� ������ ������ ��� ����� ������������ �����. �.�. ��������� ������������� ������ �������� ������������� ���������� ����������� �������� �� ���� �����������.

16. �� ������� � ������� ������� **Active Directory Users and Computers** ������� ��� ������ ������������ (����������): `RoleDeveloper`, `RoleManager`
17. �������� ������� ������������ AD � ������ **Developer**.
18. �������� ������� ������������ AD � ������ **Manager**.
19. �� ������� � ������� ������� **Active Directory Users and Computers** ������� ��� ������ ������������ (��������� � ������): `ShareFullControl`, `ShareReadOnly`.
20. �� ������� �� ����� C: ������� ����� ������� `Share`.
21. ������� ������ ������� ��� �������� **Share**
    * �� ������� **Sharing** ������� � **Advanced Sharing, Permissions** � ��������� ������ ������ ��� ���� (Everyone)
    * �� ������� **Security** ������� � **Advanced** � ��������� ������������ ���� ������� (Disable inheritance) � ������������ �������������� ���� � ����� ����� �� ������ (Convert inherited permissions into explicit permissions on this object).
    * ������� ������ ������������������� ������������� (Authenticated users) � ������������� ������ (Users)
    * �������� ����� �� ������ ��� ������ **ShareReadOnly**.
    * �������� ����� �� ������ ������ ��� ������ **ShareFullControl**.
22. � ������ **ShareFullControl** ��������� ������ **Developer**, � ������ **ShareReadOnly** ��������� ������ **Manager**.
23. ��������� ������ ���� ������� � ����������� ����������.
24. **������� ���������:**
    * **������� Advanced �� ������� Security � ��������� ����� ����� Share**
    * **������ ����� ShareFullControl � ShareReadOnly**
    * **������ ����� RoleDeveloper � RoleManager**