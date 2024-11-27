
# 👨‍👩‍👦‍👦 Rollingpaper Server 👨‍👩‍👦‍👦

![License](https://img.shields.io/badge/license-MIT-blue)
![Language](https://img.shields.io/badge/language-JavaScript-yellow)
![DBMS](https://img.shields.io/badge/DBMS-MariaDB-lightblue)
![Deployment](https://img.shields.io/badge/deploy-AWS-green)

한 사람을 위해 마음을 전달하는 온라인 롤링페이퍼! 👉 [https://rollingpaper.site/](https://rollingpaper.site/)

---

## 📖 Description

오프라인에 존재했던 롤링페이퍼 서비스를 온라인으로 옮겨왔습니다.  
친구들, 동료들과 함께 링크를 공유하여 한 사람을 위한 롤링페이퍼를 만들어보세요.  
다양한 종류의 편지지와 스티커로 화면을 꾸미고, 소중한 사람에게 뜻깊은 경험을 선물하세요!

---

## 🐤 Demo

(아래에는 서비스 화면을 보여주는 이미지를 추가하세요.)

---

## ⭐ Main Features

1. **정기 결제 기능**  
   - 아임포트(Iamport)를 이용한 정기 결제 기능 구현
2. **회원가입 및 로그인**  
   - JWT(Json Web Token) 기반 인증 구현
3. **기타 기능**  
   - 상품 리스트 조회 및 세부 사항 조회
   - 마이페이지 기능 구현

---

## 💻 Getting Started

### Installation
```bash
npm install
```

### Develop Mode
```bash
npm run dev
```

### Production
```bash
npm run build
```

---

## 🔧 Stack

- **Language**: JavaScript
- **Library & Framework**: Node.js
- **Database**: AWS RDS (MariaDB)
- **ORM**: Sequelize
- **Deployment**: AWS EC2

---

## 📂 Project Structure

```
src
├── common
│   ├── config
│   ├── types
│   └── utils
│       ├── types
│       └── utils
├── controller
├── entity
├── infrastructure
│   ├── express
│   └── typeorm
├── repository
└── ser
```

---

## 🔨 Server Architecture

(아키텍처 다이어그램을 이미지로 첨부하세요.)

---

## ⚒ CI/CD

- **CI/CD 도구**: GitHub Actions를 활용하여 지속적 통합 및 배포 구현
- **Workflow**:
  1. **Feature 브랜치**: `feature` 브랜치에서 `dev`로 Pull Request를 생성 시 CI 동작
  2. **Dev 브랜치**: `dev`에서 `master`로 Pull Request를 생성 시 CI 동작 및 운영 리소스에 자동 배포

---

## 👨‍💻 Role & Contribution

### Frontend (Web)
- 관리자 페이지 (Vue.js) 개발
- 전체 아키텍처 구성

### DevOps
- CI/CD 구축 (Docker, GitHub Actions)
- 서버 모니터링

### 기타
- 전체 개발 일정 및 이슈 관리

---

## 👨‍👩‍👧‍👦 Developer

| 이름   | 역할              | 주요 기여 사항                          |
|--------|-------------------|------------------------------------------|
| 홍길동 | Backend Developer | API 설계 및 데이터베이스 구축            |
| 김철수 | Frontend Developer| 관리자 페이지 및 UI 컴포넌트 구현        |
| 이영희 | DevOps Engineer   | CI/CD 파이프라인 구축 및 배포 관리       |

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

