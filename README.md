# 🚀 DevOps Learning Notes

## 📋 Table of Contents

- [Linux](#Linux)
- [Git](#Git)
- [Docker](#Docker)

---

## Linux

**📌 Key Takeaways:**

- apps -> shell -> kernel -> Hardware (architecture)

- ![My Image](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSd4RaKP8eP36c_V2FHPq8jEueltHrpd3S2nA&sg "This is a tooltip")

**💡 New Terms Learned:**
| Term | Meaning |
|------|---------|
| kernel | System Hart |
| bootloader | GRUB first time system start that time run |
| shell | kernel connect to user |

---

### ⌨️ Commands Cheatsheet

#### Basci

```bash
    ls                  (showing files/floders)
    cd                  (change floder )
    pwd                 (current path showing)
    mkdir               (create floder)
    rm                  (delete file)
    rm -r               (delete floder)
    rm -v file_name     (delete file with showing)
    cat                 (file read)
    zat                 (zip floder)
    touch | nano        (create file)

    cp                  (copy file)
    mv                  (move file)
    wc                  (in file word count)
    hard | soft link    (shortcut link created)

    df                  (disk usage)
    du                  (disk usage)
    ps                  (process usage)
    top                 (process usage)
    kill                (process usage)
    nohup               (process usage)
    free                (process usage)
```

#### System-level

```bash
    uname                (which platfrom run)
    uptime               (start time)
    who                  (kon se user ne kab login kiya tha, how many user login this system)
    whoami               (only one user retuen )
    which                (location)
    id                   (get user uid | gid)
    sudo                 (super user do)
    cat /etc/passwd      (list of users)
    sudo shutdown        (power off)
    sudo apt             (application pakage managner)
    sudo apt-get         (download on own system get to internet pkg)
    sudo apt-get update  (system update)
    sudo apt remove pkg  (delete application/pkg)
```

#### User & Group management

```bash
    sudo useradd -m name (addon new user)
    sudo passwd name     (create user password)
    su name              (switch user)
    sudo userdel name    (delete user)
    sudo groupadd name (create new group)
    sudo gpasswd -a username groupname (addon user to groups)
    sudo gpasswd -M username,username groupname (mutiple user addon one group)
    sudo groupdel groupname (group delete)
```

#### File permission

```bash
  ls -l                     (check folder permission)
  chmod 777 flodername      (change folder permission)
  sudo chown username filename  (change ownership)
  sudo chgrp groupname filename (change groupname )
```

#### File Compression

```bash
    sudo zip -r ldf.zip flodername (floder make it compression)
    unzip flodername.zip  (make a file normal)
```

#### File transfer

```bash
    scp -i "selected_file_name.pem" "C:\Users\jaywa\Downloads\schema.prisma" ubuntu@ip.compute-1.amazonaws.com:/home/ubuntu (local to server file.floder send)

    scp -i "selected_file_name.pem" -r ubuntu@ip.compute-1.amazonaws.com:/home/ubuntu/devops .
    (server to local file.floder send)
```

#### NetWork

```bash
    ping url        (checking you site are run)
    sudo apt install net-tools
    netstat
    ifconfig
    traceroute url
    mtr             (ping + traceroute)
    nslookup        (which ip address run)
    hostname        (this server what ip)
    iwconfig
    ss
    dig url         (this site where hosted)
    whois url       (in datils showing using domin name)
    arp             (find mac address)
    wget            (any download link click and pasted on server)
    watch -n 2 top           (everey 2s new logs showing)
    nmap               (check how many port are open)
```

### PRO

```bash
    haed -n 2 app.log    (in log file number line read)
    awk '{print}' app.log (in log file number line read)
    lsblk                 (show disk space)
     df -h                 (free space showing)
     create volumn on srevre
     1.lsblk
     2. sudo su
     3. lvm
     4. pvcreate /dev/nvme1n1 /dev/nvme2n1 /dev/nvme3n1
     5. pvs
     6. vgcreate tws-vg /dev/nvme1n1 /dev/nvme2n1
     7. vgs
    pv/vg display  (all info showing)
```

---

## Git

**📌 Key Takeaways:**

**💡 New Terms Learned:**
| Term | Meaning |
|------|---------|
| GIT | Tool for version control |
| GITHUB | store on cloud |
| | |

---

### ⌨️ Commands Cheatsheet

```bash
    git init (initializes an empty git repository)
    git status (gives the infomation of the current state of the git respository)
    git checkout -b branch_name (create a new branch)
    git restore --staged filename
    git logs
    git revert logID
```

## Docker

**📌 Key Takeaways:**

- Docker Architecture
  Engine -> Demon (DockerD -> containerD)->CLI->Client (API)

- Docker Network
  1. Host
  2. Bridge (default)
  3. User defined Bridge (Custom)
  4. None
  5. MACVLAN (docker swarm)
  6. IPVLAN
  7. Overlay

**💡 New Terms Learned:**
| Term | Meaning |
|------|---------|
| | |
| | |
| | |

---

### ⌨️ Commands Cheatsheet

```bash
    sudo usermod -aG docker $USER
    docker ps (running container show)
    newgrp docker
    docker pull imgae_name (image on server)
    docker images (check it image info)
    docker run image_name (create container)
    docker run -d -e MYSQL_ROOT_PASSWORD=root mysql
    docker exec -it container_id bash

    docker stop container_id
```

```bash
    nano Dockerfile (make it file addon cmd)
    docker build -t app_name .
    docker run -d -p 80:80 app_name (web app run as a port)
    docker logs container_id
    docker attach container_id (real time showing logs)
    mysql -u root -p
    docker run -itd image_name (all time run)
```

#### Network

```bash
    docker network create net_name -d bridge

    docker network ls


docker run -d \
  --name mysql \
  --network two-tier \
  -v mysql-data:/var/lib/mysql \
  -e MYSQL_ROOT_PASSWORD=root \
  -e MYSQL_DATABASE=devops \
  mariadb:10.5

    docker run -d \
  -p 5000:5000 \
  --network two-tier \
  -v mysql-data:/var/lib/mysql \
  -e MYSQL_HOST=mysql \
  -e MYSQL_USER=root \
  -e MYSQL_PASSWORD=root \
  -e MYSQL_DB=devops \
  two-tier-backend:latest
```

#### Volumes

```bash
   docker volume create volume_name

   docker volume ls

   docker inspect volume_name (check it path)
```
#### Compose file

``` bash
version: "3.8"

services:
  mysql:
    container_name: mysql
    image: mysql
    environment:
      MYSQL_DATABASE: devops
      MYSQL_ROOT_PASSWORD: root
    ports:
      - "3306:3306"
    volumes:
      - mysql-data:/var/lib/mysql
    networks:
      - two-tier
    restart: always
    healthcheck:
      test: ["CMD", "mysqladmin", "ping", "-h", "localhost", "-uroot", "-proot"]
      interval: 10s
      timeout: 5s
      retries: 5
      start_period: 60s

  flask:
    build:
      context: .
    container_name: two-tier-backend
    ports:
      - "5000:5000"
    environment:
      MYSQL_HOST: mysql
      MYSQL_USER: root
      MYSQL_PASSWORD: root
      MYSQL_DB: devops
    depends_on:
      - mysql
    networks:
      - two-tier
    restart: always
    healthcheck:
      test: ["CMD-SHELL", "curl -f http://localhost:5000/health || exit 1"]
      interval: 10s
      timeout: 5s
      retries: 5
      start_period: 60sr

volumes:
  mysql-data:

networks:
  two-tier:


docker compose up -d 
docker compose down

docker system prune (not woking networks and images are remove)

docker images -aq (showing all imageid only)

docker push or docker pull

docker scout quickview image_name
docker scout cves image_name
```

## 🛠️ Tools I'm Learning

| Tool       | Category         | Status         |
| ---------- | ---------------- | -------------- |
| Linux      | OS               | ✅ Done        |
| Git        | Version Control  | ✅ Done        |
| Docker     | Containerization | ✅ Done        |
| Jenkins    | CI/CD            | 🔄 In Progress |
| AWS        | Cloud            | ✅ Done        |
| Kubernetes | Orchestration    | ⬜ Not started |
| Terraform  | IaC              | ⬜ Not started |
| Ansible    | Config Mgmt      | ⬜ Not started |
| GitLab     | DevOps Platform  | ⬜ Not started |
| ArgoCD     | GitOps           | ⬜ Not started |
| Shell      | Scripting        | ⬜ Not started |

> Update status: ⬜ Not started → 🔄 In Progress → ✅ Done

---

## 📚 Resources

- 🎥 [My Playlist](https://www.youtube.com/watch?v=e01GGTKmtpc&list=PLlfy9GnSVerQjeoYfoYKEMS1yKl89NOvL)
- 📖 [roadmap.sh/devops](https://roadmap.sh/devops) — DevOps learning roadmap
- 🐳 [Docker Docs](https://docs.docker.com)
- ☸️ [Kubernetes Docs](https://kubernetes.io/docs)
- 🌿 [Git Handbook](https://guides.github.com/introduction/git-handbook/)

---
