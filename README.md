# System Requirements & Setup

The microservice runs on Node.js and requires npm to install dependencies. It uses Express.js for backend routing and basic HTML/JavaScript for the frontend interface. To use the service, simply start the Node.js server, access the HTML page in a browser, and perform calculations. The system is lightweight and can be deployed on any server.

1) Download Node.js (LTS version) from https://nodejs.org/ and install it.

2) Open a terminal and navigate to your preferred directory.

3) Initialize a Node.js project through terminal:
   ```sh
   npm init -y
   ```
4) Now create `server.js` file which will work as API with a frontend HTML file, `index.html`, within `public` directory with the given codes.

5) Creating Artifact repository
   cloud artifacts repositories create sit737-2025-prac5d --repository-format=docker --location=australia-southeast1 --description="Docker repository"

6) Tag the docker image
   docker tag kvsnikhil/web_app:1.0 australia-southeast1-docker.pkg.dev/sit737-25t1-kotapati-a48c6ac/sit737-2025-prac5d/web_app:1.0

7) Authentication
   gcloud auth print-access-token | docker login -u oauth2accesstoken --password-stdin australia-southeast1-docker.pkg.dev

8) Push image
   docker push australia-southeast1-docker.pkg.dev/sit737-25t1-kotapati-a48c6ac/sit737-2025-prac5d/web_app:1.0

9) Run the image
    docker run -d -p 3000:3000 australia-southeast1-docker.pkg.dev/sit737-25t1-kotapati-a48c6ac/sit737-2025-prac5d/web_app:1.0

10) Access `http://localhost:3000` in a browser.
