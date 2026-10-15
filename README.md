# DE TAI 7: HE THONG BLOG CMS VA MONITORING STACK HOAN CHINH

- Ma sinh vien / Du an: DTC245220023-Blog-CMS
- He dieu hanh / Moi truong: Windows 10/11, Docker Desktop, Git Bash
- Repository GitHub: [https://github.com/dhuy841/DTC245220023-Blog-CMS.git](https://github.com/dhuy841/DTC245220023-Blog-CMS.git)

1. Danh sach Dich vu & Cong Truy cap:
- Website Ghost CMS (HTTPS): https://localhost
- Quan tri CSDL phpMyAdmin: https://localhost/phpmyadmin/
- Prometheus Dashboard: http://localhost:9090
- Grafana Visualization: http://localhost:3000
- Loki Log API: http://localhost:3100/ready

2. Huong dan Khoi chay He thong:
docker compose up -d

3. Cac truy van LogQL tren Grafana (Loki + Promtail):
- Xem toan bo log Nginx: {container="nginx_proxy"}
- Loc log loi: {container=~".+"} |= "error"
- Xem log Ghost kết noi CSDL: {container="blog_app"} |= "mysql"
