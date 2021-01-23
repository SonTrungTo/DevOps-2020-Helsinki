## This documents the file size pre-optimization and post-optimization.

## [Frontend](https://github.com/SonTrungTo/DevOps-2020-Helsinki/blob/master/docker_part1/1_10/Dockerfile)
- Pre-optimization: `652 MB`, with
    - 069646e8f771   25 seconds ago       /bin/sh -c #(nop)  CMD ["npm" "start"]          0B        
    - 7bcb8af0a6ed   25 seconds ago       /bin/sh -c #(nop)  EXPOSE 5000                  0B        
    - f9bb4486fd30   25 seconds ago       /bin/sh -c #(nop)  ENV API_URL=http://localh…   0B        
    - cf13989b2a63   25 seconds ago       /bin/sh -c npm install -g serve                 5.38MB    
    - 91fcdeec4567   29 seconds ago       /bin/sh -c npm install                          222MB     
    - 0e8f3eb0454b   48 seconds ago       /bin/sh -c git clone https://github.com/dock…   919kB     
    - 76cb2cf3a50c   50 seconds ago       /bin/sh -c apt-get update && apt-get install…   212MB     
    - 1f305ef2b397   About a minute ago   /bin/sh -c curl -sL https://deb.nodesource.c…   33.6MB    
    - 58e2b16f0f03   About a minute ago   /bin/sh -c apt-get update && apt-get install…   46.7MB    
    - 1caa3a58751e   About a minute ago   /bin/sh -c #(nop) WORKDIR /mydir                0B        
- Post-optimization: `543 MB`, with
    - bececca65a1e   3 minutes ago   /bin/sh -c #(nop)  CMD ["npm" "start"]          0B        
    - be65ef8cd26c   3 minutes ago   /bin/sh -c #(nop)  EXPOSE 5000                  0B        
    - 878107b6c898   3 minutes ago   /bin/sh -c #(nop)  ENV API_URL=http://localh…   0B        
    - d171419ec3ad   3 minutes ago   /bin/sh -c apt-get update     && apt-get ins…   412MB     
    - 5e7f7e0ac077   3 minutes ago   /bin/sh -c #(nop) WORKDIR /mydir                0B        


## [Backend](https://github.com/SonTrungTo/DevOps-2020-Helsinki/blob/master/docker_part1/1_11/Dockerfile)
- Pre-optimiztion: `443 MB`, with
    - 41621e2f3f47   6 minutes ago   /bin/sh -c #(nop)  CMD ["npm" "start"]          0B        
    - f1149d8ed0ba   6 minutes ago   /bin/sh -c #(nop)  EXPOSE 8000                  0B        
    - e7d371328db5   6 minutes ago   /bin/sh -c #(nop)  ENV FRONT_URL=http://loca…   0B        
    - bef15d661b29   6 minutes ago   /bin/sh -c npm install                          19.6MB    
    - ade1a2a81bf2   6 minutes ago   /bin/sh -c git clone https://github.com/dock…   227kB     
    - 54cefde6b2f4   6 minutes ago   /bin/sh -c apt-get update && apt-get install…   212MB     
    - 6de674ce8cb2   7 minutes ago   /bin/sh -c curl -sL https://deb.nodesource.c…   33.6MB    
    - dad5faa99237   7 minutes ago   /bin/sh -c apt-get update && apt-get install…   46.7MB    
    - 5e7f7e0ac077   8 minutes ago   /bin/sh -c #(nop) WORKDIR /mydir                0B        
- Post-optimization: `336 MB`, with
    - 0fb9cd3f71ad   About a minute ago   /bin/sh -c #(nop)  CMD ["npm" "start"]          0B        
    - 037883fcf2f7   About a minute ago   /bin/sh -c #(nop)  EXPOSE 8000                  0B        
    - 8ebecc6ea98b   About a minute ago   /bin/sh -c #(nop)  ENV FRONT_URL=http://loca…   0B        
    - 8af46713cb8c   About a minute ago   /bin/sh -c apt-get update     && apt-get ins…   204MB
    - 33e0f564eda6   2 minutes ago        /bin/sh -c #(nop) WORKDIR /mydir                0B        
