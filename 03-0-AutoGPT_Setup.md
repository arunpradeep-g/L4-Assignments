### **🔧 System Requirements**



#### **Hardware:**



CPU: Minimum 4 cores (8+ recommended)



RAM: Minimum 8GB (16GB recommended)



Storage: At least 10GB free (20GB+ recommended for development)



#### **Software:**



##### **Operating Systems:**



Linux (Ubuntu 20.04 or newer recommended)



macOS (10.15 or newer)



Windows 10/11 with WSL2 enabled (Docker requires WSL2 backend)



Required Tools:



Docker Engine: v20.10.0 or newer



Docker Compose: v2.0.0 or newer



Git: v2.30 or newer



Node.js: v16.x or newer (v22.x recommended for frontend dev)



npm: v8.x or newer (or pnpm v8.x for frontend)



VSCode: v1.60+ or any modern editor



### **Installation on Ubuntu:**



##### **Prerequisites:**



1. Git (≥ 2.30) → sudo apt install git



2\. Docker Engine (≥ 20.10) → sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin



3\. Docker Compose (≥ 2.0) → sudo apt install docker-compose-plugin



4\. Node.js (≥ 16.x, ideally 22.x) → sudo apt install nodejs npm



5\. npm (≥ 8.x) → included with Node.js





#### 🛠 **Manual Installation**



1. **Clone the repo:**



git clone https://github.com/Significant-Gravitas/AutoGPT.git



cd AutoGPT



**2. Configure Environment:**



cp .env.default .env ( Use custom.env format )



**3. Install Security dependencies:**



sudo apt install ca-certificates curl

sudo install -m 0755 -d /etc/apt/keyrings

sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc

sudo chmod a+r /etc/apt/keyrings/docker.asc

sudo tee /etc/apt/sources.list.d/docker.sources <<EOF

Types: deb

URIs: https://download.docker.com/linux/ubuntu

Suites: $(. /etc/os-release \&\& echo "${UBUNTU\_CODENAME:-$VERSION\_CODENAME}")

Components: stable

Architectures: $(dpkg --print-architecture)

Signed-By: /etc/apt/keyrings/docker.asc

EOF



**4. Build:**



sudo docker compose build --progress=plain



**5. Start services:**



sudo docker compose up -d



**6. Access frontend:**



Open browser → http://localhost:3000

