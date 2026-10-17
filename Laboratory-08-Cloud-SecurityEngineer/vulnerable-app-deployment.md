# Vulnerable Application Deployment

## Objective
Deploy an Nginx web server container for security testing.

## Container Configuration
- Container name: secure-web-app
- Image: nginx
- Host port: 8080
- Container port: 80

## Deployment Command
`docker run -d --name secure-web-app -p 8080:80 nginx`

## Verification
The application was tested using:

`curl http://localhost:8080`

The command returned the default Nginx HTML page, confirming that the web server responded successfully.

## Screenshot
Screenshot filename: `vulnerable-app-running.png`

Location: `screenshots/vulnerable-app-running.png`

## Conclusion
The Nginx container is responding on port 8080 and is ready for subsequent security testing.
