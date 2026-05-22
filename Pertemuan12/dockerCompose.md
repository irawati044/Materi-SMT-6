# Deploy Multiple Container menggunakan Docker Compose Start Instance EC2 di AWS

1. Start Instance EC2 di AWS
2. Patching OS
3. Uninstall semua Services manual sebelumnya
4. Repositori baru untuk web dinamis di docker hub alt text
![alt text](image.png)
5. Buka Projek Company himafor_nim
6. Bagi 2 Folder untuk projek Web App Statis dan Dinamis
7. Move file index dan Dcoker milik web statis ke Folder web-statis
8. Copy Folder Projek Next.JS (pertemuan9)ke folder web-dinamis
9. Lakukan Testing di Local Project Next.JS
    - Install Dependencies: npm install
    - Create user di DBMS : sudo mysql -u root -p
        - CREATE USER 'userweb_23880100025'@'localhost' IDENTIFIED BY 'PXwA6o[sUQ9v-X)i';
        - GRANT ALL PRIVILEGES ON *.* TO 'userweb_23880100025'@'localhost';
        - FLUSH PRIVILEGES;
        - exit; alt text
![alt text](<Screenshot 2026-05-22 090033.png>)

        - Edit File .env di folder web-dinamis
        - npm run build
        - npm start
        - Pastikan web dapat diakses di http://localhost:3000 admin tanpa error alt text
10. Buat file Dockerfile
11. Buat file docker-compose.yml
12. Buat Workflows File -> deploy-dinamis.yml di folder .github/workflows/ dari Projek web-dinamis
13. Edit File -> deploy.yml di folder .github/workflows/ untuk
14. Update Host AWS di Github
15. Commit Changes ke GitHub dari lokal
16. Push Changes ke GitHub
17. Cek di Github, apakah actions jalan dan berhasil alt text
![alt text](<Screenshot 2026-05-22 133845.png>)
18. Cek di AWS, apakah container berjalan dengan baik alt text
![alt text](<Screenshot 2026-05-22 135845.png>)
19. Akses web melalui Browser login admin edit Layanan alt text
![alt text](<Screenshot 2026-05-22 135345.png>)
Referensi :

https://github.com/moh-firdaus/himafor_nim