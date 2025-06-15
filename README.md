# The Future of Retail-Go 
- NAME: Onah Samuel
- AltSchool ID: ALT/SOE/024/5913

## 📍 Project Description
This is a live-deployed dynamic landing page showcasing my role as a Cloud Engineer in a startup shaping the retail landscape with AI-powered self-checkout solutions. It would address the issue of long queues by instant payments via barcode scanning, ensuring a seamless experience for customers and operational efficiency for retail outlets.

## 🌐 Live Demo
**Public IP**: http://13.42.26.185  
**HTTPS**: https://myretailsite.bot.nu

## 🔧 Technologies Used
- AWS EC2 (Ubuntu 24.04)
- Nginx
- TailwindCSS
- Certbot (Let’s Encrypt SSL)
- GitHub
- Freedns

## 📸 Screenshot
![Screenshot](./images/Screenshot%20(31).png)
![Screenshot](./images/Screenshot%20(32).png)

## 📜 Deployment Steps
1. I Provisioned an EC2 instance on AWS by launching an instance with Ubuntu 24.04 LTS Operating System, a t2.micro instance type, key pair, and a security group configured to allow SSH (22) from my IP, HTTP (80) AND HTTPS (443)  

2. I gained access to the server via ssh using the command:  
```bash```  
ssh -i /path/to/your-key.pem ubuntu@ec2-public-dns  

3. I Installed nginx  
```bash```  
sudo apt install nginx  
sudo systemctl start nginx  
sudo systemctl enable nginx  

4. I cloned my github repository, created a directory for the website, and set the necessary permissions  
```bash```   
git clone (your repo link)  
sudo mkdir -p /var/www/yourdomain.com/html  
sudo chown -R $USER:$USER /var/www/yourdomain.com/html  
sudo chmod -R 755 /var/www/yourdomain.com
mv index.html /var/www/yourdomain.com/html  

5. I created a server block to specify the ports to listen on, the domain, and the files associated with it  
```bash```  
sudo nano /etc/nginx/sites-available/yourdomain.com  
sudo ln -s /etc/nginx/sites-available/yourdomain.com /etc/nginx/sites-enabled  

6. I set up HTTPS with let's encrypt   
```bash```  
sudo apt install certbot python3-cerbot-nginx  
sudo certbot --nginx

## 💡 Why This Project is Innovative
Our solution reimagines the shopping experience with AI self-checkout feature, optimizing checkout time, reduced wait times and labor costs for retailers. It is scalable, and ensures increased operational efficiency as well as a seamless experience for customers.

## 👨‍💻 About Me
 Cloud Engineer with skills in:
- AWS EC2, VPC, S3
- CI/CD pipelines (GitHub Actions, Jenkins)
- Infrastructure as Code (Terraform)
- Configuration Management (Ansible) 
- Web servers (Nginx, Apache)
- SSL & Web Security
