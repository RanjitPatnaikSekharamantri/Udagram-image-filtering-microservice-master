# RanjitPatnaik-Udagram-image-filtering-microservice

# Udagram Image Filtering Microservice

# Github Repository https://github.com/ranjit-patnaik/Udagram-image-filtering-microservice-master

This is the second assignment for the [Udacity Cloud Developer Nanodegree](https://www.udacity.com/course/cloud-developer-nanodegree--nd9990) course.

It is a Node-Express application which runs a simple script to process images, and is deployed using AWS Elastic Beanstalk.

 You'll need to create a new node server. we should open a new terminal within the project directory and run:

    Initialize a new project: npm i
    run the development server with npm run dev

Create a new endpoint in the server.ts file :

The starter code has a task for you to complete an endpoint in ./src/server.ts which uses query parameter to download an image from a public URL, filter the image, and return the result.

I included the few helper functions to handle some of the concepts and I importing it for you at the top of the ./src/server.ts file.

import {filterImageFromURL, deleteLocalFiles} from './util/util';

Deploying your system :

Follow this process described in the terminal to eb init a new application and eb create the new environment to deploy your image-filter service Don not forget you can use the eb deploy to push changes.


> For deploying used :

```terminal
   npm run build
   eb init
   eb create
   eb deploy
```

### Usage
**Base url:** http://localhost:8082
#### filtering an image
| Path | Parameter | Description |
| :--- | :--- | :--- |
| filteredimage | `image_url` | **Required**. The image url to filter |

**Example:** http://localhost:8082/filteredimage?image_url=https://www.gstatic.com/webp/gallery3/1.png

Note: _All API requests __require__ authorization headers_ (click [here](http://localhost:8082/token) to generate a token).

- AWS Elastic Beanstalk deployed application dashboard.
  ![depcruise generated graph](./deployment_screenshot/eb_app_deployed_and_running_on_aws.png)

*Postman collection file is [here](https://github.com/RanjitPatnaik/Udagram-image-filtering-microservice-master/blob/master/cloud-cdnd-c2-final.postman_collection.json).*
