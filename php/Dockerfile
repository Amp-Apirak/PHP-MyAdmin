# Dockerfile

# เลือกใช้ Base Image PHP + Apache เวอร์ชัน 8.0
FROM php:8.0-apache

# อัปเดตแพ็กเกจในระบบ
RUN apt-get update && apt-get upgrade -y

# ติดตั้ง PHP Extensions ที่ต้องการ
# - mysqli
# - pdo
# - pdo_mysql
# จากนั้นสั่ง enable
RUN docker-php-ext-install mysqli pdo pdo_mysql \
    && docker-php-ext-enable mysqli pdo pdo_mysql

# คุณสามารถเพิ่มคำสั่งอื่น ๆ ได้ตามต้องการ เช่น เปิด mod_rewrite, copy ไฟล์, etc.
# ตัวอย่าง:
# RUN a2enmod rewrite
# COPY . /var/www/html
