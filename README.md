# flask
https://flask.palletsprojects.com/en/3.0.x/tutorial/

# setup


## create virtual environment

    python -m venv venv

    venv\scipts\activate

    pip install flask 

## run flask app

    flask --app flask-tutorial/hello run --debug

    flask --app flask-tutorial/flaskr run --debug
    
# init database 

     flask --app flask-tutorial/flaskr init-db

# deploy to azure with azure cli

    az account set --subscription "My Demos"
    az webapp up --runtime PYTHON:3.9 --sku F1 --logs  -n flaskr2 --settings WEBSITES_PORT=5000 --dryrun

    az webapp update  -n flaskr2  --resource-group alainkabbouh_rg_6891  --set tags.tagName=tagValue -g MyResourceGroup
