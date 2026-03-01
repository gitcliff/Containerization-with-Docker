# Docker Volumes - Persisting Data


# 📖 Summary

Worked on **Docker Volumes: Persisting Data**, focusing on **Docker Compose, Docker volumes, and data persistence in containerized applications**.
Tasks included setting up Docker volumes to persist MongoDB data across container restarts, solving the challenge of ephemeral container storage that causes data loss.
Set up Docker Compose and local Docker volumes to automate persistent data storage for MongoDB, aiming to maintain user data integrity during container lifecycle events.

---

# 🛠️ Tools Used

* **Docker Compose**: ✨ *Orchestrated multi-container application setup and defined volume mappings.*
* **MongoDB**: ⚙️ *Served as the database requiring persistent storage for data durability.*
* **Docker CLI**: 🚀 *Managed containers lifecycle, volume inspection, and testing of persistent storage.*

---

# 🎯 Skills Gained

* **Docker Volumes Management**: 💡 *Learned how to define and attach volumes in Docker Compose to persist container data.*
* **Container Lifecycle Handling**: 🔍 *Gained experience in stopping, restarting, and validating data persistence across container restarts.*
* **Filesystem Exploration in Containers**: 🚀 *Practiced using commands like `docker exec` and `nsenter` to inspect host and container file systems.*

---

# ⚠️ Challenges Faced

* **Understanding Container Ephemerality**: 🛠️ *Overcame data loss issues by configuring volumes, shifting from ephemeral storage to persistent volumes.*
* **Accessing Docker Host Filesystem**: 🔄 *Used `nsenter` and container exec commands to inspect volume directories and confirm data persistence.*

---

# 💡 Why It Matters

This lab strengthens expertise in **DevOps and container orchestration**, demonstrating how tools like **Docker volumes and Docker Compose** improve software delivery through persistent data management.
Mastering these skills supports efficient, reliable CI/CD practices essential in modern cloud-native application deployments. 🚀🌐

---