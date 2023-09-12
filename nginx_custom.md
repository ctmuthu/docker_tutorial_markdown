# Custom nginx container

To create a custom `index.html` file and serve it using an Nginx Docker container, you can follow these steps:

1. **Create a Custom `index.html` File**:

   Create a directory for your custom HTML content and create an `index.html` file inside it. For example:

   ```html
   <!-- index.html -->
   <!DOCTYPE html>
   <html>
   <head>
       <title>Custom Nginx Container</title>
   </head>
   <body>
       <h1>Hello, Custom Nginx Container!</h1>
   </body>
   </html>
   ```

2. **Run Nginx Container with Custom HTML**:

   You can use the official Nginx Docker image and mount your custom HTML directory as a volume. Here's the command to do that:

   ```bash
   docker run -d -p 80:80 -v /path/to/your/custom/html:/usr/share/nginx/html --name my-custom-nginx nginx
   ```

   Replace `/path/to/your/custom/html` with the actual path to your custom HTML directory. This command:

   - `-d`: Runs the container in detached mode (in the background).
   - `-p 80:80`: Maps port 80 of the host to port 80 of the container.
   - `-v /path/to/your/custom/html:/usr/share/nginx/html`: Mounts your custom HTML directory to the default Nginx HTML directory inside the container.
   - `--name my-custom-nginx`: Assigns a custom name to your container (you can choose any name you like).
   - `nginx`: Specifies the name of the Nginx Docker image.

3. **Access the Custom Content**:

   Once the container is running, you can access your custom HTML content by opening a web browser and navigating to `http://localhost` (if you're running Docker locally). If you're running Docker on a remote server, replace `localhost` with the server's IP address or hostname.

Your custom `index.html` content should now be served by the Nginx container, and you'll see the "Hello, Custom Nginx Container!" message when you access the web page.
