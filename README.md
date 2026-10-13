# devops-lab1-portfolio

Lab 1 — DevOps Course: My First CI/CD Pipeline

## Thông tin Lab
- **Mục tiêu:** Trải nghiệm DevOps Workflow End-to-End (Plan → Code → Build → Test → Deploy → Monitor)
- **Công cụ:** Git, GitHub Actions, GitHub Pages
- **Tác giả:** QuanDev-thaiNG

## Cấu trúc Repository
```
devops-lab1-portfolio/
├── .github/
│   └── workflows/
│       └── deploy.yml    # CI/CD Pipeline GitHub Actions
├── index.html            # Mã nguồn trang Web tĩnh Portfolio
└── README.md             # Tài liệu hướng dẫn
```

## DevOps CI/CD Pipeline
Mỗi khi push code lên nhánh `main`, GitHub Actions sẽ tự động:
1. Checkout code
2. Kiểm tra tính hợp lệ của mã nguồn (`index.html`)
3. Tự động deploy lên nhánh `gh-pages` để phát hành trang web qua GitHub Pages.
