To use SSL with Coolify, you can follow the steps below. Coolify is a self-hosted Heroku alternative that simplifies the deployment of applications. It also provides easy SSL management. Here's how to set up SSL for your applications in Coolify:

### Prerequisites
- **Coolify Installed**: Ensure that you have Coolify installed and running on your server.
- **Domain Name**: You need a domain name pointing to your Coolify instance.
- **DNS Configuration**: Make sure your DNS settings are correctly configured to point to your Coolify server's IP address.

### Steps to Set Up SSL in Coolify

1. **Access Coolify Dashboard**:
   - Log in to your Coolify dashboard using the admin credentials.

2. **Create or Select an Application**:
   - If you haven't already deployed an application, follow the steps to create and deploy one.
   - Select the application for which you want to enable SSL.

3. **Enable SSL for Your Application**:
   - Within your application settings, locate the SSL/TLS settings.
   - Coolify integrates with **Let's Encrypt** to provide free SSL certificates.

4. **Add a Custom Domain**:
   - Under the domain settings for your application, add your custom domain name (e.g., `example.com`).
   - Ensure that the domain is correctly pointing to your Coolify instance.

5. **Request SSL Certificate**:
   - After adding the domain, you should see an option to enable SSL.
   - Click on **"Enable SSL"** or a similar option.
   - Coolify will automatically request and configure an SSL certificate for your domain using Let's Encrypt.

6. **Automatic Renewal**:
   - Coolify takes care of renewing the SSL certificate automatically. No further action is needed on your part.

7. **Verify SSL Installation**:
   - Once the SSL certificate is installed, verify that your application is accessible via `https://yourdomain.com`.
   - You can also use tools like [SSL Labs' SSL Test](https://www.ssllabs.com/ssltest/) to verify the SSL configuration.

### Troubleshooting SSL Issues
- **DNS Propagation**: Ensure that DNS changes have fully propagated. If your domain is newly pointed to the Coolify server, SSL activation might take a bit of time.
- **Firewall**: Ensure that port 443 (HTTPS) is open on your server's firewall.
- **Logs**: Check Coolify's logs if the SSL certificate request fails. It may provide insights into what went wrong.

### Important Notes
- **Wildcard Certificates**: If you need a wildcard SSL certificate (e.g., for `*.example.com`), you'll need to configure DNS validation, which might require additional steps depending on your DNS provider.
- **Manual SSL Setup**: If you prefer to use a custom SSL certificate instead of Let's Encrypt, Coolify also provides options to upload and configure your SSL certificates manually.

This approach ensures your applications hosted on Coolify are secure and accessible over HTTPS.
