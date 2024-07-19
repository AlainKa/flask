# flask

Repo containing the exact implementation of the flaskr application following the tutorial :


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
    az webapp up --runtime PYTHON:3.9 --sku F1 --logs  -n flaskr2  --resource-group portfolio_france_c_rg -s portfolio --dryrun

    az webapp update  -n flaskr2  --resource-group portfolio_france_c_rg  


    az webapp create --name flaskr2 --plan B1-dev --runtime PYTHON:3.9 --resource-group portfolio_france_c_rg -l  --deployment-local-git
    az webapp up  --logs  -n flaskr2  --resource-group portfolio_france_c_rg  --runtime PYTHON:3.9 --sku B1 --dryrun
