# botman-starter

A basic project ready-to-use of chatbot BotMan Studio running inside a Docker container. You can get more infomation in <https://botman.io>.

## How to use

1. Install Docker. To do this go to <https://www.docker.com/get-started/><br>
2. Make a clone of this repository in your computer or download this project in zip format and extract in your computer.<br>
3. Inside the clone's directory run these commands to create the container and start him:<br>
`docker-compose build`<br>
`docker-compose up -d`<br>
4. Run this command to access the container's shell:<br>
`docker exec -it botman-starter bash`<br>
5. Inside the container's shell run these commands to create .env file, generate a key to the Laravel application and download/update composer's packages:<br>
`cd /app/`<br>
`cp .env.example .env`<br>
`php artisan key:generate`<br>
`composer update`<br>

From now you can access <http://localhost/botman/tinker> to verify if the application is running correctly.<br>
Send "hi" to the chatbot and he must reply. Send "start conversation" to a interactive conversation.

## Programming the chatbot

All modifications made into the code inside the `app_botman` directory in the host computer will reflect immediately in the running application inside container.

For more information about programming the chatbot access the BotMan's documentation in <https://botman.io/2.0/welcome>.
