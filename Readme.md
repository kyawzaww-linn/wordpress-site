# WordPress Child Theme Development and Deployment

Welcome to the **WordPress Child Theme Development** project for [Neve](https://themeisle.com/themes/neve/)! 🎉 This project is all about customizing the Neve theme and deploying the website on AWS. Whether you're the first developer here or someone coming in later, this documentation will guide you through theme development and deployment.

## Key Features
- 🎨 Custom Child Theme based on Neve
- 📱 Fully responsive across mobile, tablet, and desktop
- 🎨 Navy blue (#000080) and white (#FFFFFF) color scheme
- 🗓️ Custom-coded event calendar (no plugins here!)
- 🌐 Hosted on AWS EC2 with a LAMP stack

---

## Theme Development

### Child Theme Structure

Below is the structure of the child theme directory (`neve-child-theme`). Everything starts here!

```bash
neve-child-theme/
├── style.css             # Custom styles (navy blue and white)
├── functions.php         # Enqueues parent theme styles & scripts
├── footer.php            # Custom footer for the child theme
├── header.php            # Custom header
└── templates/
    └── events.php        # Custom event calendar template
```

### Customizations Made

- **Custom Styles**: We’ve swapped out some of Neve's default styles for a navy-blue-and-white palette.
- **Custom Footer**: The footer has been customized to remove the default "Neve | Powered by WordPress" text and replaced with something fancier.
- **Event Calendar**: The calendar is 100% custom-coded. It's interactive, lightweight, and no plugins were harmed in its creation.

### Making Changes

Want to tinker around with the theme? Here’s what to do:

1. **Style Tweaks**: Head to `style.css` and go wild with your CSS changes.
2. **PHP Templates**: Edit header and footer stuff in `header.php` and `footer.php`. Want to customize a specific page? Pop your new PHP templates in the `templates/` directory.
3. **Add New Scripts**: Use `functions.php` to add new scripts or styles. Just make sure everything’s enqueued properly. No rogue JavaScript allowed! 😜

### Development Workflow

1. Clone the repo:
   ```bash
   git clone https://github.com/kyawzaww-linn/wordpress-site.git
   ```

2. Create a new branch for your changes:
   ```bash
   git checkout -b feature-awesome-update
   ```

3. When you're done coding, commit and push:
   ```bash
   git commit -m "Added awesome feature"
   git push origin feature-awesome-update
   ```

4. Before you deploy, make sure you test everything locally first!

---

## Deployment

### Deployment to AWS EC2

This project is hosted on AWS EC2 using a LAMP stack. Here’s how you can get it up and running or update the live site.

1. **Access the EC2 Instance**:
   SSH into your instance like this:
   ```bash
   ssh -i "your-key.pem" ubuntu@your-ec2-public-ip
   ```

2. **Navigate to WordPress Themes**:
   ```bash
   cd /var/www/html/wp-content/themes
   ```

3. **Pull Latest Changes from GitHub**:
   ```bash
   git pull origin main
   ```

4. **Restart Apache**:
   ```bash
   sudo systemctl restart apache2
   ```

5. **Check the Site**: Visit your public IP in a browser to make sure your changes look ✨awesome✨:
   ```bash
   http://your-ec2-public-ip
   ```

### Making Future Changes

1. **Make Changes Locally**: Tweak the child theme on your local machine.
2. **Test Everything**: Always test before pushing live. No one likes broken websites. 😉
3. **Push Changes**: Once you’re happy with your work, push those updates to GitHub:
   ```bash
   git push origin main
   ```

4. **Deploy to Production**:
   - SSH into your EC2 instance.
   - Pull the changes from GitHub.
   - Restart Apache, and you’re good to go!

---

## Conclusion

And there you have it—everything you need to develop and deploy this WordPress child theme like a pro! 💪 If you run into any issues or just want to say hi, feel free to reach out to [kyawzawwlinn279@gmail.com].

Happy developing! 🚀✨
