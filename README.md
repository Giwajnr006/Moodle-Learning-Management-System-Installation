# Moodle LMS Installation and Configuration – Newgate University Minna

This repository documents the complete offline installation, setup, configuration, testing, and usage of Moodle LMS on an Ubuntu Server for Newgate University Minna. The deployment includes fully functional modules such as course creation, lecture delivery, online exams, and result management.

## 📌 Project Highlights

- ✅ Offline installation of Moodle on Ubuntu Server
- ✅ Custom configuration for institutional use
- ✅ Fully tested with real users (screenshots included)
- ✅ Integrated features for:
  - 📚 Lectures (Course content upload & organization)
  - 📝 Online Examinations (Quiz, Assignments)
  - 📊 Results (Grading, Feedback, Report generation)

## 🖥️ System Requirements

- Ubuntu Server 22.04 LTS, 24.0 and more ....
- PHP 8.0+
- MySQL 8.0+
- Apache2 Web Server
- Moodle 4.x

## ⚙️ Offline Installation Steps on Ubuntu Server

# 1. Update system
sudo apt update && sudo apt upgrade -y

# 2. Install Apache, MySQL, PHP and required extensions
sudo apt install apache2 mysql-server php php-mysql php-xml php-curl php-gd php-intl php-mbstring php-zip php-soap php-bcmath php-cli unzip git -y

# 3. Start and enable Apache and MySQL
sudo systemctl enable apache2
sudo systemctl enable mysql
sudo systemctl start apache2
sudo systemctl start mysql

# 4. Secure MySQL installation
sudo mysql_secure_installation

# 5. Create Moodle Database and User
sudo mysql -u root -p
# 6. Download and extract Moodle
cd /var/www/html
sudo git clone -b MOODLE_401_STABLE git://git.moodle.org/moodle.git
sudo mkdir /var/www/moodledata
sudo chown -R www-data:www-data /var/www/moodledata
sudo chmod -R 755 /var/www/moodledata

# 7. Set permissions
sudo chown -R www-data:www-data /var/www/html/moodle

# 8. Open browser and complete web installation
# Visit: http://your-server-ip/moodle
# 6. Download and extract Moodle
cd /var/www/html
sudo git clone -b MOODLE_401_STABLE git://git.moodle.org/moodle.git
sudo mkdir /var/www/moodledata
sudo chown -R www-data:www-data /var/www/moodledata
sudo chmod -R 755 /var/www/moodledata

# 7. Set permissions
sudo chown -R www-data:www-data /var/www/html/moodle

# 8. Open browser and complete web installation
# Visit: http://your-server-ip/moodle
🧪 Testing & Deployment

✅ Local users created and enrolled in sample courses
✅ Admin dashboard customized
✅ Mock quizzes and exams executed successfully![WhatsApp Image 2025-04-18 at 1 10 12 PM](https://github.com/user-attachments/assets/d14d7b62-ed61-43e7-983d-2d4c3d7154f1)

✅ Screenshots available in /screenshots/ folder
![WhatsApp Image 2025-04-18 at 1 10 11 PM-3](https://github.com/user-attachments/assets/c108ac73-2cc3-4a5c-b3fc-3ec8d80e1f6c)

![WhatsApp Image 2025-04-18 at 1 15 14 PM](https://github.com/user-attachments/assets/97f8fb53-7ed8-44d8-ab4d-1fc81f378fdd)

📍 Institution

Newgate University Minna
Department of ICT & E-learning

🤝 Acknowledgements

Special thanks to the technical team and testers at Newgate University Minna for making this deployment successful.
