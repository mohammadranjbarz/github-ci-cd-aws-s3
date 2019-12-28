### The Github ci and deploy to AWS Guid

## Setup Guilde
This is a sample code for a Medium article, First of all I recommend you to read that.
[CI/CD Using Github Actions And Amazon AWS S3](https://medium.com/@mranjbar.z2993/ci-cd-using-github-actions-and-amazon-aws-s3-9693db13adda)

## Set up a sample react app
For feeling real condition, I create a website with create-react-app to check CI/CD for a react application.

for starting the project

* `npm install`
* `npm run build`
* `npm start`


## CI/CD
You should add your AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY to settings of project ( in github panel) , secrets section
then after every push your project should be build and deploy to aws s3

### ps

All I added to project is   [./aws-upload.js](aws-upload.js) , and [./github/workflows/push.yml](./github/workflows/push.yml) , So if you want
activate github CI/CD (with amazon AWS s3 deployment)
you should just add these two files to your project and
```
     "scripts": {
       "deploy-aws": "node aws-upload.js"
       }
```

to   `package.json`
