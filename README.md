# 🚀 DevOps Learning Notes

## 📋 Table of Contents

- [Linux](#Linux)
- [Git](#Git)

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
| GIT   | Tool for version control |
| GITHUB  | store on cloud  |
|  |  |

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



## 🛠️ Tools I'm Learning

| Tool        | Category              | Status        |
|------------|----------------------|---------------  |
| Linux      | OS                   | ✅ Done        |
| Git        | Version Control      | ✅ Done        |
| Docker     | Containerization     | 🔄 In Progress |
| Jenkins    | CI/CD                | ⬜ Not started |
| AWS        | Cloud                | ✅ Done        |
| Kubernetes | Orchestration        | ⬜ Not started |
| Terraform  | IaC                  | ⬜ Not started |
| Ansible    | Config Mgmt          | ⬜ Not started |
| GitLab     | DevOps Platform      | ⬜ Not started |
| ArgoCD     | GitOps               | ⬜ Not started |
| Shell      | Scripting            | ⬜ Not started |

> Update status: ⬜ Not started → 🔄 In Progress → ✅ Done

---

## 📚 Resources

- 🎥 [My Playlist](https://www.youtube.com/watch?v=e01GGTKmtpc&list=PLlfy9GnSVerQjeoYfoYKEMS1yKl89NOvL)
- 📖 [roadmap.sh/devops](https://roadmap.sh/devops) — DevOps learning roadmap
- 🐳 [Docker Docs](https://docs.docker.com)
- ☸️ [Kubernetes Docs](https://kubernetes.io/docs)
- 🌿 [Git Handbook](https://guides.github.com/introduction/git-handbook/)

---

