# Django + Vite Starting Point
This project serves as a starting point for me to use as a starting point for Django applications that use Vite as the asset server for development.

## Strategy
This application is a hybrid MPA and SPA. There is a separate page for signup/signin. Once a user is logged in they are redirected to the / view which then renders the SPA application created using React and Vite.

## Creating a new application
1. Clone the repo `git clone https://github.com/Michael-Holmes-SDE/React-Django_starter.git <your-new-project-name>`. Replace `<your-new-project-name>` with the name you want give to your project.
2. Open the pyproject.toml file and change the `name` property. You should use `-` to separate words in your name for this property.
3. This project was set up using Python 3.11. You might have an older version installed. If you run into an error later that says that your activated Python version isn't compatible, the in the pyproject.toml file, just change the version there to match the version that you have installed. If you do this, you need to make sure that the lock file gets regenerated. You can do this by running `poetry lock --no-update` or by simply deleting the poetry.lock file (it will get regenerated when you run poetry install).

## Initial Setup
1. Change the name property in the `pyproject.toml` file to be something unique to your project.
1. In the root directory, install the python dependencies `poetry install`
2. In the `client` directory, install the javascript dependencies `npm install`
3. In the `_server` directory, create a new file called `.env`
4. Copy the contents of `_server/.env.example` into the newly created `.env` file.
5. Activate the poetry env `poetry shell`
6. In the `_server` directory, run the migrations `python manage.py migrate`

## Running the application
1. In the `client` directory run `npm run dev`
2. In the `_server` directory (with your poetry env activated) run `python manage.py runserver`
3. Visit your application at `http://localhost:8000`

# IMPORTANT: This is based almost entirely on the work done by my former professor Joseph Ditton
