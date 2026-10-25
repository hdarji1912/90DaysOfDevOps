# Day 32 - Docker Volumes & Networking

## Objective

Learn how Docker manages persistent data using **Named Volumes** and **Bind Mounts**, understand Docker networking concepts, enable container-to-container communication, and build a simple multi-container application using custom networks and persistent storage.

---

## Prerequisites

- Docker Engine installed
- Basic Linux command knowledge
- Internet connection to pull Docker images

---

## Technologies Used

- Docker
- MySQL
- Nginx
- Alpine Linux
- Ubuntu EC2

---

# Task 1: The Problem (Container Data Loss)

### 1. Run a MySQL Container

Started a MySQL container and created a sample database with employee records.

![Run MySQL Container](images/1.png)

---

### 2. Create Sample Data

Created a table, inserted sample records, and verified the stored data.

![Create Database and Insert Records](images/2.png)

---

### 3. Remove the Container

Stopped and removed the MySQL container.

![Remove MySQL Container](images/3.png)

---

### 4. Create a New Container

Started a new MySQL container using the same image and verified whether the previous data still existed.

![Create New Container](images/4.png)

![Delete Containers](images/5.png)

### Key Observation

- User-created tables and records were lost.
- Containers do not preserve data after removal.
- Docker containers are **ephemeral** by default.

---

# Task 2: Named Volumes

### 1. Create a Docker Named Volume

Created a persistent Docker volume and verified it.

![Create Docker Volume](images/6.png)

---

### 2. Run MySQL with the Volume

Started a MySQL container using the named volume.

![Run MySQL with Volume](images/7.png)

---

### 3. Store Database Records

Created the employee table, inserted records, and verified the data.

![Insert Employee Records](images/8.png)

---

### 4. Remove the Container

Stopped and removed the database container while keeping the volume.

![Remove Container](images/9.png)

---

### 5. Reuse the Same Volume

Started a new MySQL container using the existing named volume and verified that the data persisted.

![Reuse Named Volume](images/10.png)

### Key Observation

- Docker volumes remain even after containers are removed.
- Database records persisted successfully.
- Named Volumes provide persistent storage independent of containers.

---

# Task 3: Bind Mounts

### 1. Create a Website Directory

Created a local website directory and added an HTML page.

![Create Website Folder](images/11.png)

---

### 2. Run an Nginx Container with a Bind Mount

Mounted the local website directory inside the Nginx container.

![Run Nginx Container](images/12.png)

---

### 3. Access the Website

Verified that the website was served successfully through the browser.

![Browser Output](images/13.png)

---

### 4. Update the Website

Modified the HTML file on the host machine and refreshed the browser.

![Updated index.html](images/14.png)

![Updated Browser Output](images/15.png)

### Key Observation

- Host files synchronized instantly with the container.
- No container rebuild or restart was required.
- Bind Mounts are ideal for local development.

---

# Task 4: Docker Networking Basics

### 1. List Docker Networks

Listed all available Docker networks.

![List Docker Networks](images/16.png)

---

### 2. Inspect the Default Bridge Network

Inspected the default bridge network and viewed the connected containers.

![Inspect Bridge Network](images/17.png)

---

### 3. Test Communication Using IP Address

Retrieved the container IP address and successfully pinged it.

![Ping by IP Address](images/18.png)

---

### 4. Test Communication Using Container Name

Attempted to communicate with another container using its container name on the default bridge network.

### Key Observation

- Containers communicated successfully using IP addresses.
- Name-based communication failed on the default bridge network.
- The default bridge network does not provide automatic DNS-based name resolution.

---

# Task 5: Custom Networks

### 1. Create a Custom Bridge Network

Created a custom Docker bridge network named **my-app-net**.

![Create Custom Network](images/19.png)

---

### 2. Run Containers on the Custom Network

Started two Alpine containers connected to the custom network.

![Run Containers on Custom Network](images/20.png)

---

### 3. Test Name-Based Communication

Verified communication between containers using container names.

![Ping Using Container Name](images/21.png)

### Key Observation

- Docker automatically resolved container names.
- Containers communicated successfully without using IP addresses.
- User-defined bridge networks include Docker's embedded DNS service.

---

# Task 6: Build a Multi-Container Application

### 1. Create a Project Network and Volume

Created a custom network (**project-net**) and a named volume (**project-data**).

![Create Project Network](images/22.png)

---

### 2. Run the Database Container

Started a MySQL database container attached to the custom network and persistent volume.

![Run Database Container](images/23.png)

---

### 3. Run the Application Container

Started an Alpine application container on the same network.

![Run Application Container](images/24.png)

---

### 4. Verify Container Communication

Verified that the application container successfully communicated with the database container using its container name.

![Verify Communication](images/25.png)

---

### 5. Cleanup

Removed all containers, custom networks, and Docker volumes created during the lab.

![Cleanup](images/26.png)

---

# 🚀 Key Learnings

- Containers are ephemeral and lose data when removed.
- Docker Named Volumes provide persistent storage independent of containers.
- Bind Mounts synchronize host files directly with containers.
- Docker Bridge Networks enable container communication using IP addresses.
- User-defined Bridge Networks provide automatic DNS-based name resolution.
- Container names can be used instead of IP addresses on custom networks.
- Volumes and custom networks simplify multi-container application deployment.
- Cleaning up unused Docker resources helps maintain a healthy Docker environment.
