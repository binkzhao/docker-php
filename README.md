# docker-php

基于laradock修改的PHP开发环境

## 如何使用该环境
  ### 1. Clone project
      git clone https://github.com/binkzhao/docker-php
  
  ### 2. Rename env-example to .env
      cp env-example .env
  
  ### 4. Modify .env files
      such as `APPLICATION="codes root directory"`
  
  ### 5. Run your containers
      docker-compose up -d nginx mysql redis 
   
## PS
    由于网络的原因，部分PHP扩展可能安装不了，可以先不安装，等容器创建好后，在容器里面直接安装。
    或者说修改扩展的安装命令，找可以下载的源。 环境比较简单，有其他的需求可以在这个基础是上面调整扩展。

