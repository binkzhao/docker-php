# docker-php

基于docker搭建的PHP开发环境

## 如何使用该环境
  ### 1. Clone project
      $ git clone https://github.com/binkzhao/docker-php
  
  ### 2. Rename .env-example to .env
      $ cd cd docker-php
      $ cp .env-example .env
  
  ### 3. Modify .env files
      such as `APPLICATION="your codes root directory"`
  
  ### 4. Run your containers
      $ docker-compose up -d nginx mysql redis
   