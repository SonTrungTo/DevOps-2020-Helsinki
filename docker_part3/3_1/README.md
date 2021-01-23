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

## [Backend](https://github.com/SonTrungTo/DevOps-2020-Helsinki/blob/master/docker_part1/1_11/Dockerfile)
