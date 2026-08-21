# 🚀 CI/CD Learning Roadmap - Hành Trình Học Tập

## 📋 Mục Lục
1. [Giai Đoạn 1: Kiến Thức Cơ Bản](#giai-đoạn-1-kiến-thức-cơ-bản)
2. [Giai Đoạn 2: GitHub Actions Cơ Bản](#giai-đoạn-2-github-actions-cơ-bản)
3. [Giai Đoạn 3: Testing & Quality Control](#giai-đoạn-3-testing--quality-control)
4. [Giai Đoạn 4: Deployment Strategies](#giai-đoạn-4-deployment-strategies)
5. [Giai Đoạn 5: Advanced Topics](#giai-đoạn-5-advanced-topics)
6. [Giai Đoạn 6: Real-World Projects](#giai-đoạn-6-real-world-projects)

---

## Giai Đoạn 1: Kiến Thức Cơ Bản
**Thời gian: 1-2 tuần**

### 1.1 Hiểu Khái Niệm
- [ ] Tìm hiểu CI (Continuous Integration)
  - Continuous merging
  - Automated testing
  - Early bug detection
  
- [ ] Tìm hiểu CD (Continuous Delivery vs Deployment)
  - Continuous Delivery: manual deploy
  - Continuous Deployment: automatic deploy
  
- [ ] Hiểu quy trình CI/CD pipeline
  - Git workflows
  - Webhook & event triggers
  - Build & test stages
  - Deployment targets

### 1.2 Các Khái Niệm Liên Quan
- [ ] Version Control (Git cơ bản)
  - Commit, Push, Pull, Merge
  - Branches & Pull Requests
  
- [ ] Build Tools
  - npm, Maven, Gradle, Go build, etc.
  - Build artifacts
  
- [ ] Docker (optional nhưng rất hữu ích)
  - Containerization basics
  - Docker images & containers

### 1.3 Tài Liệu Tham Khảo
- 📚 GitHub Docs: Tìm hiểu CI/CD
- 📚 "The DevOps Handbook" - chương về CI/CD
- 📺 YouTube: CI/CD explained in 5 minutes

---

## Giai Đoạn 2: GitHub Actions Cơ Bản
**Thời gian: 2-3 tuần**

### 2.1 GitHub Actions Fundamentals
- [ ] Hiểu cấu trúc workflow
  - Workflows, Jobs, Steps
  - Runners (GitHub-hosted vs Self-hosted)
  - Events (push, pull_request, schedule, etc.)

- [ ] Workflow Syntax
  ```yaml
  name: Learn CI/CD
  on: [push, pull_request]
  jobs:
    build:
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v3
        - name: Run a one-line script
          run: echo Hello, world!
  ```

### 2.2 Bài Tập Thực Hành
- [ ] **Bài 1**: Tạo workflow đầu tiên (Hello World)
  - Tạo `.github/workflows/hello.yml`
  - Trigger on push
  - Print "Hello World"
  - Xem logs

- [ ] **Bài 2**: Chạy Node.js project
  - Setup Node.js
  - npm install & npm test
  - Xem kết quả test

- [ ] **Bài 3**: Chạy Python project
  - Setup Python
  - pip install dependencies
  - Run tests with pytest

### 2.3 Tài Liệu Tham Khảo
- 📖 GitHub Actions Official Docs
- 📖 GitHub Actions Quickstart
- 🔗 https://docs.github.com/en/actions

---

## Giai Đoạn 3: Testing & Quality Control
**Thời gian: 2-3 tuần**

### 3.1 Unit Testing
- [ ] Viết Unit Tests
  - Jest (JavaScript)
  - Pytest (Python)
  - JUnit (Java)
  
- [ ] Tích hợp Testing vào CI/CD
  - Chạy test tự động mỗi khi commit
  - Fail job nếu test không pass

### 3.2 Code Quality Tools
- [ ] Linting
  - ESLint, Prettier (JavaScript)
  - Pylint, Black (Python)
  
- [ ] Code Coverage
  - Đo coverage % trong CI
  - Tăng coverage khi commit mới
  
- [ ] SonarQube / CodeClimate
  - Code quality reports
  - Security checks

### 3.3 Bài Tập Thực Hành
- [ ] **Bài 4**: Automated Testing Pipeline
  - Chạy unit tests tự động
  - Report test results
  - Block merge nếu test fail
  
- [ ] **Bài 5**: Code Quality Checks
  - Linting trong CI
  - Coverage reports
  - Quality gates

### 3.4 Tài Liệu Tham Khảo
- 📖 Jest Documentation
- 📖 Pytest Documentation
- 📖 GitHub Actions & Testing Best Practices

---

## Giai Đoạn 4: Deployment Strategies
**Thời gian: 3-4 tuần**

### 4.1 Deployment Basics
- [ ] Hiểu deployment environments
  - Development
  - Staging
  - Production
  
- [ ] Deployment methods
  - FTP/SFTP
  - SSH
  - Cloud platforms (Vercel, Netlify, Heroku)
  - Docker registries

### 4.2 Cloud Platforms
- [ ] **Vercel** (Frontend)
  - Deploy Next.js apps
  - Preview deployments
  
- [ ] **Netlify** (Static & JAMstack)
  - Deploy static sites
  - Build & deploy automatically
  
- [ ] **Heroku** (Backend)
  - Deploy Node.js/Python apps
  - Database management
  
- [ ] **AWS** / **Google Cloud** / **Azure**
  - EC2, App Engine, App Service
  - More complex but powerful

### 4.3 Bài Tập Thực Hành
- [ ] **Bài 6**: Deploy to Vercel
  - Setup GitHub integration
  - Auto-deploy on push
  - Preview PRs
  
- [ ] **Bài 7**: Deploy to Heroku
  - Docker container deployment
  - Environment variables
  - Database setup
  
- [ ] **Bài 8**: Multi-environment Deployment
  - Deploy to staging on PR
  - Deploy to prod on merge to main

### 4.4 Tài Liệu Tham Khảo
- 📖 Vercel Documentation
- 📖 Netlify Documentation
- 📖 Heroku Getting Started

---

## Giai Đoạn 5: Advanced Topics
**Thời gian: 3-4 tuần**

### 5.1 Docker & Container Orchestration
- [ ] Docker fundamentals
  - Dockerfile
  - Building images
  - Running containers
  
- [ ] Publishing to Docker Registry
  - Docker Hub
  - GitHub Container Registry (GHCR)
  - Push in CI/CD pipeline
  
- [ ] Kubernetes basics (optional)
  - Pods, Services, Deployments
  - CI/CD with K8s

### 5.2 Advanced Workflow Techniques
- [ ] Caching & Dependencies
  - npm cache, pip cache
  - Faster builds
  
- [ ] Matrix Builds
  - Test on multiple Node versions
  - Test on multiple OS
  
- [ ] Secrets & Environment Variables
  - Secure credentials
  - GitHub Secrets
  - Using in workflows
  
- [ ] Artifacts & Releases
  - Upload build artifacts
  - Create releases
  - Publish to npm/PyPI

### 5.3 Monitoring & Logging
- [ ] Job logging
  - Debug mode
  - Custom logging
  
- [ ] Notifications
  - Slack integration
  - Email alerts
  - GitHub notifications

### 5.4 Bài Tập Thực Hành
- [ ] **Bài 9**: Docker in CI/CD
  - Build Docker image in CI
  - Push to Docker Hub
  - Deploy container
  
- [ ] **Bài 10**: Matrix Testing
  - Test on multiple Node versions
  - Test on Ubuntu, Windows, macOS
  
- [ ] **Bài 11**: Publish to npm
  - Build & test
  - Publish on version tag
  - Semantic versioning

### 5.5 Tài Liệu Tham Khảo
- 📖 Docker Official Docs
- 📖 GitHub Actions Advanced Usage
- 📖 Kubernetes Basics

---

## Giai Đoạn 6: Real-World Projects
**Thời gian: 4-6 tuần**

### 6.1 Mini Projects
- [ ] **Project 1**: Simple Web App (Frontend + Backend)
  - React/Vue frontend
  - Node.js backend
  - Test & deploy both
  
- [ ] **Project 2**: Full Stack App with Database
  - Frontend (React/Vue)
  - Backend (Node.js/Python)
  - Database (MongoDB/PostgreSQL)
  - Deploy to staging & production
  
- [ ] **Project 3**: Microservices
  - Multiple services
  - Docker for each service
  - Deploy orchestration
  
- [ ] **Project 4**: Open Source Contribution
  - Contribute to existing project
  - Work with their CI/CD
  - Learn team practices

### 6.2 Best Practices
- [ ] Security in CI/CD
  - Dependency scanning
  - Secret management
  - Code scanning
  
- [ ] Performance Optimization
  - Parallel jobs
  - Caching strategies
  - Build optimization
  
- [ ] Disaster Recovery
  - Rollback strategies
  - Health checks
  - Monitoring

### 6.3 Learning Resources
- 📖 GitHub Actions Marketplace
- 📖 Real-world workflow examples
- 🔗 https://github.com/sdras/awesome-actions
- 📺 YouTube channels chuyên về DevOps

---

## 📊 Timeline Tóm Tắt
```
Giai Đoạn 1 (Cơ Bản):           1-2 tuần
Giai Đoạn 2 (GitHub Actions):   2-3 tuần
Giai Đoạn 3 (Testing):          2-3 tuần
Giai Đoạn 4 (Deployment):       3-4 tuần
Giai Đoạn 5 (Advanced):         3-4 tuần
Giai Đoạn 6 (Projects):         4-6 tuần
━━━━━━━━━━━━━━━━━━━━━━━━━━━
Tổng cộng:                      15-22 tuần (~4-6 tháng)
```

---

## 🎯 Mẹo Học Hiệu Quả
1. **Hands-on Practice**: Làm bài tập thực hành, không chỉ đọc lý thuyết
2. **Start Small**: Bắt đầu với hello world, sau đó phức tạp dần
3. **GitHub Repository**: Tạo repo riêng để thực hành
4. **Read Workflows**: Tìm hiểu workflows của các project nổi tiếng
5. **Join Community**: Discord, Reddit, GitHub Discussions
6. **Debugging**: Đọc logs kỹ khi có lỗi - đây là cách học tốt nhất

---

## 🚀 Bắt Đầu Ngay Hôm Nay
Hãy chọn một bài tập từ Giai Đoạn 2.1 và bắt đầu!

```bash
# 1. Clone repo của bạn
git clone https://github.com/prosaigon/ci-cd-learning.git
cd ci-cd-learning

# 2. Tạo folder workflows
mkdir -p .github/workflows

# 3. Tạo file hello.yml
# 4. Thêm vào git & push
git add .github/workflows/hello.yml
git commit -m "Add hello world workflow"
git push

# 5. Xem GitHub Actions tab trong repo
```

---

**Bạn sẵn sàng bắt đầu chưa? 🚀**
