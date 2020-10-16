# Build An Alexa Fact Skill (Volley)

This is a stripped down version of this repository https://github.com/alexa/skill-sample-nodejs-fact. With simple deployment scripts included.

## To install

```
npm install
```

# To create a lambda function

1. Go to the AWS Console - Lambda: https://console.aws.amazon.com/lambda/
2. Create function
3. Give function name and choose `Create a new role with basic Lambda permissions`
4. Create function
5. Under the `Designer` subheading, click "Add Trigger"
6. Choose `Alexa Skills Kit`
7. Select "Disable" for Skill ID verification (generally, you'd set this to your skill ID, but for the purposes of this exercise, this will do)

## To deploy

First go to `package.json` and update the `update-lambda-function` script to use your lambda function (replacing the arn with the one from the lambda console). 

Then:
```
npm run deploy
```

# To create skill on Alexa Console

1. Go to the Alexa Console: https://developer.amazon.com/alexa/console/ask > Click "Create Skill" button
2. Enter a skill name > Select "Custom" model type > Select "Provision your own" backend option > Click "Create Skill" button again
3. Select "Fact Skill" template > Click "Choose" button
5. Click "Endpoint" in the left-hand navigation > Replace the ARN in "Default Region" with your own lambda function ARN > Click "Save Endpoints"
