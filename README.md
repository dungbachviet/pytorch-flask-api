This repository referred from [original repository](https://github.com/avinassh/pytorch-flask-api) that i learned how to deploy a basic machine learning model using Flask framework.

To make the original code work well, I revised the source code at some points:

- requirements.txt: in this file, i replaced library versions to well-worked versions on my running time.
- images folder: i supplement this folder containing test images for inference.
- Change command to run Flask server from "FLASK_ENV=development FLASK_APP=app.py flask run" to "python app.py"

# PyTorch Flask API

This repo contains a sample code to show how to create a Flask API server by deploying our PyTorch model. This is a sample code which goes with [tutorial](https://pytorch.org/tutorials/intermediate/flask_rest_api_tutorial.html).

If you'd like to learn how to deploy to Heroku, then check [this repo](https://github.com/avinassh/pytorch-flask-api-heroku).

## How to

Clone the github code to local:

    git clone https://github.com/dungbachviet/pytorch-flask-api.git

Set up your virtual environment (point your terminal to the project directory "pytorch-flask-api")

    virtualenv -p python3 virtual-environment-name
    Ex: virtualenv -p python3 my_env

Activate your virtual enviroment on terminal:

    source virtual-environment-name/bin/activate
    Ex: source my_env/bin/activate

Install the dependencies (for your virtual enviroment)

    pip install -r requirements.txt

Run the Flask server (more details: a pretrained model ResNet will be downloaded and saved at somewhere in your local computer, then server will be running at your localhost http://localhost:5000/)

    python app.py

From another terminal tab, using curl to send the image file in a request to your localhost server, after that a prediction result will be returned soon:

    curl -X POST -F file=@./images/cat_pic.jpeg http://localhost:5000/predict

## License

The mighty MIT license. Please check `LICENSE` for more details.
