Run node on digital ocean server
  
  https://www.digitalocean.com/community/tutorials/how-to-set-up-a-node-js-application-for-production-on-ubuntu-16-04

  https://www.youtube.com/watch?v=RE2PLyFqCzE

  $10 FREE SIGNUP LINK:
  https://m.do.co/c/5424d440c63a

  Flightplan?

  new vps = droplet
    -VPS - Virtual Private Server

  Create an account on digital ocean.

  Create Droplet
    -selected distribution
    -$5 a month

  download putty (for windows)
    -and download puttygen
      -Mac - https://www.puttygen.com/#Download_PuTTYgen_for_Mac
      -brew install putty

      -ssh-keygen
      -cat ~/.ssh/id_rsa.pub

  Open puttyGen to create a key

  copy the key

  paste into signup page
    -name as "public key 1"

  save key from puttygen to desktop

  create droplet... now wait



  click on droplet
    -shows info
    -access - accesses the console
    -resize - change the size of droplet
    -backup - $1 extra a month to backup
    -snapshots - are free

  ssh creditials
    -username: root
    -auth: ssh-key

  create new user after sshing

  Make user admin
    -usermod -aG sudo [username]
    -whoami - identifies you

  (ssh key is one line) 

  Remove password login and root login

  WinSCP ?

  

  Run the node server after installing node, works like it does locally.



  PM2 (runs node app as a service)
    -sudo npm install -g pm2

    pm2 start [entry point of app (ex: app.js )]
    pm2 stop [entry point]


  get a new domain. 
    name servers are 
      -ns1.digitalocean.com
      -ns2.digitalocean.com
      -ns3.digitalocean.com

  Change port to port 80 so its not in the browser
    -change port in [entry file]

    -sudo apt-get install libcap2-bin

    -sudo setcap cap_net_blind_service=+ep `readlink -f \`which node\``

      (binds node service to port 80)

    Then run pm2 start [entry point]