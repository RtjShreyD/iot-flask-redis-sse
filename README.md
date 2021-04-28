## Flask SSE using Redis - IOT sensor data values update in real time on Fronted over POST API HTTP.

### Run with Docker

1. Clone this repository.

2. cd in repository.

3. Run with Docker compose - `sudo docker-compose up`.

4. Watch the app on http://localhost:5000.

5. Using Postman or any tool send POST request with header *content-type --> text-plain* and send any numerical string, to route `/therm/push`.

6. To stop the service run, `docker-compose down`.


### Run Manually with python

1. Install Redis, following the [redis docs](https://redis.io/topics/quickstart).

2. Clone the repository.

3. Create and Activate python virtual environment.

4. Install requirements `pip install requirements.txt`.

5. Run Redis command in new terminal, `redis-server`.

6. Run App, `python app.py` and wa it on http://localhost:5000.

7. Using Postman or any tool send POST request with header *content-type --> text-plain* and send any numerical string to route `/therm/push`. We can send a POST request from a new terminal as well by running, 
`curl -X POST -H "Content-Type: text/plain" -d '{"temperature":56}' http://localhost:5000/therm/push`. 

8. The value should get updated immediately on frontend without reloading it.

9. To stop the redis-server, press Ctrl+C or if the terminal got closed by mistake Redis would still be running, so run `redis-cli shutdown` to close it.

