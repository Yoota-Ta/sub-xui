- ## 搭建梯子节点以及节点 订阅

  ---

  部署基于[stilleshan/dockerfiles/tree/main/sub](https://github.com/stilleshan/dockerfiles/tree/main/sub)修改的，增加了`x-ui`，部署基于宝塔面板

  ### 操作步骤

  1. git clone 

     ```
     git clone https://github.com/Yoota-Ta/sub-xui.git
     ```

     

  2. 安装docker 需要docker-compose

     在宝塔插件中安装简单一些
     
     ![](./img/07.png)

  3. 下载拷贝目录至服务器,然后在服务器该根目录下执行

     ```
     docker-compose up -d
     ```
  
  ![](./img/06.png)

  

  ### 命令有问题，可以重启docker

  ```
  sudo systemctl restart docker
  ```
  
  ### 防火墙开放的端口

  ```
  18080
  8002
  ```
  
  
  
  ### 配置反向代理
  
  ![](./img/02.png)
  
  
  
  
  
  ![](./img/03.png)
  
  
  
  
  
  ### 订阅转换
  
  拷贝上一步生成的节点去生成订阅转换 
  
  ![](./img/05.png)
  
  
  
  
  
  ### 注意
  
  如果测试订阅，不通的话可能是端口问题，检查防火墙，以及宝塔端口是否开放
  
  ![](./img/08.png)
  
  
  
  ### 为了降低被封，做一个伪站，域名根目录放一个站点
  
  1. 修改 xui 跟路径
  
     ![](./img/09.png)
  
     
  
  2. 、修改节点配置
  
     ![](./img/11.png)
  
  3. 修改反正代理
  
     ![](./img/12.png)
  
     ![](./img/13.png)
  
  ### 推荐
  
  - [需要服务器的，欢迎关注](https://www.xwhoo.info)
  
  - [域名注册](https://www.godaddy.com/)
  
  
  
  我只是对资源进行了整合，非常感谢相关源码作者的付出
  
  ## 参考
  
  - [stilleshan/dockerfiles/tree/main/sub](https://github.com/stilleshan/dockerfiles/tree/main/sub)
  - [stilleshan/subweb](https://github.com/stilleshan/subweb)
  - [stilleshan/subconverter](https://github.com/stilleshan/dockerfiles/tree/main/sub)
  - [vaxilu](https://github.com/vaxilu)
