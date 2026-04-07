# 🚀 DevOps Learning Notes

## 📋 Table of Contents

- [Linux](#Linux)

---

## Linux 

**📌 Key Takeaways:**

- apps -> shell -> kernel -> Hardware (architecture)


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

---



## 🛠️ Tools I'm Learning

| Tool                 | Category           | Status         |
| -------------------- | ------------------ | -------------- |
| Git                  | Version Control    | ⬜ Not started |
| Docker               | Containerization   | ⬜ Not started |
| Kubernetes           | Orchestration      | ⬜ Not started |
| Jenkins              | CI/CD              | ⬜ Not started |
| Terraform            | IaC                | ⬜ Not started |
| Ansible              | Configuration Mgmt | ⬜ Not started |
| AWS / GCP / Azure    | Cloud              | ⬜ Not started |
| Prometheus + Grafana | Monitoring         | ⬜ Not started |
| Linux                | OS                 | 🔄 In Progress |

> Update status: ⬜ Not started → 🔄 In Progress → ✅ Done

---

## 📚 Resources

- 🎥 [My Playlist](https://www.youtube.com/watch?v=e01GGTKmtpc&list=PLlfy9GnSVerQjeoYfoYKEMS1yKl89NOvL)
- 📖 [roadmap.sh/devops](https://roadmap.sh/devops) — DevOps learning roadmap
- 🐳 [Docker Docs](https://docs.docker.com)
- ☸️ [Kubernetes Docs](https://kubernetes.io/docs)
- 🌿 [Git Handbook](https://guides.github.com/introduction/git-handbook/)

---

