## Understanding Vagrant and its configuration.

Today, I dive deeper on 'Vagrant' and learned about 'Vagrantfile'. I watched this [Vagrant Crash Course](https://youtu.be/vBreXjkizgo) youtube video alongside my course. This video explains every component of the 'Vagrantfile' like (network, memory and OS).

 let me tell you about how to reach to your 'Vagrantfile'.

In your shell {GitBash, Powershell} go to your directory/folder and type ``` code . ``` you will be redirected to your VS code editor.

![image](https://user-images.githubusercontent.com/89379595/157268723-9c303aeb-57f8-4584-9105-5185f6070068.png)

Vagrant uses API versions for its configuration file, this is how it can stay backwards compatible. So in every Vagrantfile we need to specify which version to use. The current one is version 2 which works with Vagrant 1.1 and up. This is the header section of a Vagrantfile as the progamming language used is ```Ruby```.

The below section **Specify the box**.
> config.vm.box = "centos/7"

That base box is hosted on Vagrant Cloud, so we only need to specify the name and Vagrant will automatically get it from there. We don't have to explicitly downlaod it.

Then comes the next setting: 

![image](https://user-images.githubusercontent.com/89379595/157270474-fcbaaeb4-5437-4809-8d4f-ec4d2a0cf6e0.png)

If true, Vagrant will check for updates to the configured box on every vagrant up. If an update is found, Vagrant will tell the user. By default it is set to false to prevent any kind of error.

![image](https://user-images.githubusercontent.com/89379595/157270406-5fff7dcd-2b12-4f91-91d9-b3e41c451827.png)

 Create a forwarded port mapping which allows access to a specific port within the machine from a port on the host machine. In the example below, accessing "localhost:8080" will access port 80 on the guest machine.
  
 NOTE: This will enable public access to the opened port.

![image](https://user-images.githubusercontent.com/89379595/157270653-f93c2bab-cad6-425f-aa3e-8aa852336cff.png)

cIt reate a forwarded port mapping which allows access to a specific port within the machine from a port on the host machine and only allow access via 127.0.0.1 to disable public access.

![image](https://user-images.githubusercontent.com/89379595/157270983-6dcddb1f-e396-40ae-91c2-1d625765ed41.png)

Create a public network, which generally matched to bridged network. Bridged networks make the machine appear as another physical device on your network.
  
  ![image](https://user-images.githubusercontent.com/89379595/157271083-1168a1f1-eac1-4992-b2e5-ec1b1e942c33.png)

Share an additional folder to the guest VM. The first argument is# the path on the host to the actual folder. The second argument is the path on the guest to mount the folder

![image](https://user-images.githubusercontent.com/89379595/157271208-49f4ab6c-3975-42d7-875a-fd4ed6b6c17a.png)

 Provider-specific configuration so you can fine-tune various backing providers for Vagrant. These expose provider-specific options.
 
 ![image](https://user-images.githubusercontent.com/89379595/157271384-05edcc40-5775-4927-9f61-ffba3c6c69f3.png)

Enable provisioning with a shell script. Additional provisioners such as Ansible, Chef, Docker, Puppet and Salt are also available.

Alongside this, I learn some basic Linux comands. It was a prodcutive day overall.
