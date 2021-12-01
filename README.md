# 关于GCP修改root密码

关于GCP修改root密码使用第三方工具连接GCP 
--------------------------------------------

第一步：进入gcp实例控制台连接ssh

第二步：获得root权限输入`sudo -i`

![image](https://user-images.githubusercontent.com/94978556/143864988-8e191819-003a-4331-81f6-a2927b17b918.png)

第三步：修改你的root密码输入`passwd root`

![image](https://user-images.githubusercontent.com/94978556/143865260-0b71e558-081e-4ff0-8210-bb3b1eb06be9.png)

第四步：输入你想要设成的密码 需要输入两遍 输入好后按回车

![image](https://user-images.githubusercontent.com/94978556/143865671-05d927ed-2ec0-4804-a90f-38d1a5026144.png)

第五步：修改允许root方式登录和密码的授权输入`vim /etc/ssh/sshd_config`

如果有以下页面输入`E`  没有的 忽略

![image](https://user-images.githubusercontent.com/94978556/143866355-637de8b4-13a5-4eef-8249-1451471bda24.png)

进入修改页面

![image](https://user-images.githubusercontent.com/94978556/143866566-10ab5eb3-366f-4476-b044-726134e0e76b.png)

第六步：按`O`进入编辑模式修改一下两项改为`yes`如果前面有#请删除

![image](https://user-images.githubusercontent.com/94978556/144199406-81567acd-480a-423e-b658-c12c178af116.png)


![image](https://user-images.githubusercontent.com/94978556/143866877-ef65c67c-8a42-4a9c-8ec7-5233d8a8716a.png)

![image](https://user-images.githubusercontent.com/94978556/143866934-ca7a1a95-45f3-4ab6-8d95-0472d50eae1a.png)

第七步：修改好后按`ESC`退出编辑

第八步：输入`Shlft+！`然后输入`wq`保存

![image](https://user-images.githubusercontent.com/94978556/143867519-a1c47638-5244-4bc0-994d-85dea4c4aa75.png)

返回root页面

![image](https://user-images.githubusercontent.com/94978556/143867636-35dd3d14-c288-41b5-860f-143517c6869c.png)

第九步：输入`reboot`重启vps  输入后就会断开vps的连接

![image](https://user-images.githubusercontent.com/94978556/143867971-28976b7e-20ad-48fd-9dff-906f0fea5c04.png)

第十步：以上修改好后就可以用你的第三方ssh工具 来登录你的VPS啦

至此整个修改就完成了  小白分享大佬勿喷
