## Powerplate

### Demo
https://powerplate.herokuapp.com/

## Features

###

## Development

Run `npm run dev` for server-side live reload.  
Run `npm run eslint` to lint the code.

## Testing
Run `npm test`  
If asked for snyk authentication, run `./node_modules/.bin/snyk auth`

## Deployment

Deployment will fail if linting causes error.

### Deploy to Heroku via Docker

#### Preparation

+ Make sure you have a working Docker installation
```bash
# Install Heroku CLI
brew install heroku

# Login to Heroku
heroku login

# Create a Heroku app
heroku apps:create your-app-name

# Add heroku remote
heroku git:remote -a your-app-name

# Set up mLab add-on
heroku addons:create mongolab -a your-app-name

# Install Heroku container registry
heroku plugins:install heroku-container-registry

# Log in to Heroku container registry
heroku container:login

# Deploy to heroku
npm run heroku-push
```

Everytime you want to update your heroku, just re-run the command
```bash
npm run heroku-push
```

If you want to have multiple environment, follow the example in `package.json`

## Future Plan

- Add React